# Öğrenme Rehberi – Avi (Aviyonik) · v2.1

Departman lideri: **Sıla Doğan** · Kapsam: **yalnızca ÖTR** (Ö2 → ÖTR §3.1 Blok şema 5 + §3.3 Donanım 20, ~1,9 sayfa)

**Amaç:** Ö2'yi (A1 v0 + A2 v0) yazabilmek için gereken konuları ve kaynakları göstermek. Her konunun sonunda küçük bir hesap
ya da şema yapabiliyor olmalısın.
**Kapsam kuralı:** ÖTR'ye kadar parça alımı, devre kurma, test ve ölçüm yok; seçimler veri sayfası ve hesapla.

## 0. ÖTR'de senden istenen (Ö2)
- **Kablo bazlı blok şema:** tüm alt birimler; bağlantı tipi (USB 3, CAN, RS485, PWM, GPIO, 24 VDC, 220 VAC) ve kablo tipi (ekranlı/ekransız, kesit, konnektör). Güç, sinyal ve e-stop hatları ayırt edilmeli.
- **Donanım tablosu:** enkoder, motor, sürücü, kamera, işlemciler, güç kaynağı/kartı, e-stop ve güç kesme elemanı. Üretici, model, özellik, fiyat; ne için gerekli ve hangi gereksinime dikkat edildi.
- **Kendi tasarladığınız kart** varsa (örn. güç dağıtım kartı): şema ya da çizim görseli.
- **Ön hesap:** Meka'nın kütle v0 tahmininden tork ve güç; marj eklenmiş.

Bu seçimler **ÖN SEÇİM**'dir. Takvim: A1 v0 31.01 → §3.3 07.02 → A2 v0 blok şema ve §3.1 14.02.

## 1. ÖTR için öğrenme listesi
| # | Konu | Neden (Ö2) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|
| 1 | Motor tipleri: fırçalı DC, BLDC, step, servo; tork-hız eğrisi | Motor seçimi | Katalog eğrisinden çalışma noktasını ve tork marjını okursun | [ ] |
| 2 | Mekanikten motora tork zinciri: yük torku, redüktör oranı/verimi, atalet uyumu | Tork ön hesabı | Pitch yükünden motor torkunu elle hesaplarsın (Meka ile aynı sayıya ulaşırsınız) | [ ] |
| 3 | Motor sürücüleri: H-köprüsü, ESC/FOC, step sürücü, akım limiti | Sürücü seçimi | Sürücü datasheet'inden akım, gerilim, haberleşme arayüzünü okursun | [ ] |
| 4 | Enkoder ve konum geri bildirimi: artımlı/mutlak, çözünürlük, limit anahtarı, homing | Enkoder satırı; R04 | Gereken açısal çözünürlüğü hesaplayıp enkoder seçersin | [ ] |
| 5 | Güç dağıtımı: 220 VAC→DC (SMPS), regülatör, sigorta, ters bağlantı ve aşırı akım koruması | Güç kartı, güç hattı; R11 | Pik ve sürekli güç bütçesi tablosu çıkarır, marj eklersin | [ ] |
| 6 | Hata-güvenli acil durdurma: NC kontak, güç kesme rölesi/kontaktör, kablo kopması | E-stop zinciri; R02 | E-stop zincirini blok şemada çizer, "kablo koparsa ne olur?" sorusunu cevaplarsın | [ ] |
| 7 | Donanımsal limit ve yasak alan: limit anahtarıyla güç kesme | Şart. §4.2, R03 | Yazılımdan bağımsız korumanın blok şemada nerede durduğunu gösterirsin | [ ] |
| 8 | Kontrolcü seçimi: MCU (STM32/Arduino/ESP32) ↔ gömülü bilgisayar (RPi/Jetson) | İşlemci satırları | Gerçek zamanlı iş ile ağır iş (görüntü) ayrımını gerekçelendirirsin | [ ] |
| 9 | Haberleşme: UART, SPI, I2C, CAN, RS422/485, Ethernet, USB; gecikme | Blok şemadaki bağlantı tipleri | Her bağlantı için arayüz tipini gerekçesiyle seçersin | [ ] |
| 12 | Atış tetik elektroniği: solenoid/röle/MOSFET, flyback diyot, güvenli devre dışı | Tetik devresinin blok şemadaki yeri | Tetik hattını ve korumasını blok şemada gösterirsin | [ ] |
| 14 | Kablolama ve izolasyon: AWG, akım taşıma, ekranlı kablo, konnektör | Kablo tipleri; Şart. §4.1 | Akıma göre kesit seçer, blok şemaya yazarsın | [ ] |
| 15 | Şematik çizimi (KiCad) – yalnızca kendi kart tasarlanacaksa | Kart görseli | Basit bir güç dağıtım kartının şematiğini çizersin | [ ] |
| 16 | Kamera donanımı: çözünürlük, FOV, kare hızı, shutter, arayüz, lens, piksel boyutu | Kamera satırı (Kodi ile) | 15 m'de 20 cm'lik balonun kaç piksel olacağını hesaplarsın | [ ] |
| 19 | Kablo bazlı blok şema çizimi: sembol seti, çizgi türleriyle güç/sinyal/e-stop ayrımı | ÖTR §3.1 | Tüm sistemi 0,6 sayfaya sığan, her çizgisi etiketli bir şema olarak çizersin | [ ] |
| 20 | Tedarik araştırması: datasheet, fiyat, stok, teslim süresi, alternatif parça | Donanım tablosu; Sis'in malzeme listesi | Her ana parça için iki alternatifi fiyatı ve kaynağıyla tabloya koyarsın | [ ] |

## 2. 3 haftalık plan (Proje Planı H1–H3)
- **Hafta 1:** konu 1, 2, 5, 19; Meka'nın kütle v0'ı geldiyse ilk tork tahmini.
- **Hafta 2:** konu 3, 4, 6, 7, 12, 14; e-stop zinciri ve güç hattı blok şemaya işlenir.
- **Hafta 3:** konu 8, 9, 16, 20; Kodi ile kamera ve işlemci ön seçimi. Ardından H4'te kavramsal blok şema.

**Öğrenme kanıtı:** Her konu için 1 sayfalık çözülmüş örnek → Drive (04_Elektronik). Hedef: 13.12.2026.

## 3. ÖTR sonrası (şimdilik kapsam dışı)
PID ve kontrol döngüsü · sinyal koşullama · EMI/EMC ayrıntısı · PCB tasarımı ve lehim · FMEA · test ekipmanı ve enerji verme prosedürü.
ÖTR'den sonra ayrı planla ele alınacak.

## 4. Kaynaklar
**Kitaplar:** Horowitz & Hill, *The Art of Electronics* · Erickson & Maksimovic, *Fundamentals of Power Electronics* ·
Hughes, *Electric Motors and Drives* · Williams, *Making Embedded Systems*
**Ders:** MIT OCW 6.002 · TI motor sürme eğitimleri · ST motor kontrol notları · draw.io dokümantasyonu · KiCad dokümantasyonu
**Üretici (birincil):** motor, sürücü, enkoder, güç kaynağı, röle/kontaktör, e-stop, kamera datasheet'leri · Digi-Key, Mouser, yerel
tedarikçiler (fiyat, teslim süresi; kaynak ve tarih) · kablo ve konnektör akım tabloları
**Standartlar:** ISO 13850 · IEC 60204-1 (özet). Amaç hata-güvenli bakış açısı.
**Yarışma:** ÖTR şablonu §3.1, §3.3 · Şartname §4.1, §4.2, §4.3, §6 · teknofest.org raporları · Soru&Cevap (Sis tutar)
**Araçlar:** draw.io, KiCad, Python/numpy

## 5. Ajanla çalışma
- Önce kavramı öğren, sonra **kendi hesabını/şemanı** yap; Avi'ye "kontrol et, hatamı bul" de.
- Güvenlik devrelerinde (e-stop, limit) Avi'ye yalnızca inceleme yaptır; son karar lider ve Konti'nin incelemesidir.
- Blok şemanı ve donanım tablonu Sis'e ver; Sis, Kodi'nin yazılım arayüz şeması ve Meka'nın tablosuyla karşılaştırır.
- Yusuf'un elektrik-elektronik desteği aldığın kalemi Teslim Notu'nda "(Yusuf katkısı)" diye işaretle.
- Fiyat ve stok bilgisini her zaman tedarikçiden doğrula.
