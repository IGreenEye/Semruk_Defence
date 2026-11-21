# Öğrenme Rehberi – Avi (Aviyonik)

Departman lideri: **Sıla Doğan**

**Amaç:** A1–A2 işlerine başlamadan önce neyi bilmen gerektiğini ve nereden öğreneceğini göstermek. Her konunun sonunda
küçük bir hesap, şema ya da devre denemesi yapabiliyor olmalısın.

> **Önemli:** Avi'nin işleri M2 (kütle, atalet, tork) ONAYLI olmadan seçim üretmez. Bu öğrenme ise M2'yi beklemeden başlayabilir.

## 1. Öğrenme listesi
Öncelik: **A** = A1'e başlamadan önce · **B** = A2 bitmeden önce · **C** = montaj ve test sırasında

| # | Konu | Öncelik | Neden (İP) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 1 | Motor tipleri: fırçalı DC, BLDC, step, servo; tork-hız eğrisi | A | A1: motor seçimi | Katalog eğrisinden çalışma noktasını ve tork marjını okursun | [ ] |
| 2 | Mekanikten motora tork zinciri: yük torku, redüktör oranı/verimi, atalet uyumu | A | A1: M2 yükünden motor torkuna | Pitch yükünden motor torkunu elle hesaplarsın (Meka ile aynı sayıya ulaşırsınız) | [ ] |
| 3 | Motor sürücüleri: H-köprüsü, ESC/FOC, step sürücü, akım limiti | A | A1: sürücü seçimi | Sürücü datasheet'inden akım, gerilim, haberleşme arayüzünü okursun | [ ] |
| 4 | Enkoder ve konum geri bildirimi: artımlı/mutlak, çözünürlük, limit anahtarı, homing | A | A1/A2: açı ölçümü, R04 | Gereken açısal çözünürlüğü hesaplayıp enkoder seçersin | [ ] |
| 5 | Güç dağıtımı: 220 VAC→DC (SMPS), regülatör, sigorta, ters bağlantı ve aşırı akım koruması | A | A1: güç bütçesi, R11 | Pik ve sürekli güç bütçesi tablosu çıkarır, marj eklersin | [ ] |
| 6 | Hata-güvenli acil durdurma: NC kontak, güç kesme rölesi/kontaktör, kablo kopması | A | A2: R02 | E-stop devresini çizer, "kablo koparsa ne olur?" sorusunu cevaplarsın | [ ] |
| 7 | Donanımsal limit ve yasak alan: limit anahtarıyla güç kesme | A | A2: R03 | Yazılım çökse bile yasak bölgeye dönülemeyeceğini devreyle gösterirsin | [ ] |
| 8 | Kontrolcü seçimi: MCU (STM32/Arduino/ESP32) ↔ gömülü bilgisayar (RPi/Jetson) | B | A2: mimari | Gerçek zamanlı iş (motor) ile ağır iş (görüntü) ayrımını gerekçelendirirsin | [ ] |
| 9 | Haberleşme: UART, SPI, I2C, CAN, RS422/485, Ethernet; gecikme ve kayıp | B | A2: ICD | Mesaj formatı ve hız tanımlayıp bant genişliği/gecikme hesaplarsın | [ ] |
| 10 | Kontrol: PID, konum/hız döngüsü, doyma, anti-windup, ayrık zaman | B | A2/Y2 arayüzü | Bir eksenin PID döngüsünü simülasyonda ayarlarsın | [ ] |
| 11 | Sensör ve sinyal koşullama: ADC, filtre, gürültü | B | A2 | Gürültülü sinyale uygun filtre seçersin | [ ] |
| 12 | Atış tetik elektroniği: solenoid/röle/MOSFET, flyback diyot, güvenli devre dışı | B | A2: tetik devresi | Solenoid sürme devresini çizer ve korumasını açıklarsın | [ ] |
| 13 | EMI/EMC: topraklama, ekranlama, güç/sinyal ayrımı, filtre, ferrit | B | A2/M3: R11 | Güç ve sinyal kablolarını ayrı yönlendiren yerleşim planı çizersin | [ ] |
| 14 | Kablolama ve izolasyon: AWG, akım taşıma, konnektör, makaron | C | M3/M4: R12 | Akıma göre kesit seçer, kablo listesi (harness) yazarsın | [ ] |
| 15 | Şematik ve PCB (KiCad/Altium), lehim, test noktaları | C | A2/M4 | Basit bir sürücü kartını şematik ve PCB olarak çizersin | [ ] |
| 16 | Kamera donanımı: çözünürlük, FOV, kare hızı, shutter, arayüz, lens, piksel boyutu | B | A2: kamera spec (Kodi ile) | 15 m'de belirli çaptaki balonun kaç piksel olacağını hesaplarsın | [ ] |
| 17 | Güvenlik tasarım ilkeleri: risk değerlendirmesi, FMEA, arıza modları | B | A2: KTR §6 | Bir alt sistem için FMEA tablosu doldurursun | [ ] |
| 18 | Test ekipmanı: multimetre, osiloskop, güç kaynağı, mantık analizörü; güvenli enerji verme | C | M4/T1: Şart. 4.2 | "Enerji vermeden önce" kontrol listesi yazarsın | [ ] |

## 2. 3 haftalık plan
- **Hafta 1:** konu 1, 2, 5; Meka'nın M1 çıktısı varsa ön tork hesabı
- **Hafta 2:** konu 6, 7, 12 ve 4; ilk e-stop devre taslağı
- **Hafta 3:** konu 8, 9, 16; Kodi ile kamera ve ICD ön görüşmesi

**Öğrenme kanıtı:** Her konu için 1 sayfalık çözülmüş örnek + e-stop devre şeması → `ogrenme/kanitlar/avi/`.

## 3. Kaynaklar
**Kitaplar:** Horowitz & Hill, *The Art of Electronics* · Erickson & Maksimovic, *Fundamentals of Power Electronics* ·
Ogata, *Modern Control Engineering* / Franklin, Powell & Emami-Naeini, *Feedback Control of Dynamic Systems* ·
Ott, *Electromagnetic Compatibility Engineering* · Williams, *Making Embedded Systems* · Hughes, *Electric Motors and Drives* ·
Boylestad / Sedra-Smith devre kitapları

**Ders:** MIT OCW 6.002 Circuits and Electronics · TI Motor Drive eğitimleri ve uygulama notları · ST motor kontrol notları ·
ADI/TI EMC uygulama notları · KiCad dokümantasyonu (docs.kicad.org) · YouTube osiloskop, PCB, BLDC/FOC anlatımları

**Üretici:** Motor, sürücü, enkoder, güç kaynağı, röle/kontaktör, e-stop datasheet'leri · Digi-Key, Mouser, yerel tedarikçiler
(fiyat ve teslim süresi tablosu; uzun teslimli parçaları erken belirle)

**Standartlar:** ISO 13850 · IEC 60204-1 · ISO 13849-1 · IEC 61000 (özet). Amaç hata-güvenli bakış açısını öğrenmek.

**Yarışma:** Şartname §4.1, §4.2, §4.3, §6 · KTR şablonu §4.2.1, §4.3, §6 · teknofest.org raporları · Soru&Cevap grubu

**Araçlar:** KiCad, LTspice, Python/numpy, osiloskop ve güç kaynağı, STM32CubeIDE / Arduino IDE

## 4. Ajanla çalışma
- Önce kavramı öğren, sonra kendi hesabını/devreni yap; Avi'ye "kontrol et, hatamı bul" de.
- Güvenlik devrelerinde (e-stop, limit) Avi yalnızca inceleme yapar; son kararı lider ve Konti'nin FMEA doğrulaması verir.
- Fiyat ve stok bilgisini her zaman tedarikçiden doğrula.
