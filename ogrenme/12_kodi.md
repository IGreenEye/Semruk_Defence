# Öğrenme Rehberi – Kodi (Görüntü İşleme ve Yazılım) · v2

Departman lideri: **Eren Aras** · Kaynak: Drive "12 Öğrenme Rehberi – Kodi (v2)"

**v2'de ne değişti:** ÖTR'nin en yüksek puanlı bölümü (Yöntem, 25) diyagram istediği için UML/SysML diyagramları (18) **en başa**
alındı. Durum makinesi (12), arayüz (14), haberleşme (15), mimari (16) ÖTR önceliğine çıktı. Yeni konu: 19 (yazılım bileşen
envanteri). Plan ekibi ikiye bölerek yeniden yazıldı.

**Amaç:** Ö3–Ö4 (ÖTR yazılım ve yöntem) ile Y1–Y4 işlerinden önce bu yarışmaya özgü boşlukları kapatmak. Ekip deneyimli;
liste "dil öğrenme" değildir. Araçlar hızla güncellenir; resmi dokümantasyonun en güncel sürümünü kullan.

## 0. ÖTR'de senden istenen (Ö3 + Ö4)
Kodi ÖTR'nin **45 puanını** taşır: Yazılım 20 + Yöntem 25; yaklaşık **3 sayfa** (raporun en büyük payı).
- **Yazılım bileşen tablosu (§3.4):** atış kontrol, görüntü işleme (tespit/takip), kullanıcı arayüzü, motor kontrol, haberleşme. Hazırlarda üretici ve sürüm; her bileşenin özellikleri ve temel gereksinimleri. **Kod paylaşılmaz.**
- **Yazılım arayüz şeması:** modüller ve mesajlar; Avi'nin kablo bazlı blok şemasıyla tutarlı.
- **Yöntem (§4):** Aşama-1, 2, 3 için **ayrı ayrı** aktivite ve sekans diyagramı; açılış ve mod/aşama seçimi için durum makinesi (isteğe bağlı ama önerilir).
- Diyagramlar şartname kurallarını göstermeli: zarf sırası ve yanlış sıra cezası, tur yapısı, dost-düşman, menzil koşulu, e-stop ve yasak alan, 0°/0° başlangıç.

**İyi haber:** Ö4 yalnızca şartnameye ve T0'a bağlı; donanımı beklemeden hemen başlar (durum makinesi taslağı 27.12,
aşama diyagramları H10–H12, bölüm teslimi 14.02).
**Önemli:** Algoritma **eşikleri** kamera ve ICD (A2) ONAYLI olmadan dondurulmaz. Öğrenme, veri toplama ve prototip serbest.

## 1. Öğrenme listesi
Öncelik: **Ö** = Ö3/Ö4'ten önce · **A** = hazırlık hattında hemen · **B** = A2'den önce/sonra · **C** = entegrasyon.
Numaralar v1 ile aynı; sıra öncelik değişikliğini gösterir.

| # | Konu | Öncelik | Neden (İP) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 18 | **İlk sırada – Davranış diyagramları:** aktivite, sekans, durum makinesi, use case (UML/SysML) | **Ö** | Ö4: Yöntem (25); KTR §4.4 | Aşama-1 için aktivite ve sekans diyagramını şartname kurallarıyla eksiksiz çizersin | [ ] |
| 12 | Durum makineleri ve senaryo mantığı (Aşama-1/2/3); zamanlama, zarf sırası, ceza | **Ö** | Ö4: durum makinesi; Y4: R08–R10 | Aşama-3 dost/düşman karar akışını durum makinesi olarak çizersin | [ ] |
| 16 | Yazılım mimarisi: modüler yapı, ROS 2 (isteğe bağlı), logging, simülasyonla test | **Ö** | Ö3: arayüz şeması; Y2/Y4 | Algılama, takip, kontrol modüllerini kutular ve mesajlarla çizersin | [ ] |
| 15 | Haberleşme ve mesaj protokolü: TCP/UDP, seri, zaman damgası, kayıp, yeniden bağlanma | **Ö** | Ö3: arayüz şeması; Y3/ICD | Mesaj formatı ve hata durumunu tanımlarsın | [ ] |
| 14 | Kullanıcı arayüzü: canlı video, durum, mod geçişi, e-stop durumu, yasak alan, joystick/klavye | **Ö** | Ö3: arayüz bileşeni; Y3: yetenek 1 | Yetenek-1 maddelerini karşılayan ekran taslağı (önce sahte veriyle) | [ ] |
| 19 | **Yeni:** Yazılım bileşen envanteri: hazır kütüphanelerin üreticisi, sürümü, lisansı; sürüm sabitleme | **Ö** | Ö3: ÖTR yazılım tablosu | Tabloyu kurulu ortamdan sürümleri okuyarak doldurursun | [ ] |
| 13 | Güvenli yazılım: yasak alan doğrulama, watchdog, güvenli duruş | **Ö** | Ö4: güvenlik dalları; Y2/Y3: R03 | "Yazılım çökerse ne olur?" için güvenli duruş senaryosu yazarsın | [ ] |
| 1 | OpenCV: yakalama, HSV, eşikleme, morfoloji, kontur | A | Y1: balon ve renk tespiti | Kırmızı/mavi balonu canlı görüntüde bulursun | [ ] |
| 2 | Işık ve renk dayanıklılığı: beyaz dengesi, pozlama, HSV kalibrasyonu | A | Y1: R10 | Farklı ışıkta yanlış pozitif/negatif oranını ölçersin | [ ] |
| 3 | Kamera geometrisi: pinhole, odak uzaklığı, FOV, kalibrasyon | A | Y1: mesafe; Ö2 kamera seçimine girdi (Avi ile) | Bilinen balon çapından 5/10/15 m mesafe tahmin edip gerçekle karşılaştırırsın | [ ] |
| 4 | Mesafe tahmini: bilinen boyut, çift kamera, derinlik sensörü; hata analizi | A | Y1: R10 menzil | Piksel hatasının metre hatasına etkisini formülle çıkarırsın | [ ] |
| 5 | Nesne tespiti ve sınıflandırma: YOLO ailesi, transfer öğrenme | A | Y1: yetenek 6, Aşama-3 | Küçük veri setiyle model eğitir, hata matrisi çıkarırsın | [ ] |
| 6 | Veri seti: etiketleme, artırma, train/val/test, sızıntı | A | Y1 | 3B baskı maketlerle farklı ışık/arka planda veri seti oluşturursun | [ ] |
| 7 | Uç cihazda çıkarım: RPi/Jetson, niceleme, TensorRT/ONNX | B | Y1/Y2: FPS; Ö2 işlemci seçimine girdi | Hedef donanımda FPS ve gecikmeyi ölçersin | [ ] |
| 8 | Takip: Kalman, SORT ailesi, çoklu hedef eşleştirme | B | Y2: hareketli hedef | Hareketli hedefin bir sonraki konumunu tahmin edersin | [ ] |
| 9 | Öne nişan ve atış modeli: hedef hızı, gecikme, uçuş süresi | B | Y2: isabet | Hedef hızı ve gecikmeden öne nişan açısını hesaplarsın | [ ] |
| 10 | Kontrol: PID, konum/hız döngüsü, gecikmeli sistemde kararlılık | B | Y2 (Avi ile) | Bir ekseni gecikmeli simülasyonda kararlı takip ettirirsin | [ ] |
| 11 | Gecikme zinciri: yakalama → işleme → karar → haberleşme → motor → mekanik | B | Y2, T1 | Uçtan uca gecikme bütçesi tablosu çıkarırsın | [ ] |
| 17 | Test ve doğrulama: metrikler (doğruluk, kesinlik, geri çağırma, FPS, gecikme), regresyon | B | T1 (Konti ile) | Eşiklerin geçip geçmediğini sayılarla gösterirsin | [ ] |

## 2. 3 haftalık plan: ekibi ikiye böl (Kodi ekibi 4 kişi)
**Grup Ö (2 kişi, ÖTR):**
- **Hafta 1:** konu 18 ve 12; Aşama-1 aktivite ve sekans taslağı; mod durum makinesi taslağı.
- **Hafta 2:** konu 13, 16, 15; Aşama-2 ve Aşama-3 diyagramları; yazılım arayüz şeması v0.
- **Hafta 3:** konu 14 ve 19; ekran taslağı, yazılım bileşen tablosu; **Ö3 ve Ö4 Teslim Notu taslağı**.

**Grup P (2 kişi, prototip):**
- **Hafta 1–3:** konu 1–6; USB kamerayla balon tespiti prototipi, veri seti toplamaya başlama. Ölçülen FPS ve kamera deneyimi
  Avi'nin Ö2 kamera ve işlemci seçimine girdi olur. (ÖTR öncesi parça alımı yok; eldeki USB kamera ve dizüstüyle.)

> **Dikkat – kapsam kuralı (Proje Planı v3, 21.11.2026):** ÖTR döneminde kod geliştirme, test ve ölçüm yapılmaz. Grup P'nin
> prototip planı bu kuralla çelişiyor; 29.11 toplantısında kaptan karar verene kadar Grup P de konu 1–6'yı yalnızca
> **kavram ve hesap** düzeyinde çalışır (ör. 15 m'de balonun piksel boyutu, mesafe hatası formülü) ve Ö3'e girdi verir.

**Öğrenme kanıtı:** 7 diyagram, yazılım tablosu, çalışan prototip ve ölçüm tablosu → Drive (05_Yazılım; kod Git'te).
ÖTR'de Yazılım ve Yöntem, KTR'de Yazılım ve Test bölümlerine malzeme olur.

## 3. Kaynaklar
**Diyagramlar (ÖTR için öncelikli):** Martin Fowler, *UML Distilled* · OMG UML Specification · Friedenthal, Moore & Steiner,
*A Practical Guide to SysML* · **PlantUML** dokümantasyonu (metinden diyagram; Git ile sürümlenir) · draw.io dokümantasyonu

**Görüntü işleme ve yapay zekâ:** Szeliski, *Computer Vision* (çevrimiçi) · Hartley & Zisserman, *Multiple View Geometry* ·
Bradski & Kaehler, *Learning OpenCV* · Goodfellow, Bengio & Courville, *Deep Learning* · Roger Labbe, *Kalman and Bayesian
Filters in Python* · Zhang (2000) kalibrasyon makalesi · Stanford CS231n · fast.ai

**Resmi dokümantasyon (tablodaki sürüm kaynağı):** OpenCV, Ultralytics, PyTorch, ONNX Runtime, TensorRT, Qt/PyQt, ROS 2 ·
Raspberry Pi ve NVIDIA Jetson

**Diğer:** Ogata / Franklin-Powell · Martin, *Clean Architecture* (isteğe bağlı)

**Yarışma:** ÖTR şablonu §3.4, §4 · Şartname §5–§6, §2.4.4.1 · KTR şablonu §4.2.2, §4.3, §4.4 · teknofest.org raporları · Soru&Cevap (Sis tutar)

**Araçlar:** Python (OpenCV, numpy, PyTorch), PlantUML ve draw.io, Label Studio / CVAT / Roboflow, Git, Qt/PyQt veya web GUI,
ROS 2 (isteğe bağlı), Gazebo/Webots/Python simülatörü

## 4. Ajanla çalışma
- Kodi'yi **diyagram gözden geçirme**, tasarım incelemesi, hata avı ve dokümantasyon için kullan; kod yazdırırsan çalıştırıp ölç.
- Diyagram taslağını verip "şartnamedeki şu kuralı diyagram gösteriyor mu?" diye sor; eksik dalları listelesin.
- Eşik ve doğruluk sayılarını **uydurtma**; ölçtüğün değeri ver, Kodi tabloya dönüştürsün.
- Yazılım tablosunu ve arayüz şemasını Sis'e ver; Sis, Avi'nin blok şemasıyla karşılaştırır.
- Veri setini ve test setini **Konti ile** ayır; modelin eğitildiği veriyle test etme.
