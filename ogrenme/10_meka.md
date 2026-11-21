# Öğrenme Rehberi – Meka (Mekanik Tasarım ve İmalat) · v2

Departman lideri: **Sezen** · Kaynak: Drive "10 Öğrenme Rehberi – Meka (v2)"

**v2'de ne değişti:** ÖTR'ye göre yeni öncelik (**Ö**) eklendi; ÖTR için gereken konular öne alındı. Yeni konular: 20 (hazır
bileşen araştırması), 21 (teknik görselleştirme). 3 haftalık plan ÖTR'ye göre yeniden yazıldı.

**Amaç:** Ö1 (ÖTR mekanik ön tasarımı) ve M1–M4 işlerinden önce neyi bilmen gerektiğini ve nereden öğreneceğini göstermek.
Liste **"yapabilme"** üzerine kuruludur: her konunun sonunda küçük bir hesap ya da çizim yapabiliyor olmalısın.

> Kitap ve kurs adları kurum/yazar ile verilmiştir. Bağlantılar değişebilir; adı arama motorunda ara.

## 0. ÖTR'de senden istenen (Ö1)
Mekanik bölüm **10 puan**, yaklaşık **1 sayfa**:
- **Bileşen tablosu:** taret yan ekseni, yükseliş ekseni, halka dişli/döner tabla yatağı, rulmanlar, aktarma, atış modülü, gövde. Hazır parçalarda üretici, model, özellik, fiyat.
- **Her bileşen için:** neden gerekli ve tasarımında neye dikkat edildi.
- **Tasarladığın parçalar için:** 3B model görseli ya da prototip fotoğrafı.
- Avi'ye **kütle v0 tahmini** (marjlı); Avi tork ön hesabını buna göre yapar.

Bu değerler **ÖN SEÇİM**'dir; KTR'de M1–M2 kapılarından geçerek kesinleşir. Mekanik KTR'de 20 puan; asıl derinlik orada.

## 1. Öğrenme listesi
Öncelik: **Ö** = Ö1'den önce · **A** = M1'den önce · **B** = M2 bitmeden önce · **C** = M3/M4 sırasında

| # | Konu | Öncelik | Neden (İP) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 1 | Statik ve moment dengesi, serbest cisim diyagramı | A | M2: motor torku, yük tablosu | Pitch ekseninde kütle ve kol uzunluğundan statik torku elle hesaplarsın | [ ] |
| 2 | Kütle merkezi ve atalet momenti (paralel eksen teoremi) | **Ö** | Ö1: kütle v0; M2: dönen kütle ataleti | Kutu + motor + kamera grubunun CG ve ataletini hesaplar, CAD ile karşılaştırırsın | [ ] |
| 3 | Dönel dinamik: tork, açısal ivme, hız profili | A | M1/A1: hız ve ivme gereksinimi | Hedef takibi için gereken °/s ve °/s² değerini çıkarırsın | [ ] |
| 4 | Pan-tilt mekanizma tipleri ve kinematiği | **Ö** | Ö1/M1: konsept seçimi | 2–3 mekanizma tipini boyut, boşluk, rijitlik, maliyet açısından karşılaştırırsın | [ ] |
| 5 | Parkur geometrisinden açı ve menzil hesabı | **Ö** | Ö1/M1: yaw/pitch aralığı | Çizimden 5-10-15 m şeritlerinde hedefe bakış açısını hesaplarsın | [ ] |
| 6 | Güç aktarımı: redüktör, planet dişli, kayış, boşluk | B | M1/M2: nişan hassasiyeti | Redüktör oranı ve verimiyle motor torkunu geriye hesaplarsın | [ ] |
| 7 | Malzeme mukavemeti: gerilme, eğilme, burulma, emniyet katsayısı | B | M2: rijitlik ve dayanım | Konsol kolun uç sehimini ve maksimum gerilmesini elle hesaplarsın | [ ] |
| 8 | Geri tepme ve darbe yükü | B | M2: gövde ve bağlantı yükü | Atış modülünün itkisinden darbe kuvvetini kabaca tahmin edersin | [ ] |
| 9 | Titreşim: doğal frekans, rezonans, sönüm | B | M2/M3: nişan ve kamera kararlılığı | Kütle-yay modelinden doğal frekans bulursun | [ ] |
| 10 | Rulman, mil, civata, bağlantı elemanı seçimi | B | M3: montaj | Civata bağlantısında ön gerilme ve kesme kapasitesi kontrolü yaparsın | [ ] |
| 11 | CAD (parametrik), montaj ve teknik resim | **Ö** | Ö1: 3B model görseli; M1–M3 | Montajı parametrik modeller, boyutlu teknik resim çıkarırsın | [ ] |
| 12 | Sonlu eleman analizi (statik, modal) | B | M2: doğrulama | Basit bir parçada el hesabıyla FEA sonucunu karşılaştırırsın | [ ] |
| 13 | GD&T, geçme toleransları | C | M3/M4: imalat | Rulman yuvası ve mil için tolerans seçersin | [ ] |
| 14 | İmalat: CNC, lazer kesim, sac bükme, 3B baskı (FDM/SLA) | C | M3/M4: yöntem seçimi | Bir parça için yöntem, malzeme, tolerans kararı verir, gerekçeni yazarsın | [ ] |
| 15 | Malzeme seçimi: Al alaşımları, çelik, PLA/PETG/ABS/naylon, karbon takviyeli baskı | **Ö** | Ö1: tablonun "özellik" sütunu; M3 | Kütle, dayanım, maliyet tablosu çıkarırsın | [ ] |
| 16 | Patlayıcısız balon patlatma yöntemleri ve güvenlik | **Ö** | Ö1/M1: atış modülü ön seçimi (R06) | 15 m için enerji, tekrarlanabilirlik, güvenlik karşılaştırma tablosu çıkarırsın | [ ] |
| 17 | Mekanik güvenlik: keskin kenar, sıkışma noktası, durdurucu, e-stop yerleşimi | B | M1/M3: R02, R03, R12 | Güvenlik kontrol listesi yazarsın | [ ] |
| 18 | Kablo yönlendirme, kablo zinciri, konnektör yuvası (Avi ile) | C | M3 | Kablo yolu ve bükülme yarıçapıyla hareketli kablo planı çizersin | [ ] |
| 19 | Test ve ölçüm: tolerans, kütle, boyut doğrulama | C | M4: R01 | Kumpas, mikrometre, tartı ile ölçüm planı yazarsın | [ ] |
| 20 | **Yeni:** Hazır bileşen araştırması: halka dişli/döner tabla yatağı, rulman, kayış-kasnak, redüktör, atış mekanizması; model, özellik, fiyat, teslim süresi | **Ö** | Ö1: bileşen tablosu; Sis'in malzeme listesi | Her hazır parça için en az iki alternatifi fiyat ve teslim süresiyle tabloya koyarsın | [ ] |
| 21 | **Yeni:** Teknik görselleştirme: render, patlatılmış görünüş, ölçülü görünüş; rapora uygun çözünürlük | **Ö** | Ö1: 3B model görseli; KTR görselleri | 1/3 sayfada okunabilen, ana bileşenleri etiketli bir montaj görseli üretirsin | [ ] |

**Roket deneyiminle köprü:** CG, yük ve dayanım benzer. Fark: burada **dönen kütle, atalet ve nişan kararlılığı** ön planda;
aerodinamiğin ağırlığı çok düşük.

## 2. 3 haftalık plan (Ö1 hazırlığı)
- **Hafta 1:** konu 4, 5, 16 (mekanizma tipi, açı aralığı, atış yöntemi karşılaştırması); CAD pratiği (11).
- **Hafta 2:** konu 2, 15, 20 (kütle v0, malzeme, hazır parça ve fiyat araştırması).
- **Hafta 3:** konu 21; **Ö1 Teslim Notu taslağı**: bileşen tablosu, kısa gerekçeler, 3B ön model görseli, kütle v0.

Ö1 bitince KTR için: konu 1, 3, 6, 7, 8 (M1–M2), ardından B ve C grubu.
**Öğrenme kanıtı:** Her konu için 1 sayfalık "çözülmüş örnek" → Drive (03_Mekanik). KTR Tecrübe ve Mekanik bölümüne malzeme olur.

## 3. Kaynaklar
**Kitaplar:** Hibbeler, *Engineering Mechanics: Statics / Dynamics* · Beer & Johnston, *Mechanics of Materials* ·
*Shigley's Mechanical Engineering Design* (Budynas & Nisbett) · Norton, *Machine Design* · Craig, *Introduction to Robotics* ·
Rao, *Mechanical Vibrations* · *Machinery's Handbook* · Boothroyd, Dewhurst & Knight, *Product Design for Manufacture and Assembly*

**Ders/video:** MIT OCW 2.003, 2.001/2.002 · MIT OCW robotik/kinematik · YouTube mekanik ders serileri ve CAD programınızın
resmi kanalları · SolidWorks / Autodesk Fusion / Onshape Learning Center; render eğitimleri · 3B baskı malzeme rehberleri

**Üretici ve tedarikçi (Ö1 için birincil):** SKF, NSK, Misumi katalogları (rulman, döner tabla yatağı, redüktör, kayış-kasnak) ·
yerel tedarikçiler (fiyat ve teslim süresi; kaynağını ve tarihini yaz) · motor üretici mekanik çizimleri (Avi ile) ·
yerel lazer/CNC atölyeleri (imalattan önce görüş al)

**Standartlar:** ISO 12100 · ISO 13850 · ISO 286

**Yarışma:** ÖTR şablonu §3.2 · Şartname ve KTR şablonu §4.1 · teknofest.org raporları (format için; alıntıda şablon formatı) ·
Soru&Cevap (Sis tutar)

**Araçlar:** CAD (SolidWorks/Fusion/Onshape), CAD içi render ve FEA, Python/numpy, dilimleyici

## 4. Ajanla çalışma
- "Bu konuyu önce kavram, sonra çözümlü örnekle anlat" de; sonra **kendi hesabını** yapıp Meka'ya kontrol ettir.
- **Meka hesabı senin yerine yapmasın;** yalnızca kontrol etsin ve hatayı göstersin.
- Bileşen tablonu ve fiyatlarını Sis'e Teslim Notu ile ver; Sis malzeme listesine işler, çelişki varsa sana döner.
- Hesaplarını görünür yaz; Konti bağımsız tekrarlayacak.
