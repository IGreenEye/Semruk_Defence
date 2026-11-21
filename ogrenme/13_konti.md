# Öğrenme Rehberi – Konti (Bağımsız Doğrulama) · v2

Kullanan: **Yusuf Köse** · Kaynak: Drive "13 Öğrenme Rehberi – Konti (v2, daraltıldı)"

**v2'de ne değişti:** Konti'nin görevi daraldı. Gereksinim yazımı, yaşam döngüsü, ICD, proje yönetimi, puan stratejisi,
operasyon planı ve rapor yazımı **Sis**'e geçti (`ogrenme/14_sis.md`). ÖTR için hakem incelemesi, biçim ve diyagram denetimi
eklendi. Liste 17 konudan 13'e indi.

**Amaç:** Başkasının ürettiği işi **bağımsız olarak doğrulayabilmek**. Konti tasarım yapmaz, rapor bölümü yazmaz, plan yapmaz;
kapıda **"doğru mu, kanıtı ne?"** sorusunu cevaplar.

**Bağımsızlık kuralı:** Konti'yi kullanan kişi kendi departmanının işini doğrulamaz. Bu takımda Konti'yi Yusuf kullanır; Yusuf
Sis'i de kullandığı için **Sis'in çıktıları Sezen veya Eren yanındayken ve onların onayıyla** doğrulanır (`docs/kapi_protokolu.md`).
Kaptan son onayı verir.

## 0. ÖTR'de senden istenen (Ö8)
Konti ÖTR'de hiçbir bölümü yazmaz; Sis'in derlediği taslağı hakem gözüyle inceler (H14, 22–28.02).
- **Puan tahmini:** her bölüm şablondaki puanıyla (Özet 5, Blok şema 5, Mekanik 10, Donanım 20, Yazılım 20, Malzeme listesi 5, Yöntem 25, Zaman-bütçe 5, Rapor düzeni 5).
- **Düzeltme listesi:** en çok puan kazandıracak ilk 3 düzeltme önce.
- **Hesap tekrarı:** kütle v0, tork, güç, piksel/menzil; %10'dan büyük farkı sahibine geri gönder.
- **Kontrol listesi:** R16 (biçim), R17 (kişisel veri), R18 (içerik zorunlulukları) madde madde.
- **Alıntı ve benzerlik:** geçmiş raporlardan alınan her cümle şablon formatıyla gösterilmiş mi; aynı/çok benzer metin riski var mı.

## 1. Öğrenme listesi
Öncelik: **Ö** = Ö8'den önce · **A** = ilk KTR kapılarından (M2, A2) önce · **B** = test planlarından önce · **C** = test ve entegrasyon

| # | Konu | Öncelik | Neden | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 1 | Doğrulama yöntemleri: analiz, test, inceleme, gösterim | **Ö** | Her kapıda onay kriteri | Her gereksinim için uygun doğrulama yöntemini seçersin | [ ] |
| 2 | Hakem gibi değerlendirme: ÖTR/KTR puan kriterleri, puan tahmini, düzeltme önceliklendirme | **Ö** | Ö8; KTR incelemesi | Bir bölümü puanlar, puanı en çok artıracak 3 düzeltmeyi gerekçesiyle yazarsın | [ ] |
| 3 | Bağımsız hesap kontrolü: büyüklük mertebesi, birim analizi, sınır durum, farklı yöntemle tekrar | **Ö** | Ö8: ön hesaplar; her kapı | Meka/Avi'nin tork ve güç hesabını kendi yönteminle tekrarlayıp farkı raporlarsın | [ ] |
| 4 | Gereksinim doğrulama: test edilebilir mi, tasarım karşılıyor mu (yazmak Sis'te) | **Ö** | REQ listesinin kontrolü | Bir gereksinimin ölçülemeyen yerini bulup Sis'e geri verirsin | [ ] |
| 5 | Biçim ve uygunluk denetimi: şablon kuralları, kişisel veri, alıntı formatı, benzerlik riski | **Ö** | Ö8: R16–R18 | ÖTR kontrol listesini bir taslak üzerinde eksiksiz işaretlersin | [ ] |
| 6 | Diyagram okuma ve denetimi: aktivite, sekans, durum makinesi; kural diyagramda var mı | **Ö** | Ö8: Yöntem (25) | Bir aşama diyagramında eksik kural dalını (ceza, menzil, e-stop) bulursun | [ ] |
| 7 | FMEA ve hata ağacı | A | A2: e-stop ve yasak alan | E-stop için FMEA tablosu doldurursun | [ ] |
| 8 | Güvenlik ve risk değerlendirmesi (hata-güvenli tasarım) | A | KTR §6, Şart. 4.2 | "Hata durumunda güvenli" gerekçesini sorgularsın | [ ] |
| 9 | Kötü gün senaryoları: kablo kopması, güç kesintisi, yazılım çökmesi, yanlış hedef, ışık | B | KTR §4.4.3, T1/T2 | 10 senaryo listeleyip beklenen davranışı yazarsın | [ ] |
| 10 | Test tasarımı: plan, kabul kriteri, test seti bağımsızlığı, tekrarlanabilirlik, kayıt | B | T1–T4 | Girdi/adım/beklenen sonuç/geçti-kaldı içeren test planı yazarsın | [ ] |
| 11 | İstatistik: ortalama, std, güven aralığı, hata matrisi | B | Y1 doğrulama, isabet | 20 atışın isabet oranını güven aralığıyla yorumlarsın | [ ] |
| 12 | Entegrasyon testi: arayüz uyumsuzluğu bulma | C | T1–T2 | Entegrasyon sırasını ve başarısızlık kriterlerini yazarsın | [ ] |
| 13 | Kök neden analizi (5 Neden, balık kılçığı), düzeltici faaliyet | C | T1–T4 | Bir test başarısızlığı için kök neden ve düzeltici faaliyet yazarsın | [ ] |

## 2. 2 haftalık plan
- **Hafta 1:** konu 1, 2, 4, 5 → ÖTR hakem kontrol listesi (bölüm, puan, kontrol soruları, R16–R18).
- **Hafta 2:** konu 3, 6 → ön hesapları tekrarlayan küçük Python betikleri (tork, güç, piksel/menzil); diyagram denetim listesi.
- Sonra, A2 kapısından önce: konu 7, 8 (e-stop FMEA şablonu hazır olsun).

**Öğrenme kanıtı:** Kontrol listeleri ve doğrulama betikleri → Drive (00_Yönetim / 07_Test ve Deney). KTR Test ve Güvenlik bölümlerine kanıt.

## 3. Kaynaklar
**Kitaplar:** *NASA Systems Engineering Handbook* (NASA/SP-2016-6105; doğrulama ve onaylama bölümleri) · AIAG & VDA FMEA El Kitabı ·
Montgomery & Runger, *Applied Statistics and Probability for Engineers* · 5 Neden / Ishikawa ders notları

**Standartlar:** IEC 60812 · ISO 12100, ISO 13850, ISO 13849-1

**Yarışma (birincil):** ÖTR şablonu (puanlar, "Rapor taslakları ile ilgili not") · KTR şablonu · Şartname §2.4 (kopya rapor
diskalifiye kuralı), §4.2, §6 · TEKNOFEST Genel Kurallar ve Etik Kurallar

**Araçlar:** Kontrol listeleri (Sheets), Python, PDF okuyucu ve karşılaştırma, Durum Tablosu v2

## 4. Ajanla çalışma
- Konti'yi **hakem gibi** kullan: "bu bölümü ÖTR puan kriterine göre puanla, eksikleri ve en büyük 3 düzeltmeyi yaz."
- Hesap doğrularken **önce kendi sonucunu yaz**, sonra Konti'ye karşılaştırt.
- Bulguyu sahibine geri ver; **tasarımı ve metni Konti düzeltmesin**.
- Sis'in yazdığı bölümler de Konti incelemesinden geçer; Sezen veya Eren yanındayken.
