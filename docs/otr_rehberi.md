# ÖTR Rehberi

Kaynak: 05 ÖTR Yol Haritası v2, Semrük Proje Planı v3, 2026 ÖTR Şablonu (geçen yılın, referans).
2027 şablonu yaklaşık Mart başında gelecek; gelince bu dosya güncellenir. Plan ile çelişirse **Plan geçerlidir**.

ÖTR 100 puan ve en fazla 10 sayfadır; kapak ve içindekiler 2 sayfa aldığı için içerik **8 sayfaya** sığmalıdır.
Puanın **45'i Kodi'de** (yazılım + yöntem), **25'i Avi'de** (blok şema + donanım).

## 1. Bölüm planı
| Bölüm | Puan | Sahip (ajan / lider) | İP | Şablonun istediği | Sayfa | Konti'nin soracağı |
|---|---|---|---|---|---|---|
| Kapak + İçindekiler | – | Sis / Yusuf | Ö7 | Takım adı, takım ID, başvuru ID; iki ayrı sayfa | 2 | Ayrı sayfalar mı? |
| 1 Proje özeti | 5 | Sis / Yusuf | Ö7 | Yürütülen faaliyetlerin özeti | 0,3 | Sistem ve yaklaşım bir paragrafta anlaşılıyor mu? |
| 2 Takım şeması | – | Sis / Yusuf | Ö0 | Tablo: sayı, görev, eğitim seviyesi, sınıf, üye rolü; farklı disiplinler | 0,3 | İsim ya da iletişim bilgisi var mı? (varsa değerlendirme dışı) |
| 3.1 Sistem blok şeması | 5 | Avi / Sıla | Ö2 | Kablo bazlı: tüm alt birimler, bağlantı tipleri, kablo tipleri | 0,6 | Her bağlantının tipi ve kablosu yazılı mı? |
| 3.2 Mekanik tasarım | 10 | Meka / Sezen | Ö1 | Bileşen tablosu (üretici, model, özellik, fiyat); neden gerekli; dikkat edilenler; 3B model ya da prototip görseli | 1 | Tasarlanan her parçanın görseli var mı? |
| 3.3 Donanım tasarım | 20* | Avi / Sıla | Ö2 | Bileşen tablosu; ne için gerekli, özellikleri, seçim gereksinimleri; kendi kartlar için çizim | 1,3 | Her seçimin gerekçesi bir gereksinime bağlı mı? |
| 3.4 Yazılım tasarım | 20 | Kodi / Eren | Ö3 | Bileşen tablosu (hazırlarda üretici ve sürüm); yazılımlar arası arayüz; temel gereksinimler; kod yok | 1,3 | Arayüz şeması blok şemayla tutarlı mı? |
| 3.5 Malzeme listesi | 5 | Sis / Yusuf | Ö5 | Tüm bileşenlerin listesi ve fiyatları | 0,5 | Toplam doğru mu, fiyatlar kaynaklı mı? |
| 4 Yöntem | 25 | Kodi / Eren | Ö4 | Her aşama için ayrı aktivite ve sekans diyagramı; mod geçişi için durum makinesi | 1,7 | Diyagramlar şartname kurallarını gösteriyor mu? |
| 5 Zaman ve bütçe | 5 | Sis / Yusuf | Ö5 | Üretim ve test zaman planı; tahmini bütçe; yöntem ve proje takip aracı | 0,5 | Plan gerçekçi mi, araç tanıtılmış mı? |
| 6 Rapor düzeni, kaynakça | 5 | Sis / Yusuf | Ö7 | Sayfa sınırı, akademik yazım, içindekiler, detaylı kaynakça | 0,5 | Kaynaklar şablondaki formatta mı? |
| **Toplam** | **100** | | | | **10** | |

\* Şablonda içindekilerde 20, metinde 25 yazıyor; toplam 100 için 20 kullanılır. Soru Soru&Cevap listesinde.

## 2. Bölüm bazında dikkat edilecekler
**Yöntem (25, Kodi):** 3 aşama × 2 diyagram + 1 durum makinesi = 7 görsel, 1,7 sayfa. Her aşamaya ~yarım sayfa (aktivite ve
sekans yan yana). Yer yetmezse durum makinesi küçültülür; aşama diyagramları küçültülmez. Yazılar okunaklı kalmalı.
- Aşama-1: manuel mod, zarfla gelen hedef sırası, operatörün yönlendirme ve ateş komutu, yanlış sıra cezasından kaçınma,
  sıradaki hedef parkurda yoksa ya da yalnızca daha düşük bir menzil bölgesinde kalmışsa pas geçme kuralı.
- Aşama-2: otonom mod, üç koldan gelen hedeflerin tespiti, hedef önceliklendirme, tur sonu.
- Aşama-3: otonom mod, renkle dost-düşman ayrımı, hedef tipine göre menzil (F16 10–15 m, helikopter/füze 5–15 m, İHA 0–15 m), dosta ateş etmeme.
- Her aşamada: e-stop, hareket-yasak ve atış-yasak alan davranışı, 0°/0° başlangıç.

**Blok şema (5, Avi):** Kutular arasındaki her çizgi bir kablodur; üzerinde bağlantı tipi (USB 3, CAN, RS485, PWM, 24 VDC,
220 VAC) ve kablo tipi (ekranlı, kesit, konnektör) yazar. Güç, sinyal ve e-stop hatları farklı çizgi türüyle ayrılır.

**Donanım ve mekanik tabloları (Avi, Meka):** Model ve fiyat sütunu boş bırakılmaz. Seçim kesin değilse ÖN SEÇİM yazılır.

**Malzeme listesi (Sis):** Aynı parça mekanik, donanım ve yazılım tablolarında aynı adla ve aynı fiyatla geçmeli.

## 3. Biçim kontrol listesi (R16, R17)
- [ ] Toplam 3–10 sayfa (kapak, içindekiler, kaynakça ve ekler dahil)
- [ ] Kapak ve içindekiler iki ayrı sayfa; kapakta takım adı, takım ID, başvuru ID
- [ ] Yazı tipi Arial 12; başlıklar Arial Black 14
- [ ] Satır aralığı 1,15; metin iki yana yaslı
- [ ] Kenar boşlukları: üst 2,8 cm; alt, sağ, sol 2,5 cm
- [ ] Takım şemasında isim, soyisim, T.C. kimlik no, iletişim bilgisi yok
- [ ] Tekrarlayan cümle yok
- [ ] Geçmiş yıl raporlarından her alıntı, cümlenin hemen ardından: "Alıntı" (Yıl, Yarışma Adı, Kategori, Takım Adı)
- [ ] Kaynakça: Dijital → Soyadı, Adın baş harfi., Yazının başlığı, Yazının tarihi, Erişim tarihi, Erişim adresi.
      Basılı → Soyadı, Adın baş harfi., (Basım tarihi) Başlık, (varsa) dergi adı, sayısı, sayfa numarası
- [ ] Şablondaki başlık numaraları ve sırası korunmuş; "Rapor taslakları ile ilgili not" sayfası rapora eklenmemiş

## 4. Geri sayım (Plan v3; 2027 takvimi geçen yılla aynı VARSAYIMI)
| İP | Ne | Tarih | Kim |
|---|---|---|---|
| Ö0 | ÖTR iskeleti ve sayfa bütçesi; takım şeması | 06.12 (iskelet), 13.12 (takım şeması) | Sis |
| Ö1 | M1 v1 ONAYLI → M2 v0 → 3B model ve bileşen tablosu; §3.2 teslimi | 27.12 → 24.01 → 31.01; bölüm 07.02 | Meka |
| Ö2 | A1 v0 (model ve fiyatla seçim); A2 v0 blok şema; §3.3 ve §3.1 teslimi | 31.01; blok şema 14.02; §3.3 07.02, §3.1 14.02 | Avi |
| Ö3 | Yazılım bileşen tablosu ve arayüz şeması; §3.4 teslimi | 31.01 (tablo); bölüm 14.02 | Kodi |
| Ö4 | Durum makinesi taslağı; Aşama-1/2/3 diyagramları; §4 Yöntem | 27.12; H10–H12; bölüm 14.02 | Kodi (+Sis metin desteği) |
| Ö5 | Malzeme listesi, bütçe, zaman planı | 14.02 | Sis |
| Ö7 | Taslak v1 birleştirme ve sayfa kontrolü; 2027 şablonuna uyarlama ve dondurma | 21.02; 05.03 | Sis |
| Ö8 | Hakem incelemesi ve kontrol listesi | H14 (22–28.02) | Konti |
| Ö9 | KYS yükleme (resmî son tarih tahmini 17.03, 17:00) | 08.03 | Kaptan |

Ocak sınav dönemi (H7–H9) hafif yükle planlandı; yarıyıl tatili (H10) yoğun haftadır.

## 5. Sık puan kaybettiren hatalar
- Takım şemasına isim yazmak (tablo değerlendirme dışı kalır).
- 10 sayfayı aşmak (rapor değerlendirilmez).
- Blok şemayı kablo bilgisi olmadan, yalnızca kutu ve okla çizmek.
- Bileşen tablolarında model ya da fiyatı boş bırakmak.
- Yöntem bölümünde üç aşamayı tek diyagramda toplamak ya da şartname kurallarını diyagrama koymamak.
- Kaynak göstermeden geçmiş rapordan cümle almak (aynı, benzer ya da kopya rapor diskalifiye sebebi).
- Aynı parçanın mekanik, donanım ve malzeme listesinde farklı adla ya da fiyatla geçmesi.

## 6. Proje takip aracı (§5 için)
Durum Tablosu v2 (iş paketleri, durumlar, onaylar) bir proje takip aracıdır ve ÖTR'de böyle anlatılabilir. İstenirse GitHub
Projects ya da Trello'ya taşınabilir; seçimi Sis önerir, kaptan onaylar. Raporda aracın adı, kullanımı ve bir ekran görüntüsü yer almalı.
