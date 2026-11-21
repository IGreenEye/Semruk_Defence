# Kapı Protokolü (dört ajan için aynı)

Kaynak: 01_Kurulum_Paketi, Bölüm 4.

1. **Durumlar:** AÇIK → ÇALIŞMADA → İNCELEMEDE → ONAYLI | ASKIDA.
2. **Başlama kuralı:** Girdi İP'lerinden biri ONAYLI değilse İP başlamaz; ajan bunu açıkça söyler ve bekler.
3. **Onay:** Sahip ajan Teslim Notu yazar; Konti bağımsız doğrular (hesabı yeniden yapar, REQ izlenebilirliğine,
   varsayımlara bakar); son onay kullanıcıdadır (kaptan).
4. **Değişiklik Talebi (DT):** ONAYLI bir çıktıyı değiştirmek isteyen ajan DT yazar; Konti etki analizini yapıp
   hangi İP'lerin ASKIDA olacağını belirler; kullanıcı onaylar; etkilenen İP'ler kapıdan yeniden geçer.
5. **Belirsizlik:** Bilinmeyen değer uydurulmaz; `VARSAYIM` etiketiyle yazılır ve onaya kadar kapanmaz.
   Şartname belirsizlikleri `docs/soru_cevap.md` listesine gider.
6. **Sayısal disiplin:** Her sayının birimi, kaynağı (dosya/bölüm veya hesap) ve güven düzeyi yazılır.

## Serbest hazırlık hattı
Bilgi toplama, literatür, veri seti hazırlığı ve alternatif araştırma her zaman serbesttir; ancak karar, donmuş değer
veya sayı üretmez. İP yalnızca girdileri ONAYLI olunca ÇALIŞMADA olabilir.

## Teslim Notu (8 başlık)
İP kodu ve sürüm · Kullanılan onaylı girdiler · Çıktılar (sayı + birim + kaynak + güven) · Kararlar ve gerekçeleri ·
Varsayımlar · Riskler · Bağımlı İP'lere etkisi · KTR bölümüne katkı. Altında "Konti doğrulaması" ve "Kaptan onayı".
Şablon: `sablonlar/teslim_notu.md`.

## Dosya adlandırma
- İncelemedeki not: `teslim_notlari/<İP>_v<sürüm>_INCELEMEDE.md`
- Onaylı not: `teslim_notlari/onayli/<İP>_v<sürüm>_ONAYLI.md` (örn. `M1_v1_ONAYLI.md`)
- DT: `dt/DT-<no>.md`
- Ajanlara (veya Claude Projelerine) yalnızca ONAYLI dosyaları girdi olarak ver.
