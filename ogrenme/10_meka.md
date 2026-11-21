# Öğrenme Rehberi – Meka (Mekanik Tasarım ve İmalat)

Departman lideri: **Güneş Beyaz**

**Amaç:** M1–M4 işlerine başlamadan önce neyi bilmen gerektiğini ve nereden öğreneceğini göstermek. Liste "bilgi" değil
"yapabilme" üzerine kuruludur: her konunun sonunda küçük bir hesap ya da çizim yapabiliyor olmalısın.

> Kitap ve kurs adları kurum/yazar ile verilmiştir. Bağlantılar değişebilir; adı arama motorunda ara.

## 1. Öğrenme listesi
Öncelik: **A** = M1'e başlamadan önce · **B** = M2 bitmeden önce · **C** = M3/M4 sırasında

| # | Konu | Öncelik | Neden (İP) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 1 | Statik ve moment dengesi, serbest cisim diyagramı | A | M2: motor torku, yük tablosu | Pitch ekseninde kütle ve kol uzunluğundan statik torku elle hesaplarsın | [ ] |
| 2 | Kütle merkezi ve atalet momenti (paralel eksen teoremi) | A | M2: dönen kütlenin ataleti | Kutu + motor + kamera grubunun CG ve ataletini hesaplar, CAD ile karşılaştırırsın | [ ] |
| 3 | Dönel dinamik: tork, açısal ivme, hız profili | A | M1/A1: hız ve ivme gereksinimi | Hedef takibi için gereken °/s ve °/s² değerini çıkarırsın | [ ] |
| 4 | Pan-tilt mekanizma tipleri ve kinematiği | A | M1: konsept seçimi | 2–3 mekanizma tipini boyut, boşluk, rijitlik, maliyet açısından karşılaştırırsın | [ ] |
| 5 | Parkur geometrisinden açı ve menzil hesabı | A | M1: yaw/pitch aralığı | Çizimden 5-10-15 m şeritlerinde hedefe bakış açısını hesaplarsın | [ ] |
| 6 | Güç aktarımı: redüktör, planet dişli, kayış, boşluk | B | M1/M2: nişan hassasiyeti | Redüktör oranı ve verimiyle motor torkunu geriye hesaplarsın | [ ] |
| 7 | Malzeme mukavemeti: gerilme, eğilme, burulma, emniyet katsayısı | B | M2: rijitlik ve dayanım | Konsol kolun uç sehimini ve maksimum gerilmesini elle hesaplarsın | [ ] |
| 8 | Geri tepme ve darbe yükü | B | M2: gövde ve bağlantı yükü | Atış modülünün itkisinden darbe kuvvetini kabaca tahmin edersin | [ ] |
| 9 | Titreşim: doğal frekans, rezonans, sönüm | B | M2/M3: nişan ve kamera kararlılığı | Kütle-yay modelinden doğal frekans bulursun | [ ] |
| 10 | Rulman, mil, civata, bağlantı elemanı seçimi | B | M3: montaj | Civata bağlantısında ön gerilme ve kesme kapasitesi kontrolü yaparsın | [ ] |
| 11 | CAD (parametrik), montaj ve teknik resim | A | M1–M3: çizimler, KTR görselleri | Montajı parametrik modeller, boyutlu teknik resim çıkarırsın | [ ] |
| 12 | Sonlu eleman analizi (statik, modal) | B | M2: doğrulama | Basit bir parçada el hesabıyla FEA sonucunu karşılaştırırsın | [ ] |
| 13 | GD&T, geçme toleransları | C | M3/M4: imalat | Rulman yuvası ve mil için tolerans seçersin | [ ] |
| 14 | İmalat: CNC, lazer kesim, sac bükme, 3B baskı (FDM/SLA) | C | M3/M4: yöntem seçimi | Bir parça için yöntem, malzeme, tolerans kararı verir, gerekçeni yazarsın | [ ] |
| 15 | Malzeme seçimi: Al alaşımları, çelik, PLA/PETG/ABS/naylon, karbon takviyeli baskı | C | M1/M3: kütle-dayanım | Kütle, dayanım, maliyet tablosu çıkarırsın | [ ] |
| 16 | Patlayıcısız balon patlatma yöntemleri ve güvenlik | A | M1: atış modülü (R06) | 15 m için enerji, tekrarlanabilirlik, güvenlik karşılaştırma tablosu çıkarırsın | [ ] |
| 17 | Mekanik güvenlik: keskin kenar, sıkışma noktası, durdurucu, e-stop yerleşimi | B | M1/M3: R02, R03, R12 | Güvenlik kontrol listesi yazarsın | [ ] |
| 18 | Kablo yönlendirme, kablo zinciri, konnektör yuvası (Avi ile) | C | M3 | Kablo yolu ve bükülme yarıçapıyla hareketli kablo planı çizersin | [ ] |
| 19 | Test ve ölçüm: tolerans, kütle, boyut doğrulama | C | M4: R01 | Kumpas, mikrometre, tartı ile ölçüm doğrulama planı yazarsın | [ ] |

**Roket deneyiminle köprü:** CG, yük ve dayanım konuları benzer. Fark: burada dönen kütle, atalet ve nişan kararlılığı
(dinamik doğruluk) ön planda; aerodinamiğin ağırlığı çok düşük.

## 2. 3 haftalık plan (M1 hazırlığı)
- **Hafta 1:** konu 1, 2, 3, 5; CAD pratiği (11)
- **Hafta 2:** konu 4 ve 16; parkur geometrisi hesabı
- **Hafta 3:** konu 6, 7, 8, 17; M1 Teslim Notu taslağı

**Öğrenme kanıtı:** Her konu için 1 sayfalık "çözülmüş örnek" → `ogrenme/kanitlar/meka/` (KTR Tecrübe ve Mekanik bölümüne malzeme).

## 3. Kaynaklar
**Kitaplar:** Hibbeler, *Engineering Mechanics: Statics / Dynamics* · Beer & Johnston, *Mechanics of Materials* ·
*Shigley's Mechanical Engineering Design* (Budynas & Nisbett) · Norton, *Machine Design* · Craig, *Introduction to Robotics* ·
Rao, *Mechanical Vibrations* · *Machinery's Handbook* · Boothroyd, Dewhurst & Knight, *Product Design for Manufacture and Assembly*

**Ders/video:** MIT OCW 2.003 Engineering Dynamics, 2.001/2.002 Mechanics and Materials · MIT OCW robotik dersleri ·
YouTube mekanik ders serileri · SolidWorks / Autodesk Fusion / Onshape Learning Center · Prusa Knowledge Base

**Üretici:** SKF, NSK, Misumi katalogları · motor üretici mekanik çizimleri (Avi ile) · yerel lazer/CNC atölyeleri

**Standartlar:** ISO 12100 (risk değerlendirmesi) · ISO 13850 (acil durdurma) · ISO 286 (tolerans ve geçmeler)

**Yarışma:** Şartname ve KTR şablonu §4.1 · teknofest.org yayımlanmış raporlar (format için; alıntıda kaynak göster) · Soru&Cevap grubu

**Araçlar:** CAD (SolidWorks/Fusion/Onshape), FEA, Python/numpy, dilimleyici (PrusaSlicer/Cura/Bambu Studio)

## 4. Ajanla çalışma
- "Bu konuyu X seviyesinde, önce kavramı sonra çözümlü örneği anlat" de; sonra kendi hesabını yapıp Meka'ya kontrol ettir.
- **Meka hesabı senin yerine yapmasın;** yalnızca kontrol etsin ve hatayı göstersin.
- Konti bağımsız doğrulayacağı için hesaplarını görünür yaz.

Claude Code'da: `> meka ajanını kullan: konu 1'i lisans seviyesinde anlat, sonra benim hesabımı kontrol et`
