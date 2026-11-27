# Öğrenme Rehberi – Sis (Sistem Mühendisliği, Plan ve Rapor) · v1.1

Kullanan: **Yusuf Köse (kaptan)** · Kapsam: **yalnızca ÖTR** (Ö0, Ö5, Ö7 ve T0 v2)

**Amaç:** Gereksinimleri yönetmek, departmanların çıktılarını tutarlı tutmak, malzeme listesi-bütçe-takvimi yürütmek ve ÖTR'yi
şablona tam uygun derlemek. Sis **tasarım kararı vermez**: çelişkiyi ve boşluğu bulur, sahibine geri verir.

## 0. ÖTR'de senden istenen (Ö0, Ö5, Ö7)
Sis ÖTR'de yaklaşık **2,1 sayfa** içerik yazar, kapak ve içindekileri hazırlar ve raporu derler
(iskelet 06.12, takım şeması 13.12, taslak v1 21.02, dondurma 05.03, yükleme 08.03).
- **Ö0 – ÖTR planı:** bölüm sahipleri, sayfa bütçesi, iç teslim tarihleri; takım şeması taslağı (kişisel veri yok).
- **Ö5 – Malzeme listesi, bütçe, takvim metni:** Meka, Avi, Kodi tablolarından toplu liste; fiyat kaynaklı ve tarihli; ÖTR §5 tahmini takvim **yalnızca rapor metni**; proje takip aracı.
- **Ö7 – Derleme:** proje özeti (en son), kaynakça, biçim kuralları, 10 sayfaya sığdırma, bölümler arası tutarlılık.
- **T0 v2 (10.01):** 2027 şartnamesindeki farkları REQ listesine işle; Soru&Cevap sorularını madde numarasıyla hazırla.
- Doğrudan yazılan bölümler 20 puan; biçim hatası tüm raporu değerlendirme dışı bırakabilir. Kendi çıktıların Konti'de Sezen veya Eren yanında doğrulanır.

## 1. ÖTR için öğrenme listesi
| # | Konu | Neden | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|
| 1 | Gereksinim mühendisliği: ölçülebilir, test edilebilir gereksinim; izlenebilirlik | T0 v2; R16–R18 | Bir gereksinimi ölçülebilir hâle getirir, hangi Ö işine bağlandığını gösterirsin | [ ] |
| 2 | Ön tasarım incelemesi olarak ÖTR'nin yeri; ÖN SEÇİM mantığı | Ö hattının mantığı | ÖN SEÇİM ile ONAYLI farkını açıklarsın | [ ] |
| 3 | Arayüz tutarlılığı: blok şema, donanım tablosu, yazılım arayüz şeması; aynı parçanın her yerde aynı adla geçmesi | Ö7 | Üç belge arasındaki 3 çelişkiyi bulursun | [ ] |
| 4 | Teknik rapor yazımı: şablon disiplini, akademik dil, tekrarsız anlatım, sayfa ekonomisi, şekil/tablo numaralama | Ö7; R16 | 1 sayfalık bir bölümü anlamı kaybetmeden 3/4 sayfaya indirirsin | [ ] |
| 5 | Kaynak gösterme ve alıntı: şablondaki dijital/basılı format, geçmiş rapor alıntı formatı | ÖTR §6; Şart. §2.1 | 10 kaynağı şablon formatıyla eksiksiz yazarsın | [ ] |
| 6 | Kişisel veri ve takım şeması: rol tabanlı tablo | R17; Şart. §2.1 (3–15 kişi) | Takım şemasını isimsiz, görev-eğitim-sınıf-rol ile doldurursun | [ ] |
| 7 | Malzeme listesi (BOM) ve maliyet: parça kimliği, adet, birim fiyat, kaynak ve tarih, kur, kargo ve vergi payı | Ö5: ÖTR §3.5 ve §5 | Üç departmanın tablolarından tek BOM çıkarır, toplamı bütçe varsayımıyla karşılaştırırsın | [ ] |
| 8 | Zaman planlama: iş kırılımı, Gantt, kilometre taşı | Ö5: ÖTR §5 takvim metni | ÖTR §5'e girecek tahmini üretim ve test takvimini rapor metni olarak yazarsın | [ ] |
| 9 | Proje takip aracı: Durum Tablosu (Sheets); raporda anlatımı | ÖTR §5 | Aracı bir paragraf ve bir ekran görüntüsüyle anlatırsın | [ ] |
| 10 | Soru&Cevap yönetimi: şartname maddesine atıfla soru yazma; cevabı REQ'e işleme | Şart. §2.3.2 | Bir belirsizliği madde numarasıyla, cevaplanabilir bir soruya çevirirsin | [ ] |

## 2. 3 haftalık plan (Proje Planı H1–H3)
- **Hafta 1:** konu 1, 2, 6, 10 → takım şeması taslağı; Soru&Cevap listesi; iletişim sorumlusu ve teknofest.org grup üyeliği (Şart. §2.1, §2.3.1).
- **Hafta 2:** konu 4, 5, 8, 9 → Ö0 ÖTR iskeleti ve sayfa bütçesi (06.12); Word/LibreOffice şablon dosyası (Arial 12, Arial Black 14, 1,15, kenar boşlukları).
- **Hafta 3:** konu 3, 7 → BOM şablonu (sütunlar, fiyat kaynağı, tarih); tutarlılık kontrol listesi.

## 3. ÖTR sonrası (şimdilik kapsam dışı)
Tedarik ve sipariş takvimi · konfigürasyon yönetimi ayrıntısı · risk kaydı ve puan stratejisi · video ve yarış günü planı.
ÖTR'den sonra ayrı planla ele alınacak.

## 4. Kaynaklar
**Kitaplar:** *NASA Systems Engineering Handbook* · *INCOSE Systems Engineering Handbook* · Wiegers & Beatty, *Software Requirements* · PMI, *PMBOK Guide*
**Standartlar ve mevzuat:** ISO/IEC/IEEE 29148 · 6698 sayılı KVKK (takım şemasındaki kişisel veri yasağının arka planı)
**Yarışma (birincil):** ÖTR şablonu (bölüm yapısı, puanlar, "Rapor taslakları ile ilgili not") · Şartname §2 (takvim, rapor süreci,
Soru&Cevap kuralları) · TEKNOFEST Genel Kurallar ve Etik Kurallar · Soru&Cevap grubu
**Araçlar:** Google Sheets (Durum Tablosu, REQ, BOM), draw.io, Zotero, Word/LibreOffice stil şablonu, PDF karşılaştırma

## 5. Ajanla çalışma
- Teslim Notlarını Sis'e ver: "bu notları karşılaştır, aynı parçanın farklı ad, sayı ya da fiyatla geçtiği yerleri listele."
- Sis **teknik boşluğu doldurmaz**; eksik tork değeri ya da kamera özelliğini sahibine soru olarak geri verir.
- Kısaltırken: "anlamı değiştirmeden kısalt; hangi cümleyi çıkardığını göster"; teknik içerik için sahibinin onayını al.
- Kendi yazdığın bölümleri Konti'de **Sezen veya Eren yanındayken** incelet.
