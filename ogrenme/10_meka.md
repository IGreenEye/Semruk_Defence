# Öğrenme Rehberi – Meka (Mekanik Tasarım) · v2.1

Departman lideri: **Sezen** · Kapsam: **yalnızca ÖTR** (Ö1 → ÖTR §3.2 Mekanik, 10 puan, ~1 sayfa)

**Amaç:** Ö1'i (M1 v1 + M2 v0 + 3B model) yazabilmek için gereken konuları ve kaynakları göstermek. Liste **"yapabilme"**
üzerine kuruludur: her konunun sonunda küçük bir hesap ya da çizim yapabiliyor olmalısın.
**Kapsam kuralı:** ÖTR'ye kadar parça alımı, üretim, maket, test ve ölçüm yok; seçimler katalog, veri sayfası ve hesapla.

> Kitap ve kurs adları kurum/yazar ile verilmiştir. Bağlantılar değişebilir; adı arama motorunda ara.

## 0. ÖTR'de senden istenen (Ö1)
- **Bileşen tablosu:** taret yan ekseni, yükseliş ekseni, halka dişli/döner tabla yatağı, rulmanlar, aktarma, atış modülü, gövde. Hazır parçalarda üretici, model, özellik, fiyat.
- **Her bileşen için:** neden gerekli ve tasarımında neye dikkat edildi.
- **Tasarladığın parçalar için:** 3B model görseli.
- Avi'ye **kütle v0 tahmini** (%20 marjlı); Avi tork ön hesabını buna göre yapar.
- **Atış modülü:** aday aileleri karşılaştır ve öneri yaz; seçimi kaptan yapar.

Bu değerler **ÖN SEÇİM**'dir. Takvim: M1 v1 27.12 → M2 v0 24.01 → 3B model ve bileşen tablosu 31.01 → bölüm 07.02.

## 1. ÖTR için öğrenme listesi
| # | Konu | Neden (Ö1) | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|
| 1 | Statik ve moment dengesi, serbest cisim diyagramı | M2 v0: statik tork | Pitch ekseninde kütle ve kol uzunluğundan statik torku elle hesaplarsın | [ ] |
| 2 | Kütle merkezi ve atalet momenti (paralel eksen teoremi) | M2 v0: kütle ve atalet | Kutu + motor + kamera grubunun CG ve ataletini hesaplar, CAD ile karşılaştırırsın | [ ] |
| 3 | Dönel dinamik: tork, açısal ivme, hız profili | M1 v1: hız ve ivme gereksinimi | Hedef takibi için gereken °/s ve °/s² değerini çıkarırsın | [ ] |
| 4 | Pan-tilt mekanizma tipleri ve kinematiği | M1 v1: konsept seçimi | 2–3 mekanizma tipini boyut, boşluk, rijitlik, maliyet açısından karşılaştırırsın | [ ] |
| 5 | Parkur geometrisinden açı ve menzil hesabı | M1 v1: yaw/pitch aralığı | Çizimden 5-10-15 m şeritlerinde hedefe bakış açısını hesaplarsın | [ ] |
| 6 | Güç aktarımı: redüktör, planet dişli, kayış, boşluk | Bileşen tablosu: aktarma | Redüktör oranı ve verimiyle motor torkunu geriye hesaplarsın | [ ] |
| 7 | Malzeme mukavemeti temelleri: gerilme, eğilme, emniyet katsayısı | Malzeme seçimi gerekçesi | Bir konsol kolun uç sehimini ve maksimum gerilmesini elle hesaplarsın | [ ] |
| 11 | CAD (parametrik modelleme) ve montaj | 3B model görseli | Bir montajı parametrik modellersin | [ ] |
| 15 | Malzeme seçimi: Al alaşımları, çelik, PLA/PETG/ABS/naylon, karbon takviyeli baskı | Tablonun "özellik" sütunu | Kütle, dayanım, maliyet tablosu çıkarırsın | [ ] |
| 16 | Patlayıcısız balon patlatma yöntemleri ve güvenlik | Atış modülü karşılaştırması (R06) | 15 m için enerji, tekrarlanabilirlik, güvenlik karşılaştırma tablosu çıkarırsın | [ ] |
| 17 | Mekanik güvenlik kuralları: keskin kenar, yalıtım, mekanik durdurucu, e-stop yerleşimi | Şart. §4.2, R03, R12 | Konsept için güvenlik kontrol listesi yazarsın | [ ] |
| 20 | Hazır bileşen araştırması: model, özellik, fiyat, teslim süresi | Bileşen tablosu; Sis'in malzeme listesi | Her hazır parça için en az iki alternatifi fiyatı ve kaynağıyla tabloya koyarsın | [ ] |
| 21 | Teknik görselleştirme: render, patlatılmış ve ölçülü görünüş | 3B model görseli | 1/3 sayfada okunabilen, ana bileşenleri etiketli bir montaj görseli üretirsin | [ ] |

**Roket deneyiminle köprü:** CG, yük ve dayanım benzer; fark dönen kütle, atalet ve nişan kararlılığıdır.

## 2. 3 haftalık plan (Proje Planı H1–H3)
- **Hafta 1:** konu 1, 2, 3, 5; CAD pratiği (11).
- **Hafta 2:** konu 4, 16; atış modülü aday tablosu (katalog ve literatürden).
- **Hafta 3:** konu 6, 7, 17; konsept eskizleri. Ardından H4'te M1 v1 Teslim Notu.

**Öğrenme kanıtı:** Her konu için 1 sayfalık "çözülmüş örnek" → Drive (03_Mekanik). Hedef: 13.12.2026.

## 3. ÖTR sonrası (şimdilik kapsam dışı)
Geri tepme ve darbe yükü · titreşim · rulman/mil/civata hesabı · sonlu eleman analizi · GD&T ve toleranslar · imalat yöntemleri ·
kablo yönlendirme · test ve ölçüm. ÖTR'den sonra ayrı planla ele alınacak.

## 4. Kaynaklar
**Kitaplar:** Hibbeler, *Engineering Mechanics: Statics / Dynamics* · Beer & Johnston, *Mechanics of Materials* ·
*Shigley's Mechanical Engineering Design* · Norton, *Machine Design* · Craig, *Introduction to Robotics* · *Machinery's Handbook*
**Ders/video:** MIT OCW 2.003, 2.001/2.002 · CAD programınızın resmi eğitimleri ve render eğitimleri (SolidWorks, Fusion, Onshape)
**Üretici ve tedarikçi:** SKF, NSK, Misumi katalogları · yerel tedarikçiler (fiyatın kaynağını ve tarihini yaz)
**Standartlar:** ISO 12100 · ISO 13850
**Yarışma:** ÖTR şablonu §3.2 · Şartname §4.1, §4.2 · teknofest.org raporları (format için; alıntıda şablon formatı) · Soru&Cevap (Sis tutar)
**Araçlar:** CAD, CAD içi render, Python/numpy

## 5. Ajanla çalışma
- "Bu konuyu önce kavram, sonra çözümlü örnekle anlat" de; sonra **kendi hesabını** yapıp Meka'ya kontrol ettir.
- **Meka hesabı senin yerine yapmasın;** yalnızca kontrol etsin ve hatayı göstersin.
- Bileşen tablonu ve fiyatlarını Sis'e Teslim Notu ile ver; Sis malzeme listesine işler, çelişki varsa sana döner.
- Hesaplarını görünür yaz; Konti bağımsız tekrarlayacak.
