# Bağımlılık Haritası – ÖTR hattı

Kaynak: 01 Kurulum Paketi v2.1. İP'lerin **güncel durumu** Durum Tablosu v2'de ve Semrük Ana Dosya'dadır; tarihler
Semrük Proje Planı v4'tedir. **Kapsam kuralı:** bu harita yalnızca ÖTR dönemini kapsar. ÖTR'den sonraki iş paketleri
ÖTR resmî son tarihinden sonra ayrı bir planla tanımlanacak.

```
T0 (ONAYLI) → Ö0 → Ö1 → Ö2 → (Ö3 ‖ Ö5) → Ö7 → Ö8 → Ö9
Ö4, T0 ile başlar ve Ö3'ten bileşen adlarını alır. T0 v2, 2027 şartnamesi gelince Sis'te yürür.
```

| İP | Sahip | İş | Girdi | Çıktı | Kapı kriteri (Konti) | Tarih |
|---|---|---|---|---|---|---|
| T0 | Sis | Gereksinim taban çizgisi R01–R18, açık sorular | Dosyalar | REQ listesi | **ONAYLI 21.11.2026** (≤60 cm kararıyla) | – |
| T0 v2 | Sis | 2027 şartnamesindeki farkların REQ listesine işlenmesi; S&C soruları | 2027 şartnamesi | REQ güncellemesi | Tam kapı; Sezen veya Eren yanında doğrulanır | 10.01 |
| Ö0 | Sis | ÖTR planı: bölüm sahipleri, sayfa bütçesi, iç teslim tarihleri, takım şeması taslağı | T0 | ÖTR plan sayfası | Her bölümün sahibi ve tarihi var; R17 sağlanıyor | İskelet 06.12, takım şeması 13.12 |
| Ö1 | Meka | Mekanik ön konsept (M1 v1 tam kapı + M2 v0): 2 eksen mimari, atış modülü ailesi (kâğıt üzerinde), ≤60 cm zarf, kütle v0, mekanik bileşen tablosu, 3B ön model görseli | T0 | Konsept notu, bileşen tablosu, görsel | Her bileşenin neden gerektiği yazılı; R01, R06 ile uyumlu; geometri bağımsız yeniden hesaplandı | M1 v1 27.12 → M2 v0 24.01 → 3B model 31.01; bölüm 07.02 |
| Ö2 | Avi | Donanım ön seçimi (A1 v0 + A2 v0): motor, sürücü, enkoder, kamera, işlemci, güç kartı, e-stop; tork ve güç ön hesabı; kablo bazlı blok şema | Ö1 | Donanım tablosu, blok şema, ön hesaplar | Tork ve güç hesabı tekrarlandı (fark ≤%10); blok şemada her bağlantının tipi ve kablosu var | A1 v0 31.01; §3.3 07.02; blok şema ve §3.1 14.02 |
| Ö3 | Kodi | Yazılım ön tasarımı: bileşen tablosu (hazırlarda üretici ve sürüm), yazılım arayüz şeması, temel gereksinimler; kod yok | Ö2 (kamera ve işlemci) | Yazılım tablosu, arayüz şeması | Arayüzler Ö2 blok şemasıyla çelişmiyor | Tablo 31.01; bölüm 14.02 |
| Ö4 | Kodi | Yöntem: Aşama-1/2/3 aktivite ve sekans diyagramları; mod geçişi durum makinesi | T0 (+Ö3 bileşen adları) | 6 diyagram + durum makinesi | Her diyagram R05, R08–R10 kurallarıyla eşleşiyor | Durum makinesi 27.12; diyagramlar H10–H12; bölüm 14.02 |
| Ö5 | Sis | Malzeme listesi ve bütçe; ÖTR §5 tahmini takvim metni; proje takip aracı | Ö1, Ö2, Ö3 | BOM, bütçe, takvim metni | Fiyatlar kaynaklı ve tarihli; toplam bütçe varsayımıyla karşılaştırıldı | 14.02 |
| Ö7 | Sis | Derleme: proje özeti, takım şeması, kaynakça, biçim, 10 sayfaya sığdırma, bölümler arası tutarlılık | Ö0–Ö5 (Ö1–Ö4 dahil) İNCELEMEDE geçmiş | ÖTR taslağı | R16, R17, R18 kontrol listesi tam | Taslak v1 21.02; uyarlama ve dondurma 05.03 |
| Ö8 | Konti | Hakem incelemesi: bölüm bölüm puan tahmini, hesap tekrarı, şartnameye uygunluk, alıntı ve benzerlik kontrolü | Ö7 | İnceleme raporu, düzeltme listesi | Tüm düzeltmeler kapandı | H14 (22–28.02) |
| Ö9 | Kaptan | Son onay ve KYS yükleme (son günden en az 2 gün önce) | Ö8 | Yüklenmiş ÖTR | Yükleme teyidi | 08.03 (resmî son tarih tahmini 17.03, 17:00) |

**P1 ile eşleşme:** Ö1 = M1 v1 + M2 v0 (kütle, tork tahmini) + 3B model; Ö2 = A1 v0 + A2 v0 (blok şema);
Ö3 = yazılım ön tasarımı (kavramsal); Ö4 = aşama diyagramları ve durum makinesi.

Not: Numaralandırmada Ö6 kullanılmıyor.
