# Öğrenme Rehberi – Konti (Bağımsız Doğrulama) · v2.1

Kullanan: **Yusuf Köse** · Kapsam: **yalnızca ÖTR** (Ö8 hakem incelemesi; T0 ve M1 tam kapı doğrulaması; Ö işlerinin kontrolü)

**Amaç:** Başkasının ürettiği işi **bağımsız olarak doğrulayabilmek**. Konti tasarım yapmaz, rapor bölümü yazmaz, plan yapmaz;
kapıda **"doğru mu, kanıtı ne?"** sorusunu cevaplar.

**Bağımsızlık kuralı:** Konti'yi kullanan kişi kendi departmanının işini doğrulamaz. Konti'yi Yusuf kullanır; Yusuf Sis'i de
kullandığı için **Sis'in çıktıları ve "(Yusuf katkısı)" işaretli kalemler Sezen veya Eren yanındayken ve onların onayıyla**
doğrulanır. Kaptan son onayı verir.

## 0. ÖTR'de senden istenen
- **Ö işleri:** ön hesapları (kütle v0, tork, güç, piksel/menzil) kendi yönteminle tekrarla; %10'dan büyük farkı sahibine geri gönder.
- **M1 v1 (H4):** geometri ve açı hesaplarını bağımsız tekrarla.
- **Ö8 hakem incelemesi (H14, 22–28.02):**
  - Puan tahmini: her bölüm şablondaki puanıyla (Özet 5, Blok şema 5, Mekanik 10, Donanım 20, Yazılım 20, Malzeme listesi 5, Yöntem 25, Zaman-bütçe 5, Rapor düzeni 5).
  - Düzeltme listesi: en çok puan kazandıracak ilk 3 düzeltme önce.
  - Kontrol listesi: R16 (biçim), R17 (kişisel veri), R18 (içerik zorunlulukları) madde madde.
  - Alıntı ve benzerlik: geçmiş raporlardan alınan her cümle şablon formatıyla gösterilmiş mi; aynı/çok benzer metin riski var mı (Şart. §2.1, diskalifiye).

## 1. ÖTR için öğrenme listesi
| # | Konu | Neden | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|
| 1 | Doğrulama yöntemleri: analiz, inceleme, gösterim | Her kapıda onay kriteri | Her gereksinim için uygun doğrulama yöntemini seçersin | [ ] |
| 2 | Hakem gibi değerlendirme: ÖTR puan kriterleri, puan tahmini, düzeltme önceliklendirme | Ö8 | Bir bölümü puanlar, puanı en çok artıracak 3 düzeltmeyi gerekçesiyle yazarsın | [ ] |
| 3 | Bağımsız hesap kontrolü: büyüklük mertebesi, birim analizi, sınır durum, farklı yöntemle tekrar | Ö işleri, M1 | Meka/Avi'nin tork ve güç hesabını kendi yönteminle tekrarlayıp farkı raporlarsın | [ ] |
| 4 | Gereksinim doğrulama: test edilebilir mi, tasarım karşılıyor mu (yazmak Sis'te) | REQ listesinin kontrolü | Bir gereksinimin ölçülemeyen yerini bulup Sis'e geri verirsin | [ ] |
| 5 | Biçim ve uygunluk denetimi: şablon kuralları, kişisel veri, alıntı formatı, benzerlik riski | Ö8: R16–R18 | ÖTR kontrol listesini bir taslak üzerinde eksiksiz işaretlersin | [ ] |
| 6 | Diyagram okuma ve denetimi: aktivite, sekans, durum makinesi | Ö8: Yöntem (25) | Bir aşama diyagramında eksik kural dalını (ceza, menzil, e-stop) bulursun | [ ] |

## 2. 2 haftalık plan
- **Hafta 1:** konu 1, 2, 4, 5 → ÖTR hakem kontrol listesi (bölüm, puan, kontrol soruları, R16–R18).
- **Hafta 2:** konu 3, 6 → ön hesapları tekrarlayan hesap sayfaları (tork, güç, piksel/menzil); diyagram denetim listesi.

**Öğrenme kanıtı:** Kontrol listeleri ve hesap sayfaları → Drive (00_Yönetim). Hedef: 13.12.2026.

## 3. ÖTR sonrası (şimdilik kapsam dışı)
FMEA ve hata ağacı · kötü gün senaryoları · test tasarımı ve istatistik · entegrasyon testi · kök neden analizi.
ÖTR'den sonra ayrı planla ele alınacak.

## 4. Kaynaklar
**Kitap:** *NASA Systems Engineering Handbook* (NASA/SP-2016-6105; doğrulama bölümleri)
**Yarışma (birincil):** ÖTR şablonu (puanlar, "Rapor taslakları ile ilgili not") · Şartname §2.1 (kopya rapor kuralı), §2.4, §4.2 ·
TEKNOFEST Genel Kurallar ve Etik Kurallar (alıntı ve kaynak gösterme)
**Araçlar:** Kontrol listeleri (Sheets), Python, PDF okuyucu ve karşılaştırma, Durum Tablosu v3 (Google E-Tablo)

## 5. Ajanla çalışma
- Konti'yi **hakem gibi** kullan: "bu bölümü ÖTR puan kriterine göre puanla, eksikleri ve en büyük 3 düzeltmeyi yaz."
- Hesap doğrularken **önce kendi sonucunu yaz**, sonra Konti'ye karşılaştırt.
- Bulguyu sahibine geri ver; **tasarımı ve metni Konti düzeltmesin**.
- Sis'in bölümlerini doğrularken Sezen veya Eren yanında olsun; Teslim Notu'na doğrulayan olarak onların adı yazılır.
