# Çelikkubbe Proje Ajanları

TEKNOFEST 2026 Çelikkubbe Hava Savunma Sistemleri Yarışması için 4 mühendislik ajanı (Meka, Avi, Kodi, Konti),
kapı protokolü, gereksinimler, şablonlar ve öğrenme rehberleri.

## Klasör yapısı
```
CLAUDE.md                   Ortak talimat (Claude Code otomatik okur)
.claude/agents/             Ajan tanımları: meka.md, avi.md, kodi.md, konti.md
docs/                       Tek doğruluk kaynağı
  kapi_protokolu.md         Durumlar, onay, DT, VARSAYIM kuralları
  bagimlilik_haritasi.md    İP zinciri ve onay kriterleri
  durum_tablosu.md          Güncel İP durumları + DT kaydı
  gereksinimler.md          R01–R15
  soru_cevap.md             Şartname belirsizlikleri
  teslim_raporu_rehberi.md  Örnek Teslim Notları
sablonlar/                  teslim_notu.md, degisiklik_talebi.md
ogrenme/                    Departman öğrenme rehberleri (✓ sütunu ilerleme takibi için)
  kanitlar/<ajan>/          1 sayfalık çözülmüş örnekler
teslim_notlari/             İncelemedeki notlar
  onayli/                   <İP>_v<sürüm>_ONAYLI.md
dt/                         Değişiklik Talepleri
icd/                        Arayüz kontrol dokümanları
kaynaklar/                  Şartname, parkur çizimi, KTR şablonu (PDF)
```

## Kullanım 1 – Claude Code (önerilen)
1. Bu klasörde `claude` çalıştır. `CLAUDE.md` otomatik yüklenir, ajanlar `/agents` ile görünür.
2. Ajanı adıyla çağır:
   - `meka ajanını kullan: M1 için parkur geometrisinden yaw/pitch aralığını hesapla`
   - `konti ajanıyla teslim_notlari/M1_v1_INCELEMEDE.md dosyasını doğrula`
   - `avi ajanı: öğrenme rehberindeki konu 6'yı anlat, sonra benim e-stop şemamı kontrol et`
3. Önce `kaynaklar/` klasörüne şartname, parkur çizimi ve KTR şablonunu koy.

## Kullanım 2 – claude.ai Projeleri
Kurulum Paketi'ndeki yöntem: 4 ayrı Claude Projesi aç (Meka, Avi, Kodi, Konti).
- Proje talimatına ilgili `.claude/agents/<ajan>.md` dosyasının `---` satırlarının **altındaki** kısmını yapıştır.
- Proje dosyalarına ekle: şartname, parkur çizimi, KTR şablonu, `docs/` içindeki tüm .md dosyaları,
  ilgili `ogrenme/` rehberi ve yalnızca **ONAYLI** teslim notları.

## Akış
Sahip ajan Teslim Notu yazar → `teslim_notlari/` → Konti doğrular → kaptan onaylar →
dosya `teslim_notlari/onayli/` altına `_ONAYLI` adıyla taşınır → `docs/durum_tablosu.md` ve Google Sheets güncellenir.
