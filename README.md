# Semrük Defence – Çelikkubbe Proje Ajanları

TEKNOFEST Çelikkubbe Hava Savunma Sistemleri Yarışması (2027) için beş mühendislik ajanı (Meka, Avi, Kodi, Sis, Konti),
kapı protokolü, ÖTR rehberi, gereksinimler, şablonlar ve öğrenme rehberleri. Kurulum Paketi v2.1'e ve ÖTR kapsam kuralına göredir.
**Şimdiki hedef: ÖTR (Ö0–Ö9).**

## Ne nerede?
| Depo (GitHub) – kurallar, PR ile değişir | Drive – güncel durum, herkes düzenler |
|---|---|
| Beş ajanın tanımı, ortak talimat | Durum Tablosu v2: İP durumları, DT kaydı |
| Kapı protokolü, bağımlılık haritası | Semrük Ana Dosya: kararlar, varsayımlar, riskler, S&C |
| ÖTR rehberi | Semrük Proje Planı: tarihler, sayfa bütçesi |
| R01–R18 (onaylı taban çizgisi kopyası) | Teslim Notları, DT'ler, ICD |
| Teslim Notu / DT şablonları, örnekler | Şartname, ÖTR/KTR şablonları, parkur çizimi |
| Öğrenme rehberleri (v2.1) | Öğrenme kanıtları, CAD, rapor taslakları |

Drive'daki **Ajan Talimatları** klasöründeki belgeler, öğrenme rehberleri, şablonlar, Kurulum Paketi ve ÖTR Yol Haritası bu
depodaki dosyalardan üretilir; **ana kaynak bu depodur.** Bir kural değişirse önce burada (PR) değiştirin, sonra Drive'daki
belgeyi ve ilgili Claude Projesi'ni güncelleyin.

## Klasör yapısı
```
CLAUDE.md                   Ortak talimat (Claude Code otomatik okur)
.claude/agents/             meka.md, avi.md, kodi.md, sis.md, konti.md
.github/                    PR şablonu
docs/
  otr_rehberi.md            ÖTR bölüm planı, dikkat edilecekler, biçim kontrol listesi, geri sayım
  kapi_protokolu.md         Durumlar, ÖN SEÇİM, bağımsızlık ataması, Drive'da dosya yerleri
  bagimlilik_haritasi.md    ÖTR hattı (T0, Ö0–Ö9)
  gereksinimler.md          R01–R18
  teslim_raporu_rehberi.md  Örnek Teslim Notları
sablonlar/                  teslim_notu.md, degisiklik_talebi.md
ogrenme/                    10_meka, 11_avi, 12_kodi, 13_konti, 14_sis
kaynaklar/                  (yerel, Git'e girmez) Drive'dan indirilen şartname ve şablonlar
```

## Ajanlar nerede çalışır
| Ajan | Nerede | Nasıl kurulur |
|---|---|---|
| Meka, Sis, Konti | Yusuf'un bilgisayarı (Meka'yı Sezen birlikte kullanır) | Bu depoda `claude` çalıştır; ajanlar `.claude/agents/` klasöründen gelir. Sis ve Konti Drive bağlayıcısıyla Teslim Notlarını okur. |
| Avi | Sıla'nın bilgisayarı | Sıla'nın Claude hesabında bir Claude Projesi; talimat Drive'daki "Talimat – Avi (v2.1)" belgesinden |
| Kodi | Eren ve ekibinin bilgisayarları | Kendi Claude hesaplarında bir Claude Projesi; talimat "Talimat – Kodi (v2.1)" belgesinden |

Claude Projesi kurulumu: proje talimatına ilgili talimat belgesinin tamamını yapıştır; proje dosyalarına şartname, parkur çizimi,
KTR şablonu ve ÖTR şablonunu ekle; girdi olarak yalnızca **ÖN SEÇİM / ONAYLI** Teslim Notlarını ver.

Yusuf'un bilgisayarında kullanım örnekleri:
- `sis ajanı: 03_Mekanik klasöründeki Ö1 Teslim Notu'nu oku, eksik alanları ve Avi'nin notuyla çelişkileri listele`
- `konti ajanı: Ö2 Teslim Notu'ndaki tork ve güç hesabını kendi yönteminle tekrarla`
- `meka ajanı: Sezen ile konu 5'i (parkur geometrisinden açı hesabı) çalışıyoruz; önce kavramı anlat`

İsteğe bağlı: şartname ve şablonların yerel kopyası için `kaynaklar/` klasörüne indir (Git'e girmez).

## Depoda değişiklik yapma
`main` korumalıdır; her değişiklik dal + Pull Request ile gelir ve bir onay ister.
```
git switch main; git pull
git switch -c <konu>
git add -A ; git commit -m "..." ; git push -u origin <konu>
```
