# 📡 SDX Kanal Editör

**SatcoDX (`.sdx`) uydu kanal listesi dosyaları için tarayıcıda çalışan, kurulum gerektirmeyen kanal listesi editörü.**

Televizyonunuzun USB'ye çıkardığı `.sdx` kanal listesini açın; kanalları sıralayın, adlarını düzenleyin, boş kanal ekleyin, silin ve kaydedip TV'ye geri yükleyin. İsterseniz bir **kanal listesi** (istediğiniz sıra) ve bir **frekans listesi** (uydudaki kanalların teknik bilgileri) vererek bütün listeyi tek tıkla otomatik olarak sıralatın.

> **Tek bir HTML dosyası.** İndirin, çift tıklayın, çalışsın. İnternet gerekmez; dosyanız hiçbir yere gönderilmez, her şey tarayıcınızda olur.

🔗 **Hemen deneyin (kurulum yok):** https://yusufkilinc44.github.io/SDX-Kanal-Editor/  
⬇️ **İndirin:** [Son sürüm (Releases)](../../releases/latest) ya da [`index.html`](index.html) dosyasını indirip tarayıcıda açın.

🇬🇧 *English summary at the bottom.*

---

## ✨ Özellikler

**Editör**
- `.sdx` dosyasını açma, kaydetme (bayt bayt aynı biçimde; kayıt uzunluğu ve dosya sonu bloğu korunur)
- Kanalları taşıma (▲ ▼), alan alan düzenleme (✎), altına boş kanal ekleme (＋), kaydı boş kanalla ezme (⊘), silme (✕)
- **Toplu seçim ve silme:** Ctrl + tık, Shift + tık, Ctrl + A
- **Bul / Değiştir:** tüm kanal adlarında, büyük-küçük harf duyarlı ya da değil
- **Büyük / küçük harf:** HEPSİ BÜYÜK ya da Kelimelerin İlk Harfi Büyük (Türkçe kurallarıyla)
- Her alana göre **filtre** (frekans, SID, ONID, şifreli, tip…), boş kanalları gizleme
- Kayıt üzerinde renkli alan haritası ve kanal detay penceresi
- **Dosya kontrolü:** bozuk / tutarsız kayıtları bulur, düzeltme önerir
- Türkçe karakterler (İ, Ş, Ğ, ı…) TV'nin kendi kodlamasıyla doğru okunur ve yazılır
- **Kanal Listesi İndir:** bütün kayıtları tüm alanlarıyla biçimli bir Excel'e aktarır

**Otomatik eşleştirme (isteğe bağlı)**
- **📋 Kanal listesi** (Excel / CSV / TXT; `Kanal No` + `Kanal Adı`): kanallar bu sıraya dizilir, adlar bu listeden alınır
- **📡 Frekans listesi** (Excel): kanallar DVB kimliğiyle (ONID + TSID + SID) ya da frekans + polarizasyon + SID ile tanınır
  - adı olmayan kayıtlara ad yazılır
  - eksik Video / Ses / PCR PID'leri doldurulur
  - kanal listesinde isteyip dosyanızda olmayan kanallar **yeni kayıt olarak eklenir**
- Akıllı ad eşleştirme: HD / SD / TV ekleri, ülke ekleri (*ATV ↔ ATV Türkiye*), numaralı kayıtlar (*Ulusal TV ↔ ULUSAL 1 TV*), Türkçe karakter farkları
- Belirsiz eşleşmeleri tek tek onaylama, sonucu rozetlerle görme, Geri al
- **SDX + iki Excel'i tek seferde açma**
- Listeleri hazırlamak için örnek bir yapay zekâ prompt'u sayfanın içinde (zorunlu değil; listeleri elle de hazırlayabilirsiniz)

**Format rehberi**
- SatcoDX kayıt yapısı, alan haritası (ofset / sütun / uzunluk), ONID değerleri ve hangi anakartın hangi sürümü kullandığı

---

## 📺 Desteklenen dosyalar

| Sürüm | Kayıt | Kullanan anakartlar (17MB serisi) |
|---|---|---|
| `SATCODX103` | 127 karakter | MB45, MB62, **MB82** *(test edildi)*, MB95, MB96, MB97 |
| `SATCODX105` | 132 (bazen 127) karakter | MB110, MB120, MB130, MB140, MB211, MB180E, MB181TC |

Bu anakartlar Vestel üretimi TV'lerde ve aynı altyapıyı kullanan markalarda (Regal, SEG, Finlux, Hi-Level, Toshiba, JVC, Telefunken, Hitachi, Panasonic'in bazı modelleri…) bulunur. Kanal listesini USB'ye `.sdx` olarak dışa aktaran TV'lerin dosyaları açılabilir. Anakart listesi internet kaynaklarına dayanır; dosyanızın ilk satırı `SATCODX` ile başlıyorsa editör onu okuyabilir.

---

## 🚀 Kullanım

1. TV menüsünden kanal listesini USB belleğe aktarın (genellikle *Ayarlar → Uydu Ayarları → Kanal Tablosu / SatcoDX → USB'ye aktar*).
2. `index.html` dosyasını Chrome, Edge ya da Firefox ile açın.
3. **📂 SDX Dosyası Aç** ile `.sdx` dosyanızı açın.
4. Kanalları düzenleyin, isterseniz **📋 Kanal Listesi Aç** / **📡 Frekans Listesi Aç** ile eşleştirin.
5. **💾 SDX Kaydet** ile kaydedin, dosyayı USB'den TV'ye geri yükleyin.

> ⚠️ Başlamadan önce TV'nin çıkardığı ilk dosyanın bir **yedeğini** saklayın.

Chrome / Edge'de pencereler son kullandığınız klasörde açılır ve dosya aynı yere kaydedilebilir. Diğer tarayıcılarda dosya "İndirilenler" klasörüne iner.

---

## ❓ Sık sorulanlar

**Kurulum gerekiyor mu?** Hayır. Tek bir HTML dosyası; başka dosya, sunucu ya da internet bağlantısı gerekmez.

**Verilerim bir yere gönderiliyor mu?** Hayır. Dosyalar yalnızca tarayıcınızda okunur ve işlenir.

**Kanal listesi / frekans listesi zorunlu mu?** Hayır. Editör yalnız SDX dosyasıyla da çalışır. Listeler otomatik sıralama ve eşleştirme içindir; biçimlerine uyduğu sürece istediğiniz yolla hazırlayabilirsiniz (sayfadaki şablonları kullanın).

**Hangi platformlar için?** Hepsi: TKGS, D-Smart, Digiturk, Tivibu… Sayfadaki örnek prompt D-Smart'ı örnek alır; başka bir platformun sayfasını vermeniz yeterli.

---

## ⚖️ Sorumluluk reddi

SatcoDX biçiminin herkese açık resmi bir şartnamesi yoktur; editör gerçek dosyaların incelenmesiyle geliştirilmiştir. Yazılım "olduğu gibi" sunulur. TV'nize yüklemeden önce mutlaka yedek alın. Vestel ve diğer marka adları sahiplerine aittir; bu proje onlarla bağlantılı değildir.

---

## 👤 Geliştirici

**Yusuf Kılınç** · Ekim 2026 · [yusuf.kilinc@hotmail.com](mailto:yusuf.kilinc@hotmail.com)

Beğendiyseniz depoya ⭐ vermeyi unutmayın; öneri ve hata bildirimleri için [Issues](../../issues) bölümünü kullanabilirsiniz.

---

## 🇬🇧 English

**SDX Kanal Editör** is a free, single-file, browser-based editor for **SatcoDX (`.sdx`) satellite channel lists**, the format exported to USB by TVs built on Vestel 17MB chassis (sold under brands such as Vestel, Regal, SEG, Finlux, Hi-Level, Toshiba, JVC, Telefunken, Hitachi and some Panasonic models).

- **Try it online:** https://yusufkilinc44.github.io/SDX-Kanal-Editor/ — or download [`index.html`](index.html) and open it in Chrome / Edge / Firefox. No install, no server, works offline; your file never leaves your browser.
- **Edit:** reorder (move up/down), rename, insert / overwrite blank channels, delete (also multi-select), find & replace, upper / title case, per-field filters, field-by-field record editor, file health check. Saves byte-for-byte in the same format (`SATCODX103` 127-char and `SATCODX105` 132-char records, trailing NUL block preserved).
- **Auto-sort (optional):** give a *channel list* (number + name, Excel/CSV/TXT) and/or a *frequency list* (Excel); channels are matched by DVB identity (ONID + TSID + SID) or frequency + polarisation + SID, unnamed records get names, missing PIDs are filled and channels missing from your file can be added.
- **Export:** the whole list to a formatted Excel workbook.
- The user interface is in Turkish. Tested with MB82 (`SATCODX103`) files. Always keep a backup of the original file exported by your TV.

Author: **Yusuf Kılınç** · [yusuf.kilinc@hotmail.com](mailto:yusuf.kilinc@hotmail.com) · If you find it useful, please give the repo a ⭐
