# Öğrenme Rehberi – Konti (Doğrulama, Analiz ve Geliştirme)

Sorumlu: **Yusuf Köse (kaptan)** ve **Sıla Doğan**

**Amaç:** Konti rolünü üstlenen kişinin sistemi bağımsız doğrulama, gereksinim yönetimi, test, risk ve KTR derlemesi
konularında yönetebilmesi. Konti diğer üç departmanın işini yapmaz; kapıda "doğru mu?" sorusunu cevaplar.

## 1. Öğrenme listesi
Öncelik: **A** = T0/M1 aşamasında · **B** = ilk kapılardan önce · **C** = test ve rapor aşamasında

| # | Konu | Öncelik | Neden (iş) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 1 | Gereksinim mühendisliği: ölçülebilir/test edilebilir gereksinim, izlenebilirlik matrisi | A | T0: R01–R15 | Bir gereksinimi test edilebilir hâle getirir, İP ve teste bağlarsın | [ ] |
| 2 | Sistem mühendisliği yaşam döngüsü (V modeli) | A | Bağımlılık haritası ve kapılar | Kapı kriterlerini V modeline eşlersin | [ ] |
| 3 | Doğrulama yöntemleri: analiz, test, inceleme, gösterim | A | Her kapıda onay kriteri | Her REQ için doğrulama yöntemini seçersin | [ ] |
| 4 | Arayüz yönetimi: ICD, dondurulmuş zarflar, değişiklik kontrolü | A | M2/A2 sonu, DT | Bir ICD sayfası yazarsın (kim, ne, birim, sürüm) | [ ] |
| 5 | Bağımsız hesap kontrolü: büyüklük mertebesi, birim analizi, sınır durumu | A | Her kapıda | Meka/Avi'nin tork ve güç hesabını kendi yönteminle tekrarlarsın | [ ] |
| 6 | FMEA ve hata ağacı (RPN/AP) | B | A2: e-stop, yasak alan | E-stop için FMEA tablosu doldurursun | [ ] |
| 7 | Güvenlik ve risk değerlendirmesi (hata-güvenli tasarım) | B | KTR §6, Şart. 4.2 | Bir alt sistem için "hata durumunda güvenli" gerekçe yazarsın | [ ] |
| 8 | Kötü gün senaryoları: kablo kopması, güç kesintisi, yazılım çökmesi, yanlış hedef, ışık | B | KTR §4.4.3, T1/T2 | 10 senaryo listeleyip beklenen davranışı yazarsın | [ ] |
| 9 | Test tasarımı: plan, kabul kriteri, test seti bağımsızlığı, kayıt | B | T1–T4 | Girdi/adım/beklenen sonuç/geçti-kaldı içeren test planı yazarsın | [ ] |
| 10 | İstatistik: ortalama, std, güven aralığı, hata matrisi, kesinlik/geri çağırma | B | Y1 doğrulama, isabet | 20 atışın isabet oranını güven aralığıyla yorumlarsın | [ ] |
| 11 | Entegrasyon stratejisi | C | T1–T2 | Entegrasyon sırasını ve başarısızlık kriterlerini yazarsın | [ ] |
| 12 | Puan stratejisi ve simülasyon (Şart. 6) | C | T4 | Aşama-1/2/3 beklenen puan tablosu ve riskli karar noktaları çıkarırsın | [ ] |
| 13 | Operasyon planı: 30 dk hazırlık, 10 dk bakım, kontrol listeleri, roller | C | R13, T4 | Yarış günü zaman çizelgesi ve rol kartları hazırlarsın | [ ] |
| 14 | Proje yönetimi: WBS, kritik yol, zaman-bütçe-risk matrisi | A | Tüm süreç, KTR | 4 aylık kritik yol ve risk matrisi hazırlarsın | [ ] |
| 15 | Diyagramlar: SysML/UML (blok, use case, durum, sekans) | C | KTR §4.4 | Sistem blok ve sekans diyagramı çizersin | [ ] |
| 16 | Teknik rapor yazımı: KTR yapısı, puan kriterleri, kaynakça ve alıntı | A | KTR (50 puan) | Her KTR bölümünün puanını ve hakemin ne arayacağını açıklarsın | [ ] |
| 17 | Kök neden analizi (5 Neden, balık kılçığı), düzeltici faaliyet | C | T1–T4 | Bir test başarısızlığı için kök neden ve düzeltici faaliyet yazarsın | [ ] |

## 2. 2 haftalık plan (T0 ve M1 ile paralel)
- **Hafta 1:** konu 1, 2, 3, 14, 16 → REQ listesi sürümü + 4 aylık kritik yol taslağı
- **Hafta 2:** konu 4, 5, 6, 8 → ICD şablonu + e-stop FMEA taslağı (Avi'den önce hazır olsun)

**Öğrenme kanıtı:** Her konu için 1 sayfa → `ogrenme/kanitlar/konti/` (KTR Zaman-Bütçe-Risk, Test, Güvenlik, Tecrübe).

## 3. Kaynaklar
**Kitaplar:** *NASA Systems Engineering Handbook* (NASA/SP-2016-6105, ücretsiz) · *INCOSE SE Handbook* ·
Blanchard & Fabrycky, *Systems Engineering and Analysis* · Wiegers & Beatty, *Software Requirements* ·
AIAG & VDA FMEA El Kitabı · Friedenthal, Moore & Steiner, *A Practical Guide to SysML* ·
Montgomery & Runger, *Applied Statistics and Probability for Engineers* · 5 Neden / Ishikawa ders notları

**Standartlar:** ISO/IEC/IEEE 29148 · ISO/IEC/IEEE 15288 · IEC 60812 · ISO 12100, ISO 13850, ISO 13849-1

**Ders:** MIT OCW, edX/Coursera (Systems Engineering, Project Management, Statistics) · NASA ve INCOSE materyalleri ·
yayımlanmış ÖTR/KTR örnekleri (format için)

**Yarışma (birincil):** Şartname v1.5 (özellikle §2.4, §6) · KTR şablonu (Arial 12, 1,15, 2,5 cm, ≤30 sayfa) ·
TEKNOFEST Genel Kurallar ve Etik Kurallar · Soru&Cevap grubu (her belirsizliği kaydet, REQ'e işle)

**Araçlar:** Google Sheets (durum, REQ, risk), Google Docs/Drive, draw.io, Python, isteğe bağlı SysML aracı

## 4. Ajanla çalışma
- Konti'yi hakem gibi kullan: "Bu notun zayıf noktalarını ve eksik REQ eşlemelerini bul."
- Hesap doğrulatırken önce kendi sonucunu yaz, sonra Konti'ye karşılaştırt; aksi hâlde "bağımsız" olmaz.
- Konti'nin bulgusunu sahibine geri ver; tasarımı Konti yapmasın.
