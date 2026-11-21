# Öğrenme Rehberi – Avi (Aviyonik) · v2

Departman lideri: **Sıla Doğan** · Kaynak: Drive "11 Öğrenme Rehberi – Avi (v2)"

**v2'de ne değişti:** ÖTR'ye göre yeni öncelik (**Ö**) eklendi. ÖTR "kablo bazlı" blok şema istediği için kablolama (14) öne alındı;
yeni konular: 19 (kablo bazlı blok şema çizimi), 20 (tedarik araştırması). Plan ÖTR'ye göre yeniden yazıldı.

**Amaç:** Ö2 (ÖTR donanım ön seçimi) ve A1–A2 işlerinden önce neyi bilmen gerektiğini göstermek. Her konunun sonunda küçük bir
hesap, şema ya da devre denemesi yapabiliyor olmalısın.

## 0. ÖTR'de senden istenen (Ö2)
Avi ÖTR'de **25 puan** taşır: Blok şema 5 + Donanım 20; yaklaşık **1,9 sayfa**.
- **Kablo bazlı blok şema:** tüm alt birimler; bağlantı tipi (USB 3, CAN, RS485, PWM, GPIO, 24 VDC, 220 VAC) ve kablo tipi (ekranlı/ekransız, kesit, konnektör). Güç, sinyal ve e-stop hatları ayırt edilmeli.
- **Donanım tablosu:** enkoder, motor, sürücü, kamera, işlemciler, güç kaynağı/kartı, e-stop ve güç kesme elemanı. Üretici, model, özellik, fiyat; ne için gerekli ve hangi gereksinime dikkat edildi.
- **Kendi tasarladığınız kart** varsa (örn. güç dağıtım kartı): şema ya da çizim görseli.
- **Ön hesap:** Meka'nın kütle v0 tahmininden tork ve güç; marj eklenmiş.

Bu seçimler **ÖN SEÇİM**'dir; KTR'de M2 onaylandıktan sonra A1–A2 kapılarından geçerek kesinleşir.
KTR hattında Avi, M2 ONAYLI olmadan seçim kesinleştirmez; ÖTR hattında Ö1'in ÖN SEÇİM'i yeterlidir.

## 1. Öğrenme listesi
Öncelik: **Ö** = Ö2'den önce · **A** = A1'den önce · **B** = A2 bitmeden önce · **C** = montaj ve test sırasında

| # | Konu | Öncelik | Neden (İP) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 1 | Motor tipleri: fırçalı DC, BLDC, step, servo; tork-hız eğrisi | **Ö** | Ö2/A1: motor seçimi | Katalog eğrisinden çalışma noktasını ve tork marjını okursun | [ ] |
| 2 | Mekanikten motora tork zinciri: yük torku, redüktör oranı/verimi, atalet uyumu | **Ö** | Ö2: tork ön hesabı; A1 | Pitch yükünden motor torkunu elle hesaplarsın (Meka ile aynı sayıya ulaşırsınız) | [ ] |
| 3 | Motor sürücüleri: H-köprüsü, ESC/FOC, step sürücü, akım limiti | **Ö** | Ö2/A1: sürücü seçimi | Sürücü datasheet'inden akım, gerilim, haberleşme arayüzünü okursun | [ ] |
| 4 | Enkoder ve konum geri bildirimi: artımlı/mutlak, çözünürlük, limit anahtarı, homing | **Ö** | Ö2: enkoder satırı; R04 | Gereken açısal çözünürlüğü hesaplayıp enkoder seçersin | [ ] |
| 5 | Güç dağıtımı: 220 VAC→DC (SMPS), regülatör, sigorta, ters bağlantı ve aşırı akım koruması | **Ö** | Ö2: güç kartı, güç hattı; R11 | Pik ve sürekli güç bütçesi tablosu çıkarır, marj eklersin | [ ] |
| 6 | Hata-güvenli acil durdurma: NC kontak, güç kesme rölesi/kontaktör, kablo kopması | **Ö** | Ö2: e-stop zinciri; A2: R02 | E-stop devresini çizer, "kablo koparsa ne olur?" sorusunu cevaplarsın | [ ] |
| 7 | Donanımsal limit ve yasak alan: limit anahtarıyla güç kesme | A | A2: R03 | Yazılım çökse bile yasak bölgeye dönülemeyeceğini devreyle gösterirsin | [ ] |
| 8 | Kontrolcü seçimi: MCU (STM32/Arduino/ESP32) ↔ gömülü bilgisayar (RPi/Jetson) | **Ö** | Ö2: işlemci satırları; A2: mimari | Gerçek zamanlı iş ile ağır iş (görüntü) ayrımını gerekçelendirirsin | [ ] |
| 9 | Haberleşme: UART, SPI, I2C, CAN, RS422/485, Ethernet, USB; gecikme ve kayıp | **Ö** | Ö2: bağlantı tipleri; A2: ICD | Mesaj formatı ve hız tanımlayıp bant genişliği/gecikme hesaplarsın | [ ] |
| 10 | Kontrol: PID, konum/hız döngüsü, doyma, anti-windup, ayrık zaman | B | A2/Y2 arayüzü | Bir eksenin PID döngüsünü simülasyonda ayarlarsın | [ ] |
| 11 | Sensör ve sinyal koşullama: ADC, filtre, gürültü | B | A2 | Gürültülü sinyale uygun filtre seçersin | [ ] |
| 12 | Atış tetik elektroniği: solenoid/röle/MOSFET, flyback diyot, güvenli devre dışı | B | A2: tetik devresi | Solenoid sürme devresini çizer ve korumasını açıklarsın | [ ] |
| 13 | EMI/EMC: topraklama, ekranlama, güç/sinyal ayrımı, filtre, ferrit | B | A2/M3: R11 | Güç ve sinyal kablolarını ayrı yönlendiren yerleşim planı çizersin | [ ] |
| 14 | Kablolama ve izolasyon: AWG, akım taşıma, ekranlı kablo, konnektör, makaron | **Ö** | Ö2: kablo tipleri; M3/M4: R12 | Akıma göre kesit seçer, kablo listesi (harness) yazarsın | [ ] |
| 15 | Şematik ve PCB (KiCad/Altium), lehim, test noktaları | Ö / C | Kendi kart varsa Ö (Ö2 görseli), yoksa C | Basit bir güç dağıtım kartını şematik ve PCB olarak çizersin | [ ] |
| 16 | Kamera donanımı: çözünürlük, FOV, kare hızı, shutter, arayüz, lens, piksel boyutu | **Ö** | Ö2: kamera satırı (Kodi ile) | 15 m'de belirli çaptaki balonun kaç piksel olacağını hesaplarsın | [ ] |
| 17 | Güvenlik tasarım ilkeleri: risk değerlendirmesi, FMEA, arıza modları | B | A2: KTR §6 | Bir alt sistem için FMEA tablosu doldurursun (Konti doğrular) | [ ] |
| 18 | Test ekipmanı: multimetre, osiloskop, güç kaynağı, mantık analizörü; güvenli enerji verme | C | M4/T1: Şart. 4.2 | "Enerji vermeden önce" kontrol listesi yazarsın | [ ] |
| 19 | **Yeni:** Kablo bazlı blok şema çizimi: sembol seti, çizgi türleriyle güç/sinyal/e-stop ayrımı, her bağlantıya tip ve kablo etiketi | **Ö** | Ö2: ÖTR §3.1; A2 | Tüm sistemi 0,6 sayfaya sığan, her çizgisi etiketli bir şema olarak çizersin | [ ] |
| 20 | **Yeni:** Tedarik araştırması: datasheet, fiyat, stok, teslim süresi, alternatif parça; ithalatta gümrük ve kargo süresi | **Ö** | Ö2: donanım tablosu; Sis'in malzeme listesi | Her ana parça için iki alternatifi fiyat ve teslim süresiyle tabloya koyarsın | [ ] |

## 2. 3 haftalık plan (Ö2 hazırlığı)
- **Hafta 1:** konu 1, 2, 5, 19 (motor, tork zinciri, güç, blok şema çizim dili); Meka'nın kütle v0'ı geldiyse ilk tork tahmini.
- **Hafta 2:** konu 3, 4, 6, 14 (sürücü, enkoder, e-stop, kablo); **e-stop zinciri ve güç hattı** blok şemaya işlenir.
- **Hafta 3:** konu 8, 9, 16, 20 (işlemciler, haberleşme, kamera, tedarik); Kodi ile kamera ve işlemci ön seçimi;
  **Ö2 Teslim Notu taslağı**: donanım tablosu + blok şema v0 + ön hesaplar.

Ö2 bitince KTR için: konu 7, 10–13, 17 (A1–A2), ardından C grubu. Tarihler: A1 v0 31.01, blok şema 14.02.
**Öğrenme kanıtı:** Her konu için 1 sayfalık çözülmüş örnek ve e-stop devre şeması → Drive (04_Elektronik).

## 3. Kaynaklar
**Kitaplar:** Horowitz & Hill, *The Art of Electronics* · Erickson & Maksimovic, *Fundamentals of Power Electronics* ·
Ogata, *Modern Control Engineering* / Franklin, Powell & Emami-Naeini, *Feedback Control of Dynamic Systems* ·
Ott, *Electromagnetic Compatibility Engineering* · Williams, *Making Embedded Systems* · Hughes, *Electric Motors and Drives* ·
Boylestad / Sedra-Smith devre kitapları

**Ders:** MIT OCW 6.002 · TI motor sürme eğitimleri ve uygulama notları · ST motor kontrol notları · ADI/TI EMC uygulama notları ·
KiCad dokümantasyonu · **draw.io (diagrams.net) dokümantasyonu** (katman ve çizgi stili) · YouTube osiloskop, PCB, BLDC/FOC

**Üretici (Ö2 için birincil):** motor, sürücü, enkoder, güç kaynağı, röle/kontaktör, e-stop, kamera datasheet ve uygulama notları ·
Digi-Key, Mouser, yerel tedarikçiler (fiyat ve teslim süresi; kaynak ve tarih) · kablo ve konnektör akım taşıma tabloları

**Standartlar:** ISO 13850 · IEC 60204-1 · ISO 13849-1 · IEC 61000 (özet). Amaç hata-güvenli bakış açısı.

**Yarışma:** ÖTR şablonu §3.1, §3.3 · Şartname §4.1, §4.2, §4.3, §6 · KTR şablonu §4.2.1, §4.3, §6 · teknofest.org raporları · Soru&Cevap (Sis tutar)

**Araçlar:** draw.io, KiCad, LTspice, Python/numpy, osiloskop ve güç kaynağı, STM32CubeIDE / Arduino IDE

## 4. Ajanla çalışma
- Önce kavramı öğren, sonra **kendi hesabını/devreni** yap; Avi'ye "kontrol et, hatamı bul" de.
- Güvenlik devrelerinde (e-stop, limit) Avi'ye **yalnızca inceleme** yaptır; son karar lider ve Konti'nin FMEA doğrulaması.
- Blok şemanı ve donanım tablonu Sis'e ver; Sis, Kodi'nin yazılım arayüz şeması ve Meka'nın tablosuyla karşılaştırır.
- Fiyat ve stok bilgisini her zaman tedarikçiden doğrula.
