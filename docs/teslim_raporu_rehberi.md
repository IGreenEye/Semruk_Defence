# Teslim Raporu Rehberi

Kaynak: 03_Teslim_Raporu_Rehberi. Örneklerdeki değerler **ÖRNEK DEĞERDİR**, tasarım kararı ya da tavsiye değildir.
Örnekler v1 dönemindendir (M1, A1, Y1). Kurulum Paketi v2'de ÖTR işleri Ö hattında yürür: Örnek A'nın ÖTR karşılığı Ö1,
Örnek B'ninki Ö2, Örnek C'ninki Ö3'tür ve hedef durum ONAYLI değil **ÖN SEÇİM**'dir. "Rapor bölümüne katkı" satırları
ÖTR bölümlerine çevrildi (`docs/otr_rehberi.md`). Örnek A'nın sorumlusu artık Sezen'dir.

## Beş temel kural
- Her sayının birimi ve kaynağı yazılır. "Yeterli tork" değil, "3,5 N·m (hesap: m·g·r·2)".
- Hesap görünür olmalı; Konti bağımsız tekrarlayacak.
- Bilinmeyen değer uydurulmaz: `VARSAYIM` yaz, ne zaman netleşeceğini söyle.
- Her karar bir gereksinime (R01–R15) bağlanır.
- "Bağımlı İP'lere etkisi" boş bırakılmaz.

## ÖRNEK A – Meka · M1 Konsept Notu
**Girdiler:** T0 v1 (REQ, ≤60 cm kararı), Parkur Çizimi PLG26-A-001-002-00

| Büyüklük | Değer | Birim | Kaynak | Güven |
|---|---|---|---|---|
| En uzun boyut hedefi | 55 | cm | R01 (≤60), 5 cm marj | yüksek |
| Yaw açı aralığı | ±60 | derece | atan(5/5)=45° + 15° marj | orta |
| Pitch aralığı | −10 / +25 | derece | atan(1,5/5)=16,7° + marj | düşük |
| Başlangıç pozisyonu | 0 / 0 | derece | R04 | yüksek |
| Hedef yaw hızı | 90 | derece/s | örnek hareketli hedef hesabı | düşük |

- Karar: 2 eksenli (yaw+pitch) platform (Şart. 5.1, R01). Yaw'da ±60° mekanik durdurucu (R03). Patlatma modülü: [seçilen aile] (R06).
- VARSAYIM: gövde yüksekliği 0,5 m, hedef yüksekliği 0,3–2,0 m. VARSAYIM: balon çapı şartnamede yok (S&C).
- Risk: hedef yüksekliği farklıysa pitch yetmeyebilir → çizim doğrulaması + ±5° yedek.
- Bağımlı İP: M2 (açı, zarf, atalet), A1/A2 (dönme aralığı, enkoder), Y2 (yasak alan sınırları). ÖTR: §3.2 Mekanik Tasarım (bileşen tablosu, 3B model görseli).

## ÖRNEK B – Avi · A1 Motor ve Güç Notu
**Girdiler:** M2 v1, T0 v1

| Büyüklük | Değer | Birim | Kaynak | Güven |
|---|---|---|---|---|
| Pitch yük torku (statik) | 1,77 | N·m | 1,2 kg · 9,81 · 0,15 m | orta |
| Gereken çıkış torku (2× marj) | 3,53 | N·m | 1,77 · 2 | orta |
| Redüktör oranı | 10:1 | – | tasarım seçimi | orta |
| Gereken motor torku | 0,42 | N·m | 3,53 / 10 / 0,85 | orta |
| Pik güç (iki motor) | 150 | W | katalog | düşük |
| Güç kaynağı (1,6× marj) | 240 | W | 150 · 1,6 | orta |

- Karar: 220 VAC → 24 VDC (R11). Enkoder + limit anahtarı (R03).
- VARSAYIM: redüktör verimi %85. VARSAYIM: atalet torku statik torkun altında.
- Risk: tedarik gecikmesi → iki alternatif üretici.
- Bağımlı İP: A2 (sürücü arayüzü), M3 (montaj, kutu hacmi), Y2 (PWM/seri arayüz). ÖTR: §3.3 Donanım Tasarımı (üretici, model, fiyat tablosu), §3.5 Malzeme Listesi.

## ÖRNEK C – Kodi · Y1 Algılama Notu
**Girdiler:** A2 v1 (kamera spec, ICD), T0 v1

| Büyüklük | Değer | Birim | Kaynak | Güven |
|---|---|---|---|---|
| Balon tespit doğruluğu (5/10/15 m) | ≥95 | % | Konti test seti | orta |
| Hedef sınıflandırma doğruluğu | ≥90 | % | yetenek 6 | düşük |
| Uçtan uca görüntü gecikmesi | ≤50 | ms | ölçüm planı | düşük |
| Kare hızı | ≥30 | FPS | kamera spec | orta |
| Mesafe hatası (10 m) | ±0,5 | m | Z²/(f·D)·Δd, Δd=1 px | orta |
| Mesafe hatası (15 m) | ±1,1 | m | aynı formül | orta |

(f = 1000 px, D = 0,20 m VARSAYIM)
- Karar: iki aşamalı algoritma (renk → maket sınıflandırma) (R09, R10). Tek kamera + bilinen boyuttan mesafe.
- Risk: F16 10 m sınırında mesafe hatası puan kaybı → ikinci yöntem veya güvenlik payı.
- Bağımlı İP: Y2, Y4, T1. ÖTR: §3.4 Yazılım Tasarımı (bileşen tablosu, arayüz şeması).

> **ÖTR dönemi notu:** Bu örnekteki doğruluk ve gecikme değerleri ÖTR'de "ölçüm" değil **hedef** olarak yazılır;
> ölçüm KTR döneminde yapılır. ÖTR'de kod paylaşılmaz.

## Sık yapılan hatalar
Birim/kaynak eksik · varsayımı kesin gibi yazmak · REQ bağlantısı yok · "Bağımlı İP" boş ·
ONAYLI notu DT'siz güncellemek · durum tablosuna bakmadan sonraki İP'ye başlamak.
