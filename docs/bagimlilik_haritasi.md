# Bağımlılık Haritası v2

Kaynak: 01 Kurulum Paketi v2 §4. İP'lerin **güncel durumu** Durum Tablosu v2'de ve Semrük Ana Dosya'dadır.
İki hat vardır: **ÖTR hattı** ön tasarım düzeyindedir ve ÖN SEÇİM üretir; **KTR hattı** katı kapılarla devam eder.

## ÖTR hattı (şimdiki dönem)
```
T0 → Ö0 → Ö1 → Ö2 → (Ö3 ‖ Ö5) → Ö7 → Ö8 → Ö9
Ö4, T0 ile başlar ve Ö3'ten bileşen adlarını alır.
```

| İP | Sahip | İş | Girdi | Çıktı | Kapı kriteri (Konti) | Tarih (Plan v3) |
|---|---|---|---|---|---|---|
| Ö0 | Sis | ÖTR planı: bölüm sahipleri, sayfa bütçesi, iç teslim tarihleri, takım şeması taslağı | T0 | ÖTR plan sayfası | Her bölümün sahibi ve tarihi var; R17 sağlanıyor | İskelet 06.12, takım şeması 13.12 |
| Ö1 | Meka | Mekanik ön konsept: 2 eksen mimari, atış modülü ailesi, ≤60 cm zarf, kütle v0, mekanik bileşen tablosu, 3B ön model görseli | T0 | Konsept notu, bileşen tablosu, görsel | Her bileşenin neden gerektiği yazılı; R01, R06 ile uyumlu | M1 v1 27.12 → M2 v0 24.01 → 31.01; bölüm 07.02 |
| Ö2 | Avi | Donanım ön seçimi: motor, sürücü, enkoder, kamera, işlemci, güç kartı, e-stop; tork ve güç ön hesabı; kablo bazlı blok şema v0 | Ö1 | Donanım tablosu, blok şema v0, ön hesaplar | Tork ve güç hesabı tekrarlandı; blok şemada her bağlantının tipi ve kablosu var | A1 v0 31.01; §3.3 07.02; blok şema ve §3.1 14.02 |
| Ö3 | Kodi | Yazılım mimarisi: bileşen tablosu (hazırlarda üretici ve sürüm), yazılım arayüz şeması, temel gereksinimler | Ö2 (kamera ve işlemci) | Yazılım tablosu, arayüz şeması | Arayüzler Ö2 blok şemasıyla çelişmiyor | Tablo 31.01; bölüm 14.02 |
| Ö4 | Kodi | Yöntem: Aşama-1/2/3 aktivite ve sekans diyagramları; mod geçişi durum makinesi | T0 (+Ö3 bileşen adları) | 6 diyagram + durum makinesi | Her diyagram R05, R08–R10 kurallarıyla eşleşiyor | Durum makinesi 27.12; diyagramlar H10–H12; bölüm 14.02 |
| Ö5 | Sis | Malzeme listesi ve bütçe; zaman planı; proje takip aracı | Ö1, Ö2, Ö3 | BOM, bütçe, Gantt | Fiyatlar kaynaklı; toplam bütçe varsayımıyla karşılaştırıldı | 14.02 |
| Ö7 | Sis | Derleme: proje özeti, takım şeması, kaynakça, biçim, 10 sayfaya sığdırma | Ö0–Ö5 İNCELEMEDE geçmiş | ÖTR taslağı | R16, R17, R18 kontrol listesi tam | Taslak v1 21.02; uyarlama ve dondurma 05.03 |
| Ö8 | Konti | Hakem incelemesi: bölüm bölüm puan tahmini, hesap tekrarı, şartnameye uygunluk, alıntı ve intihal kontrolü | Ö7 | İnceleme raporu, düzeltme listesi | Tüm düzeltmeler kapandı | H14 (22–28.02) |
| Ö9 | Kaptan | Son onay ve KYS yükleme (son günden en az 2 gün önce) | Ö8 | Yüklenmiş ÖTR | Yükleme teyidi | 08.03 (resmî son tarih tahmini 17.03, 17:00) |

**P1 ile eşleşme:** Ö1 = M1 v1 + M2 v0 (kütle, tork tahmini) + 3B model; Ö2 = A1 v0 + A2 v0 (blok şema);
Ö3 = yazılım ön tasarımı (Y1–Y3 kavramsal); Ö4 = Y4 ön tasarımı (aşama diyagramları, durum makinesi).

Notlar: Numaralandırmada Ö6 yok. Ö7'nin girdisi Kurulum Paketi v2'de "Ö0–Ö5", Ana Dosya v5'te "Ö0, Ö4, Ö5" yazıyor;
bu depo Kurulum Paketi'ni izler.

## KTR hattı (ÖTR sonrası)
```
T0 → M1 → M2 → A1 → A2 → (M3 ‖ Y1 ‖ Y3) → Y2 → Y4;  M3 → M4 → T1 → T2 → T3 → T4
T5 (KTR derleme) Sis'tedir ve bölümler onaylandıkça ilerler.
```

| İP | Sahip | İş | Girdi (ONAYLI) |
|---|---|---|---|
| T0 | Sis | Gereksinim taban çizgisi, açık sorular, takvim doğrulama (**ONAYLI 21.11.2026**, ≤60 cm kararıyla) | Dosyalar |
| M1 | Meka | Konsept: 2 eksen mekanizma, atış modülü, ≤60 cm zarf, açı-hız-ivme, parkur geometrisi (Ö1 ile birlikte yürür) | T0 |
| M2 | Meka | Kütle, atalet, tork, rijitlik, geri tepme; dondurulmuş arayüz zarfı | M1 |
| A1 | Avi | Güç bütçesi, motor, sürücü, enkoder/limit, 220 VAC→DC | M2 |
| A2 | Avi | Kontrol mimarisi, e-stop zinciri, tetik, haberleşme, kamera şartnamesi, blok şema, ICD v1 | A1 |
| M3 | Meka | Detay tasarım, kablo yolu, montaj, teknik resim | A2 |
| Y1 | Kodi | Algılama, sınıflandırma, mesafe tahmini | A2 |
| Y3 | Kodi | Arayüz: GUI/joystick/klavye, mod geçişi, e-stop durumu, yasak alan tanımı | A2 |
| Y2 | Kodi | Takip ve atış kontrol | Y1, M2, A2 |
| Y4 | Kodi | Aşama-1/2/3 durum makineleri, puan mantığı | Y2, Y3 |
| M4 | Meka | İmalat, montaj, ölçüm | M3 |
| T1 | Konti | Alt sistem testleri | M4, Y4 |
| T2 | Konti | Entegrasyon testi | T1 |
| T3 | Konti | Video yetenek provası (1–7); video planı Sis'te | T2 |
| T4 | Konti | Aşama provaları; 30 dk hazırlık ve 10 dk bakım planı Sis'te | T3 |
| T5 | Sis | KTR ve final sunumu derleme | Bölüm İP'leri |
