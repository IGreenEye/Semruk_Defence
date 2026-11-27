# Kapı Protokolü (beş ajan için aynı)

Kaynak: 01 Kurulum Paketi v2.1. Kapsam: yalnızca ÖTR dönemi.

1. **Durumlar:** AÇIK → ÇALIŞMADA → İNCELEMEDE → ÖN SEÇİM (Ö işleri) veya ONAYLI (T0, M1) | ASKIDA.
2. **Başlama kuralı:** Girdi İP'si ÖN SEÇİM ya da ONAYLI değilse iş başlamaz.
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
- ÖTR şablonu, motor ve kamera gibi parçaların model ve fiyatını ister. Bu seçimler ÖTR'de test ve ölçüm olmadan, katalog,
  veri sayfası ve hesapla yapılır.
- Bu yüzden Ö işleri **marjlı tahmin** ve **ön seçim** üretir. Konti'nin kontrolünden geçince durumu **ÖN SEÇİM** olur.
  Konti ön hesapları (kütle v0, tork, güç, piksel/menzil) kendi yöntemiyle tekrarlar; fark %10'u aşarsa sahibine geri gönderir.
- ÖN SEÇİM ÖTR'de kullanılır, ama **dondurulmuş değer değildir**. ÖTR'den sonra ayrı plan kapsamında yeniden ele alınır;
  değişiklik hata sayılmaz.

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
  "Ajan Talimatları" belgelerinden kopyalanır. Çıktılar Drive'a Teslim Notu olarak yüklenir.

## Serbest hazırlık hattı
Bilgi toplama, öğrenme, veri seti, alternatif araştırma her zaman serbesttir; karar ya da donmuş değer üretmez.

## Kapsam kuralı (kaptan kararı, 21.11.2026; Proje Planı v4)
ÖTR dönemine yalnızca ÖTR şablonuna veya şartname kurallarına bağlanan işler girer. ÖTR'ye kadar parça alımı, üretim, maket,
test ve ölçüm, kod geliştirme, KTR ve video hazırlığı, test parkuru ve simülatör yoktur. Seçimler katalog, veri sayfası ve
hesapla yapılır; fiyatlar kaynağı ve tarihiyle yazılır. Balon çapı hesaplarda 20 cm (kötü durum VARSAYIM).

## Nerede tutulur (Drive)
| Ne | Drive | Dosya adı |
|---|---|---|
| İncelemedeki Teslim Notu | Departman klasörü (03_Mekanik, 04_Elektronik, 05_Yazılım, 06_Atış Modülü) | `<İP>_v<sürüm>_INCELEMEDE` |
| ÖN SEÇİM / ONAYLI Teslim Notu | Onaylı Teslim Notları | `<İP>_v<sürüm>_ONSECIM` / `<İP>_v<sürüm>_ONAYLI` |
| Değişiklik Talebi | Değişiklik Talepleri (DT) | `DT-<no>` |
| ICD | Arayüz (ICD) | `ICD_v<sürüm>` |
| İP durumları, REQ, DT kaydı | Durum Tablosu v3 (Google E-Tablo) (Sheets, 00_Yönetim) – Sis günceller, kaptan onaylar | – |
| Kararlar, varsayımlar, riskler, S&C | Semrük Ana Dosya | – |
| Tarihler, sayfa bütçesi | Semrük Proje Planı (T0 → ÖTR) | – |

Ajanlara (Claude Projelerine) yalnızca **ÖN SEÇİM** veya **ONAYLI** notları girdi olarak ver.
