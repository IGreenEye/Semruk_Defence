# İP Durum Tablosu

Canlı kaynak Google Sheets'teki **Çelikkubbe Proje Defteri – İP Durum Tablosu**'dur; bu dosya onun Git'teki kopyasıdır.
Durumu değiştirdiğinde ikisini birlikte güncelle ve commit mesajına İP kodunu yaz (örn. `M1: ÇALIŞMADA → İNCELEMEDE`).
"Başlayabilir mi?" = girdi İP'lerinin hepsi ONAYLI ise EVET.

Son güncelleme: 2026-11-21 (Drive'daki 04_Durum_Tablosu.pdf'ten)

| İP | Ajan | Girdiler | Durum | Başlayabilir mi? | Sorumlu | Onay tarihi | Onaylayan | Not |
|---|---|---|---|---|---|---|---|---|
| T0 | Konti | – | ONAYLI | EVET | Yusuf | _girilecek_ | Yusuf | ≤60 cm kararı onaylandı |
| M1 | Meka | T0 | ÇALIŞMADA | EVET | Güneş | | | |
| M2 | Meka | M1 | AÇIK | HAYIR | Güneş | | | |
| A1 | Avi | M2 | AÇIK | HAYIR | Sıla | | | |
| A2 | Avi | A1 | AÇIK | HAYIR | Sıla | | | |
| M3 | Meka | A2 | AÇIK | HAYIR | Güneş | | | |
| Y1 | Kodi | A2 | AÇIK | HAYIR | Eren | | | Veri seti ve model araştırması serbest hazırlık hattı |
| Y3 | Kodi | A2 | AÇIK | HAYIR | Eren | | | |
| Y2 | Kodi | Y1, M2, A2 | AÇIK | HAYIR | Eren | | | Önce simülasyon; donanım ayarı M4 sonrası |
| Y4 | Kodi | Y2, Y3 | AÇIK | HAYIR | Eren | | | |
| M4 | Meka | M3 | AÇIK | HAYIR | Güneş | | | |
| T1 | Konti | M4, Y4 | AÇIK | HAYIR | Yusuf | | | |
| T2 | Konti | T1 | AÇIK | HAYIR | Yusuf | | | |
| T3 | Konti | T2 | AÇIK | HAYIR | Yusuf | | | |
| T4 | Konti | T3 | AÇIK | HAYIR | Yusuf | | | |

## Değişiklik Talebi (DT) kaydı

| DT no | Tarih | İsteyen | Değişen İP | Ne değişiyor ve neden | Etkilenen İP'ler (Konti) | Karar | Karar tarihi |
|---|---|---|---|---|---|---|---|
| _ÖRNEK-DT-01_ | 01.01.2027 | Güneş | M2 | Pitch ekseni kütlesi 1,2 kg → 1,6 kg; kamera montajı büyüdü | A1, A2, Y2 | BEKLİYOR | |
