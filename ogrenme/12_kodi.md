# Öğrenme Rehberi – Kodi (Görüntü İşleme ve Yazılım)

Departman lideri: **Eren Aras**

**Amaç:** Y1–Y4 işlerine başlamadan önce bu yarışmaya özgü bilgi boşluklarını (kamera geometrisi, takip, gecikme, güvenli
kontrol) kapatmak. Ekip deneyimli olduğu için liste "dil öğrenme" değildir.

> **Önemli:** Algoritma eşikleri kamera ve ICD (A2) ONAYLI olmadan dondurulmaz. Öğrenme, veri toplama ve prototip beklemeden başlayabilir.
> Araçlar hızla güncellenir; resmi dokümantasyonun en güncel sürümünü kullan.

## 1. Öğrenme listesi
Öncelik: **A** = hazırlık hattında hemen · **B** = A2'den önce/sonra · **C** = entegrasyon sırasında

| # | Konu | Öncelik | Neden (İP) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 1 | OpenCV: yakalama, HSV, eşikleme, morfoloji, kontur | A | Y1: balon ve renk tespiti | Kırmızı/mavi balonu canlı görüntüde bulur, ışık değişiminde test edersin | [ ] |
| 2 | Işık ve renk dayanıklılığı: beyaz dengesi, pozlama, HSV kalibrasyonu | A | Y1: R10 | Farklı ışıkta yanlış pozitif/negatif oranını ölçersin | [ ] |
| 3 | Kamera geometrisi: pinhole, odak uzaklığı, FOV, kalibrasyon, bozulma | A | Y1: mesafe tahmini | Bilinen balon çapından 5/10/15 m mesafe tahmin edip gerçekle karşılaştırırsın | [ ] |
| 4 | Mesafe tahmini: bilinen boyut, çift kamera, derinlik sensörü; hata analizi | A | Y1: R10 menzil | Piksel hatasının metre hatasına etkisini formülle çıkarırsın | [ ] |
| 5 | Nesne tespiti ve sınıflandırma: YOLO ailesi, transfer öğrenme | A | Y1: yetenek 6, Aşama-3 | Küçük veri setiyle model eğitir, hata matrisi çıkarırsın | [ ] |
| 6 | Veri seti: etiketleme, artırma, train/val/test ayrımı, sızıntı | A | Y1 | 3B baskı maketlerle farklı ışık/arka planda veri seti oluşturursun | [ ] |
| 7 | Uç cihazda çıkarım: RPi/Jetson, niceleme, TensorRT/ONNX | B | Y1/Y2: FPS | Hedef donanımda FPS ve gecikmeyi ölçersin | [ ] |
| 8 | Takip: Kalman, SORT ailesi, çoklu hedef eşleştirme | B | Y2: hareketli hedef | Hareketli hedefi filtreleyip bir sonraki konumunu tahmin edersin | [ ] |
| 9 | Öne nişan (lead) ve atış modeli: hedef hızı, gecikme, atış süresi | B | Y2: isabet | Hedef hızı ve gecikmeden önüne nişan açısını hesaplarsın | [ ] |
| 10 | Kontrol: PID, konum/hız döngüsü, gecikmeli sistemde kararlılık | B | Y2 (Avi ile) | Bir ekseni gecikmeli simülasyonda kararlı takip ettirirsin | [ ] |
| 11 | Gecikme zinciri: yakalama → işleme → karar → haberleşme → motor → mekanik | B | Y2, T1 | Uçtan uca gecikme bütçesi tablosu çıkarırsın | [ ] |
| 12 | Durum makineleri ve senaryo mantığı (Aşama-1/2/3) | B | Y4: R08–R10 | Aşama-3 dost/düşman karar akışını durum makinesi olarak çizersin | [ ] |
| 13 | Güvenli yazılım: yasak alan doğrulama, watchdog, güvenli duruş | A | Y2/Y3: R03 | "Yazılım çökerse ne olur?" için güvenli duruş senaryosu yazarsın | [ ] |
| 14 | Kullanıcı arayüzü: canlı video, durum, mod geçişi, e-stop durumu, yasak alan, joystick/klavye | A | Y3: yetenek 1 | Yetenek-1 maddelerini karşılayan arayüz taslağı (önce sahte veriyle) | [ ] |
| 15 | Haberleşme: TCP/UDP, seri, zaman damgası, kayıp, yeniden bağlanma | B | Y3/ICD | Mesaj formatı ve hata durumunu tanımlayıp test edersin | [ ] |
| 16 | Yazılım mimarisi: modüler yapı, ROS 2 (opsiyonel), logging, simülasyon | B | Y2/Y4 | Algılama, takip, kontrol modüllerini ayrı çalıştırıp test edersin | [ ] |
| 17 | Test ve doğrulama: metrikler (doğruluk, kesinlik, geri çağırma, FPS, gecikme), regresyon | B | T1 (Konti ile) | Eşiklerin geçip geçmediğini sayılarla gösterirsin | [ ] |
| 18 | Davranış diyagramları: use case, durum, aktivite, sekans (UML/SysML) | C | KTR §4.4 | KTR için 4 diyagram çizersin | [ ] |

## 2. 3 haftalık plan
- **Hafta 1:** konu 1, 2, 3; USB kamerayla balon tespiti prototipi
- **Hafta 2:** konu 4, 5, 6; veri seti toplamaya başla (3B baskı maketler)
- **Hafta 3:** konu 13, 14 (GUI iskeleti sahte veriyle); konu 12 için durum makinesi taslağı

**Öğrenme kanıtı:** Çalışan prototip + ölçüm tablosu (doğruluk, FPS, gecikme) → `ogrenme/kanitlar/kodi/`.

## 3. Kaynaklar
**Kitaplar:** Szeliski, *Computer Vision: Algorithms and Applications* (çevrimiçi) · Hartley & Zisserman, *Multiple View Geometry* ·
Bradski & Kaehler, *Learning OpenCV* · Goodfellow, Bengio & Courville, *Deep Learning* (çevrimiçi) ·
Roger Labbe, *Kalman and Bayesian Filters in Python* (GitHub, ücretsiz) · Ogata / Franklin-Powell · Martin, *Clean Architecture* (isteğe bağlı)

**Ders:** Stanford CS231n · fast.ai *Practical Deep Learning for Coders* · docs.opencv.org · docs.ultralytics.com ·
PyTorch / ONNX Runtime / TensorRT belgeleri · Raspberry Pi ve NVIDIA Jetson dokümantasyonu · docs.ros.org ·
Zhang, "A Flexible New Technique for Camera Calibration" (2000)

**Araçlar:** Python (OpenCV, numpy, PyTorch), Label Studio / CVAT / Roboflow, Git, Qt/PyQt veya web GUI, ROS 2 (ops.),
Gazebo/Webots/Python simülatörü

**Yarışma:** Şartname §5–§6, §2.4.4 · KTR şablonu §4.2.2, §4.3, §4.4 · teknofest.org raporları · Soru&Cevap grubu

## 4. Ajanla çalışma
- Kodi'yi tasarım gözden geçirme, hata avı ve dokümantasyon için kullan; kod yazdırırsan çıktıyı mutlaka çalıştırıp ölç.
- Eşik ve doğruluk sayılarını Kodi'ye uydurtma; ölçtüğün değeri ver, Kodi tabloya dönüştürsün.
- Veri setini ve test setini Konti ile birlikte ayır; modelin eğitildiği veriyle test etme.
