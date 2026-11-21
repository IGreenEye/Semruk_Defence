# Öğrenme Rehberi – Sis (Sistem Mühendisliği, Plan ve Rapor) · v1

Kullanan: **Yusuf Köse (kaptan)** · Kaynak: Drive "14 Öğrenme Rehberi – Sis (yeni)"

**Bu rehber yeni:** Sis, Kurulum Paketi v2 ile eklenen beşinci ajandır. Konti'den gereksinim yazımı, yaşam döngüsü, arayüz
yönetimi, proje yönetimi, puan stratejisi, operasyon planı ve rapor yazımı Sis'e geçti.

**Amaç:** Gereksinimleri yönetmek, departmanların çıktılarını tutarlı tutmak, malzeme listesi-bütçe-takvimi yürütmek ve ÖTR/KTR'yi
şablona tam uygun derlemek. Sis **tasarım kararı vermez**: çelişkiyi ve boşluğu bulur, sahibine geri verir.

## 0. ÖTR'de senden istenen (Ö0, Ö5, Ö7)
Sis ÖTR'de yaklaşık **2,1 sayfa** içerik yazar, kapak ve içindekileri hazırlar ve raporu derler
(iskelet 06.12, taslak v1 21.02, dondurma 05.03, yükleme 08.03).
- **Ö0 – ÖTR planı:** bölüm sahipleri, sayfa bütçesi, iç teslim tarihleri; takım şeması taslağı (kişisel veri yok).
- **Ö5 – Malzeme listesi, bütçe, zaman planı:** Meka, Avi, Kodi tablolarından toplu liste; fiyat kaynaklı; Gantt; proje takip aracı.
- **Ö7 – Derleme:** proje özeti (en son), kaynakça, biçim kuralları, 10 sayfaya sığdırma, bölümler arası tutarlılık.
- Doğrudan yazılan bölümlerin puanı: Özet 5 + Malzeme listesi 5 + Zaman-bütçe 5 + Rapor düzeni 5 = **20 puan**. Biçim hatası
  tüm raporu değerlendirme dışı bırakabilir; bu yük de Sis'tedir.

## 1. Öğrenme listesi
Öncelik: **Ö** = ÖTR'den önce · **A** = KTR hattının ilk kapılarından önce · **B** = KTR yazımından önce · **C** = video ve yarış hazırlığı

| # | Konu | Öncelik | Neden | Yapabildiğini nasıl anlarsın | ✓ |
|---|---|---|---|---|---|
| 1 | Gereksinim mühendisliği: ölçülebilir, test edilebilir gereksinim; izlenebilirlik matrisi | **Ö** | T0 bakımı; R16–R18 | Bir gereksinimi ölçülebilir hâle getirir, İP'ye ve teste bağlarsın | [ ] |
| 2 | Sistem yaşam döngüsü: V modeli; ÖTR ön tasarım, KTR kritik tasarım incelemesi | **Ö** | ÖTR ve KTR hatlarının mantığı | ÖN SEÇİM ile ONAYLI farkını ve ÖTR→KTR değişikliğinin nasıl anlatılacağını açıklarsın | [ ] |
| 3 | Arayüz yönetimi: sistem blok şeması, ICD, aynı parçanın her belgede aynı adla geçmesi | **Ö** | Ö7: tutarlılık; A2: ICD | Blok şema, donanım tablosu ve yazılım arayüz şeması arasında 3 çelişki bulursun | [ ] |
| 4 | Teknik rapor yazımı: şablon disiplini, akademik dil, tekrarsız anlatım, sayfa ekonomisi, şekil/tablo numaralama | **Ö** | Ö7; R16 | 1 sayfalık bölümü anlamı kaybetmeden 3/4 sayfaya indirirsin | [ ] |
| 5 | Kaynak gösterme ve alıntı: dijital/basılı format, geçmiş rapor alıntı formatı, kaynak yönetim aracı | **Ö** | ÖTR §6; diskalifiye riski | 10 kaynağı şablondaki formatla eksiksiz yazarsın | [ ] |
| 6 | Kişisel veri ve takım şeması: rol tabanlı tablo | **Ö** | R17 | Takım şemasını isimsiz, görev-eğitim-sınıf-rol ile doldurursun | [ ] |
| 7 | Malzeme listesi (BOM) ve maliyet: parça kimliği, adet, birim fiyat, kaynak ve tarih, kur, kargo ve vergi, beklenmeyen gider payı | **Ö** | Ö5: ÖTR §3.5 ve §5 | Üç departmanın tablolarından tek BOM çıkarır, toplamı bütçe varsayımıyla karşılaştırırsın | [ ] |
| 8 | Zaman planlama: WBS, Gantt, kritik yol, kilometre taşı | **Ö** | Ö5: ÖTR §5 | ÖTR ve KTR'ye kadar olan Gantt'ı kritik yoluyla çizersin | [ ] |
| 9 | Proje takip aracı: Durum Tablosu (Sheets), isteğe bağlı GitHub Projects/Trello; raporda anlatımı | **Ö** | ÖTR §5 | Aracı bir paragraf ve bir ekran görüntüsüyle anlatırsın | [ ] |
| 10 | Soru&Cevap yönetimi: madde numarasıyla soru yazma; cevabı REQ'e işleme | **Ö** | Belirsizlik yönetimi | Bir belirsizliği cevaplanabilir biçimde ve madde numarasıyla soruya çevirirsin | [ ] |
| 11 | Tedarik: teslim süresi, alternatif tedarikçi, ithalat riski; sponsor ve TEKNOFEST destek takvimi | A | Ö5 sonrası satın alma; KTR bütçesi | Uzun teslim süreli 5 parçayı ve sipariş son tarihlerini listelersin | [ ] |
| 12 | Değişiklik ve konfigürasyon yönetimi: DT akışı, sürüm numaraları, geçerli belge | A | DT süreci | Bir DT'nin etkilediği İP'leri listeler, tabloyu günceller, Konti'ye doğrulatırsın | [ ] |
| 13 | Risk kaydı: olasılık × etki, azaltma, risk sahibi | A | KTR Zaman-Bütçe-Risk | İlk 10 riski puanlayıp azaltma önlemleriyle yazarsın | [ ] |
| 14 | Toplantı ve karar kaydı: gündem, karar, sorumlu, tarih | A | Kapı onayları | Bir toplantının kararlarını tek sayfada kaydedersin | [ ] |
| 15 | Puan stratejisi: aşama ve baraj puanları, beklenen puan tablosu | B | KTR, T4 | Aşama-1/2/3 için beklenen puanı isabet olasılığına göre hesaplarsın | [ ] |
| 16 | Video ve yarış günü planı: 7 yetenek senaryosu, 30 dk hazırlık, 10 dk bakım, rol kartları | C | R13, R14; T3–T4 (Konti prova eder) | Yarış günü zaman çizelgesini ve rol kartlarını hazırlarsın | [ ] |

## 2. 3 haftalık plan (Ö0 ve Ö5 hazırlığı)
- **Hafta 1:** konu 1, 2, 6, 10 → REQ listesine R16–R18 işlenmiş; takım şeması taslağı; Soru&Cevap listesi (ÖTR şablonundaki puan çelişkisi dahil).
- **Hafta 2:** konu 4, 5, 8, 9 → Ö0 ÖTR planı; Word/LibreOffice şablon dosyası (Arial 12, Arial Black 14, 1,15, kenar boşlukları); Gantt v0.
- **Hafta 3:** konu 3, 7, 11 → BOM şablonu (sütunlar, fiyat kaynağı, tarih); tutarlılık kontrol listesi; uzun teslim süreli parça listesi.

## 3. Kaynaklar
**Kitaplar:** *NASA Systems Engineering Handbook* (NASA/SP-2016-6105) · *INCOSE Systems Engineering Handbook* ·
Blanchard & Fabrycky, *Systems Engineering and Analysis* · Wiegers & Beatty, *Software Requirements* · PMI, *PMBOK Guide* ·
Kerzner, *Project Management: A Systems Approach to Planning, Scheduling, and Controlling*

**Standartlar ve mevzuat:** ISO/IEC/IEEE 29148 · ISO/IEC/IEEE 15288 · ISO 21502 · ISO 10007 · 6698 sayılı KVKK
(takım şemasındaki kişisel veri yasağının arka planı)

**Ders:** MIT OCW, edX/Coursera sistem mühendisliği ve proje yönetimi · NASA ve INCOSE materyalleri · Zotero dokümantasyonu

**Yarışma (birincil):** ÖTR şablonu (bölüm yapısı, puanlar, "Rapor taslakları ile ilgili not") · KTR şablonu · Şartname §2
(takvim, rapor süreci, Soru&Cevap kuralları), §6 · TEKNOFEST Genel Kurallar ve Etik Kurallar · Soru&Cevap grubu

**Araçlar:** Google Sheets (Durum Tablosu, REQ, BOM), GanttProject / ProjectLibre, draw.io, Zotero, Word/LibreOffice stil şablonu, PDF karşılaştırma

## 4. Ajanla çalışma
- Teslim Notlarını Sis'e ver: "bu notları karşılaştır, aynı parçanın farklı ad, sayı ya da fiyatla geçtiği yerleri listele."
- Sis **teknik boşluğu doldurmaz**; eksik tork değeri ya da kamera özelliğini sahibine soru olarak geri verir.
- Kısaltırken: "anlamı değiştirmeden kısalt; hangi cümleyi çıkardığını göster"; teknik içerik için sahibinin onayını al.
- Kendi yazdığın bölümleri (özet, takım şeması, malzeme listesi, zaman-bütçe) Konti'de **Sezen veya Eren yanındayken** incelet.
