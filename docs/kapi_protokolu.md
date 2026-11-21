# Kapı Protokolü (beş ajan için aynı)

Kaynak: 01 Kurulum Paketi v2, §4.2 ve §5. v1 Drive'da Arşiv (v1 – 15.11.2026) klasöründedir.

1. **Durumlar:** AÇIK → ÇALIŞMADA → İNCELEMEDE → ONAYLI | ASKIDA. Yalnız Ö işlerinde ONAYLI yerine **ÖN SEÇİM**.
2. **Başlama kuralı:** KTR hattında girdi İP'si ONAYLI değilse iş başlamaz. ÖTR hattında girdi ÖN SEÇİM ya da ONAYLI olmalıdır.
3. **Onay:** Sahip ajan Teslim Notu yazar → Sis notu toplar, tabloya işler ve diğer departmanlarla çelişki var mı bakar →
   Konti bağımsız doğrular → kaptan onaylar.
4. **Değişiklik Talebi (DT):** ONAYLI çıktıyı değiştirmek için DT açılır; Sis etkilenen İP'leri listeler, Konti etki
   analizini doğrular, kaptan onaylar.
5. **Belirsizlik:** Bilinmeyen değer uydurulmaz; VARSAYIM etiketi alır. Şartname belirsizlikleri Sis'in Soru&Cevap listesine gider.
6. **Sayısal disiplin:** Her sayının birimi, kaynağı ve güven düzeyi yazılır.
7. **Bağımsızlık:** Konti'yi kullanan kişi kendi departmanının işini doğrulamaz. Konti hesabı kendi yöntemiyle tekrarlar;
   yalnızca "uygun görünüyor" diyerek onay vermez.
8. **Rol sınırı:** Sis tasarım kararı vermez; çelişkiyi bulur ve sahibine geri gönderir. Konti tasarım yapmaz ve rapor bölümü yazmaz.

## ÖN SEÇİM nedir
- ÖTR şablonu, motor ve kamera gibi parçaların model ve fiyatını ister. KTR hattında bu seçimler ancak M2 ve A1
  onaylanınca yapılır; ÖTR tarihine yetişmez.
- Bu yüzden Ö işleri **marjlı tahmin** ve **ön seçim** üretir. Konti'nin hızlı kontrolünden geçince durumu **ÖN SEÇİM** olur.
  Konti ön hesapları (kütle v0, tork, güç, piksel/menzil) kendi yöntemiyle tekrarlar; fark %10'u aşarsa sahibine geri gönderir.
- ÖN SEÇİM ÖTR'de kullanılabilir, ama KTR iş paketleri için **dondurulmuş değer değildir**. M1, M2, A1, A2 bu değerleri
  başlangıç tahmini olarak alır ve kapıdan geçirerek ONAYLI yapar.
- ÖTR'den KTR'ye değişen her seçim KTR'de "değişiklik ve gerekçe" olarak yazılır. Değişiklik hata değildir.

## Bağımsızlık: bu takımdaki atama
| Ajan | Kullanan / nerede | Çıktılarını Konti olarak kim doğrular |
|---|---|---|
| Meka | Sezen, Yusuf'un bilgisayarında | Yusuf (Konti). Yusuf'un içerik katkısı yaptığı kalem → Eren yanında |
| Avi | Sıla, kendi bilgisayarında | Yusuf (Konti). Yusuf'un EE olarak yardım ettiği kalem → Sezen veya Eren yanında |
| Kodi | Eren ve yazılım ekibi, kendi bilgisayarlarında | Yusuf (Konti) |
| Sis | Yusuf, kendi bilgisayarında | Yusuf'un Konti oturumunda, **Sezen veya Eren yanındayken ve onların onayıyla** |
| Konti | Yusuf, kendi bilgisayarında | – |

- Sis ve Konti'ye Yusuf dışında kimse erişmez. "Yanında doğrulama"da Konti'yi Yusuf çalıştırır; hesabı ve kontrol listesini
  Sezen veya Eren okur, karar onlarındır. Teslim Notu'nun "Doğrulayan" satırına **onların adı** yazılır.
- Yusuf'un yardım ettiği ya da katkı yaptığı kalemler, Teslim Notu'nun "Kararlar" bölümünde "(Yusuf katkısı)" diye işaretlenir.
- Yusuf hem Konti hem kaptan olduğu için doğrulama ile son onay çoğu işte aynı kişidedir. Bunu dengeleyen adım, Ö7 sonrası
  tüm takımın çapraz okumasıdır (Proje Planı H13); atlanmaz.
- T0 v1'i Yusuf yazdı ve onayladı. T0 v2'de (2027 şartnamesi) REQ listesi Sezen veya Eren yanında doğrulanır.

## Ajanların çalıştığı yer
- **Meka, Sis, Konti:** Yusuf'un bilgisayarında, bu deponun `.claude/agents/` tanımlarıyla (Claude Code). Sis ve Konti Drive
  bağlayıcısıyla Teslim Notlarını okur. Bulgularını önce sohbette Yusuf'a sunar; Drive'daki bir dosyaya yalnızca Yusuf
  onaylarsa ve yalnızca kendi kutusuna ("Sis kontrolü", "Konti doğrulaması") yazar.
- **Avi, Kodi:** ekiplerin kendi bilgisayarlarında, kendi Claude hesaplarında bir Claude Projesi olarak. Talimat metni Drive'daki
  "Ajan Talimatları (v2)" belgelerinden kopyalanır. Çıktılar Drive'a Teslim Notu olarak yüklenir.

## Serbest hazırlık hattı
Bilgi toplama, öğrenme, veri seti, alternatif araştırma her zaman serbesttir; karar ya da donmuş değer üretmez.

## ÖTR dönemi kuralları (Proje Planı v3)
ÖTR'ye kadar parça alınmaz, üretilmez, test edilmez. Seçimler katalog, veri sayfası ve hesapla yapılır. Fiyatlar kaynağı ve
tarihiyle yazılır. Balon çapı hesaplarda 20 cm (kötü durum VARSAYIM).

## Nerede tutulur (Drive)
| Ne | Drive | Dosya adı |
|---|---|---|
| İncelemedeki Teslim Notu | Departman klasörü (03_Mekanik, 04_Elektronik, 05_Yazılım, 06_Atış Modülü) | `<İP>_v<sürüm>_INCELEMEDE` |
| ÖN SEÇİM / ONAYLI Teslim Notu | Onaylı Teslim Notları | `<İP>_v<sürüm>_ONSECIM` / `<İP>_v<sürüm>_ONAYLI` |
| Değişiklik Talebi | Değişiklik Talepleri (DT) | `DT-<no>` |
| ICD | Arayüz (ICD) | `ICD_v<sürüm>` |
| İP durumları, REQ, DT kaydı | Durum Tablosu v2 (Sheets, 00_Yönetim) – Sis günceller, kaptan onaylar | – |
| Kararlar, varsayımlar, riskler, S&C | Semrük Ana Dosya | – |
| Tarihler, sayfa bütçesi | Semrük Proje Planı (T0 → ÖTR) | – |

Ajanlara (Claude Projelerine) yalnızca **ÖN SEÇİM** veya **ONAYLI** notları girdi olarak ver.
