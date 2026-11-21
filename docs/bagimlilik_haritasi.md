# Bağımlılık Haritası

Kaynak: 01_Kurulum_Paketi, Bölüm 3.

```
T0 → M1 → M2 → A1 → A2 → (M3 ‖ Y1 ‖ Y3) → Y2 → Y4
                          M3 → M4 → T1 → T2 → T3 → T4
T5 (KTR/final derlemesi): her bölüm kendi İP'si onaylandıkça ilerler.
```

| İP | Sahip | İş | Girdi (ONAYLI olmalı) | Çıktı | Onay kriteri (Konti) |
|---|---|---|---|---|---|
| T0 | Konti | Gereksinim taban çizgisi, açık sorular, takvim doğrulama | Dosyalar | REQ listesi, Soru&Cevap listesi | Kullanıcı onayı |
| M1 | Meka | Konsept: 2 eksen mekanizma, atış modülü tipi, ≤60 cm zarf, açı/hız/ivme, parkur geometrisi | T0 | Karar kaydı, kinematik gereksinimler | Her karar bir REQ'e izlenebilir; geometri bağımsız yeniden hesaplandı |
| M2 | Meka | Kütle, atalet, tork, rijitlik, geri tepme; elektronik/kamera/e-stop hacim zarfları | M1 | Yük tablosu, kütle bütçesi, dondurulmuş arayüz zarfı | Konti analizi bağımsız tekrarladı; tork marjı onaylı |
| A1 | Avi | Güç bütçesi, motor, sürücü, enkoder/limit, 220 VAC→DC dağıtım | M2 | BOM, güç bütçesi, seçim gerekçesi | Tork-hız eğrisi M2 yüküyle örtüşüyor; güç marjı var |
| A2 | Avi | Kontrol mimarisi, e-stop zinciri, tetik devresi, donanımsal yasak alan limiti, haberleşme, kamera spec, blok şema | A1 | Blok şema, ICD v1, kablaj planı, kamera spec | E-stop FMEA; tüm arayüzler tanımlı; Meka ve Kodi imzaladı |
| M3 | Meka | Detay tasarım, kablo yolu, kamera/elektronik montajı, imalat yöntemi, teknik resimler | A2 | İmalat dosyaları, montaj sırası | ≤60 cm, keskin kenar yok, e-stop erişilebilir; tasarım incelemesi |
| Y1 | Kodi | Algılama: balon, hedef, kırmızı/mavi, sınıflandırma, mesafe tahmini | A2 (kamera spec) | Model, 5/10/15 m doğruluk raporu | Test seti ve metrik Konti'nin; eşikler geçildi |
| Y3 | Kodi | Arayüz: GUI/joystick/klavye, mod geçişi, e-stop durumu, yasak alan tanımı | A2 (ICD) | Arayüz yazılımı, mesaj protokolü | Yetenek-1 maddeleri karşılanıyor |
| Y2 | Kodi | Takip ve atış kontrol: yönlenme, angajman, imha değerlendirme, yasak alan | Y1, M2, A2 | Kontrol yazılımı (önce simülasyon) | Gecikme zinciri analizi; yasak alan ihlali sıfır |
| Y4 | Kodi | Aşama-1/2/3 durum makineleri ve puan mantığı | Y2, Y3 | Senaryo yazılımı | Her aşama kuralı REQ'e eşlendi |
| M4 | Meka | İmalat, montaj, ölçüm | M3 | Fiziksel sistem, ölçüm raporu | Boyut ve kütle ölçüldü, R01 sağlandı |
| T1 | Konti | Alt sistem testleri | M4, Y1–Y4 | Test raporları | Kabul kriterleri geçildi |
| T2 | Konti | Entegrasyon testi | T1 | Entegrasyon raporu | Uçtan uca zincir çalışıyor |
| T3 | Konti | Video yetenek provası (1–7) | T2 | Prova kaydı | 7 yetenek sırayla tamam |
| T4 | Konti | Aşama provaları, puan simülasyonu, 30 dk hazırlık ve 10 dk bakım planı | T3 | Prova ve strateji raporu | Baraj puanları aşıldı |
