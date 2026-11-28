# Öğrenme Rehberi – Kodi (Görüntü İşleme ve Yazılım) · v2.1

Departman lideri: **Eren Aras** · Kapsam: **yalnızca ÖTR** (Ö3 + Ö4 → ÖTR §3.4 Yazılım 20 + §4 Yöntem 25, ~3 sayfa)

**Amaç:** Ö3 ve Ö4'ü yazabilmek için bu yarışmaya özgü boşlukları kapatmak. Ekip deneyimli; liste "dil öğrenme" değildir.
**Kapsam kuralı:** ÖTR döneminde **kod geliştirme, veri seti, test ve ölçüm yapılmaz.** Yazılım tasarım düzeyinde ele alınır:
bileşen tablosu, arayüz şeması, diyagramlar, hesaplar. Konular bu yüzden kavram ve hesap düzeyinde çalışılır.

## 0. ÖTR'de senden istenen (Ö3 + Ö4)
Kodi ÖTR'nin **45 puanını** taşır (raporun en büyük payı).
- **Yazılım bileşen tablosu (§3.4):** atış kontrol, görüntü işleme (tespit/takip), kullanıcı arayüzü, motor kontrol, haberleşme. Hazırlarda üretici ve sürüm; her bileşenin özellikleri ve temel gereksinimleri. **Kod paylaşılmaz.**
- **Yazılım arayüz şeması:** modüller ve mesajlar; Avi'nin kablo bazlı blok şemasıyla tutarlı.
- **Yöntem (§4):** Aşama-1, 2, 3 için **ayrı ayrı** aktivite ve sekans diyagramı; açılış ve mod/aşama seçimi için durum makinesi.
- Diyagramlar şartname kurallarını göstermeli: zarf sırası ve yanlış sıra cezası, pas geçme kuralı, tur yapısı, dost-düşman, menzil koşulu (F16 10–15 m, helikopter/füze 5–15 m, İHA 0–15 m), e-stop ve yasak alanlar, 0°/0° başlangıç.

Takvim: durum makinesi taslağı 27.12 → yazılım tablosu ve arayüz şeması 31.01 → aşama diyagramları H10–H12 → bölüm 14.02.
Ö4 yalnızca T0'a bağlıdır, hemen başlar; Ö3, Ö2'deki kamera ve işlemci ön seçimine bağlıdır.

## 1. ÖTR için öğrenme listesi
| # | Konu | Neden | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|
| 18 | **İlk sırada – Davranış diyagramları:** aktivite, sekans, durum makinesi (UML/SysML) | Ö4: Yöntem (25) | Aşama-1 için aktivite ve sekans diyagramını şartname kurallarıyla eksiksiz çizersin | [ ] |
| 12 | Durum makineleri ve senaryo mantığı (Aşama-1/2/3); zarf sırası, ceza kuralları | Ö4: durum makinesi | Aşama-3 dost/düşman karar akışını durum makinesi olarak çizersin | [ ] |
| 16 | Yazılım mimarisi: modüler yapı, ROS 2 (isteğe bağlı), kayıt (logging) | Ö3: arayüz şeması | Algılama, takip ve kontrol modüllerini kutular ve mesajlarla çizersin | [ ] |
| 15 | Haberleşme ve mesaj protokolü: TCP/UDP, seri, zaman damgası, kayıp | Ö3: arayüz şeması | Mesaj formatı ve hata durumunu tanımlarsın | [ ] |
| 14 | Kullanıcı arayüzü: canlı video, durum, mod geçişi, e-stop durumu, yasak alan tanımı, joystick/klavye | Ö3: arayüz bileşeni | Ekran taslağını (çizim olarak) çıkarırsın | [ ] |
| 19 | Yazılım bileşen envanteri: hazır kütüphanelerin üreticisi, sürümü ve lisansı | Ö3: ÖTR yazılım tablosu | Tabloyu resmi dokümantasyondaki sürüm bilgisiyle doldurursun | [ ] |
| 13 | Güvenli yazılım: atış-yasak alan fonksiyonu, watchdog, güvenli duruş | Ö4 güvenlik dalları; Şart. §4.2 | "Yazılım çökerse ne olur?" senaryosunu diyagrama işlersin | [ ] |
| 1 | Renk uzayları (HSV) ve renk tabanlı tespit yaklaşımı | Ö3: görüntü işleme bileşeni | Kırmızı/mavi ayrımı yaklaşımını ve ışık riskini gerekçesiyle anlatırsın | [ ] |
| 3 | Kamera geometrisi: pinhole model, odak uzaklığı, FOV | Ö2 kamera seçimine girdi (Avi ile) | 15 m'de 20 cm'lik balonun piksel boyutunu hesaplarsın | [ ] |
| 4 | Mesafe tahmini yöntemleri ve hata analizi | Aşama-3 menzil koşulu (R10) | Piksel hatasının metre hatasına etkisini formülle çıkarırsın | [ ] |
| 5 | Hazır tespit/sınıflandırma modelleri (YOLO ailesi vb.) | Ö3 bileşen seçimi | 2–3 modeli doğruluk, hız ve lisans açısından literatürden karşılaştırırsın | [ ] |
| 8 | Takip yöntemleri: Kalman filtresi, SORT ailesi | Ö3 takip bileşeni, Aşama-2 | Yöntem farkını ve hareketli hedefte kullanımını diyagramla açıklarsın | [ ] |

## 2. 3 haftalık plan (Proje Planı H1–H3)
- **Hafta 1:** konu 1, 3, 4 (renk uzayları, kamera geometrisi, mesafe tahmini); konu 18'e başla.
- **Hafta 2:** konu 5, 8 (hazır modeller, takip); konu 18 ve 12 – Aşama-1 diyagram taslağı.
- **Hafta 3:** konu 13, 14, 12 (güvenli yazılım, arayüz, durum makineleri); konu 16, 15, 19. Ardından H4'te yazılım mimarisi taslağı.

**Öğrenme kanıtı:** Diyagram taslakları, hesap sayfaları ve bileşen karşılaştırmaları → Drive (05_Yazılım). Hedef: 13.12.2026.

## 3. ÖTR sonrası (şimdilik kapsam dışı)
OpenCV ile prototip · ışık ve renk kalibrasyonu ölçümü · veri seti hazırlama · uç cihazda çıkarım ve FPS ölçümü · hareketli hedefte nişan alma ·
PID ve gecikmeli kontrol · gecikme zinciri ölçümü · test ve doğrulama metrikleri. ÖTR'den sonra ayrı planla ele alınacak.

## 4. Kaynaklar
**Diyagramlar (öncelikli):** Martin Fowler, *UML Distilled* · OMG UML Specification · Friedenthal, Moore & Steiner,
*A Practical Guide to SysML* · PlantUML ve draw.io dokümantasyonu
**Görüntü işleme:** Szeliski, *Computer Vision* (çevrimiçi) · Bradski & Kaehler, *Learning OpenCV* · Roger Labbe, *Kalman and
Bayesian Filters in Python* · Stanford CS231n ders notları
**Resmi dokümantasyon (sürüm kaynağı):** OpenCV, Ultralytics, PyTorch, ONNX Runtime, Qt/PyQt, ROS 2 · Raspberry Pi, NVIDIA Jetson
**Yarışma:** ÖTR şablonu §3.4, §4 · Şartname §4.2, §5–§6 · teknofest.org raporları · Soru&Cevap (Sis tutar)
**Araçlar:** PlantUML, draw.io

## 5. Ajanla çalışma
- Kodi'yi **diyagram gözden geçirme**, tasarım incelemesi ve dokümantasyon için kullan.
- Diyagram taslağını verip "şartnamedeki şu kuralı diyagram gösteriyor mu?" diye sor; eksik dalları listelesin.
- Doğruluk ve FPS sayılarını uydurtma; ÖTR'de bunlar ölçüm değil, gerekçeli **hedef** olarak yazılır.
- Yazılım tablosunu ve arayüz şemasını Sis'e ver; Sis, Avi'nin blok şemasıyla karşılaştırır.
