# Advanced Cipher Tool / Gelişmiş Şifre Çözücü

**Version 1.0.0**

[English](#english) · [Türkçe](#türkçe)



## English

A lightweight tool for **encoding and decoding classical ciphers**, with extended Polybius variants and full Turkish-alphabet support. It is a single HTML file with no dependencies and works completely offline. A Windows desktop version is also available.

🌐 **Try it online:** https://kuzeykizilbayir.github.io/Advanced-Cipher-Tool/

### Features

* **Atbash** `!` — mirrors the alphabet (A↔Z, B↔Y…). The same operation encodes and decodes.
* **Caesar** `?S` — shift by S steps, with separate *Encode* (S forward) and *Decode* (S back) buttons.
* **Vigenère** `\\\&` — encode and decode with a keyword.
* **A1Z26** `%` — letters ↔ numbers. Use `-` between letters and a space between words (`HELLO` → `8-5-12-12-15`). Numbers above 26 are handled with modulo 26.
* **Auto-detection** — if the input is only numbers, A1Z26 decoding is applied automatically.
* **Polybius square** with four methods:

  * **Basic** `+` — letter ↔ coordinate (row-column), e.g. `S` → `43`.
  * **Method 1** `-` — Caesar-style shift by S rows (or columns) in the square.
  * **Method 2 – Bifid** `xS` — row and column coordinates are written separately, then recombined into pairs.
  * **Method 3 – Bifid + Shift** `½S` — Bifid followed by a left shift of S steps on the coordinate string.
* **Secret `ğ` modes (English Polybius)** — add `ğ` at the start of the text to change behaviour (swap coordinate order to (y,x), switch row/column shifting, or choose the stage in Method 3). Trailing `ğ` characters cancel leading ones. Details are in the in-app guide.
* **Turkish alphabet mode** 🇹🇷 — 29-letter alphabet for Atbash, Caesar, Vigenère, **A1Z29**, and **Polybius ver.:TR** (5×6 square).
* **Bilingual interface** — switch the UI and guides between English and Turkish with the 📖 EN/TR button.
* **Built-in guides** for every method.

### Usage

**In the browser**

1. Open `index.html` in any modern browser (no installation or internet connection needed).
2. Type or paste your text and press **Start**.
3. Pick a method, enter S / the keyword if needed, then press **Encode** or **Decode**.

### Technical notes

* Pure HTML/CSS/JavaScript, single file, no external libraries.
* English Polybius uses a 5×5 square where I and J share a cell (24): `ABCDE / FGHIK / LMNOP / QRSTU / VWXYZ`.
* Turkish Polybius uses a 5×6 square: `ABCÇDE / FGĞHIİ / JKLMNO / ÖPRSŞT / UÜVYZ·`.

### ⚠️ Disclaimer

These are **classical ciphers** made for learning, puzzles, and fun. They are **not secure** and must not be used to protect sensitive information.



## Türkçe

**Klasik şifreleme yöntemlerini oluşturmak ve çözmek** için hazırlanmış hafif bir araç. Genişletilmiş Polybius varyasyonları ve tam Türk alfabesi desteği içerir. Tek bir HTML dosyasından oluşur, hiçbir bağımlılığı yoktur ve tamamen internetsiz çalışır. Windows masaüstü sürümü de mevcuttur.

🌐 **Online dene:** https://kuzeykizilbayir.github.io/Advanced-Cipher-Tool/

### Özellikler

* **Atbash** `!` — alfabeyi aynalar (A↔Z, B↔Y…). Aynı işlem hem şifreler hem çözer.
* **Caesar** `?S` — S adım kaydırma; *Oluştur* (S ileri) ve *Çöz* (S geri) için ayrı butonlar.
* **Vigenère** `\\\&` — anahtar kelime ile oluşturma ve çözme.
* **A1Z26** `%` — harf ↔ sayı. Harfler arasında `-`, kelimeler arasında boşluk kullanılır (`HELLO` → `8-5-12-12-15`). 26'dan büyük sayılar modulo 26 ile işlenir.
* **Otomatik algılama** — girilen metin yalnızca sayılardan oluşuyorsa A1Z26 çözümü otomatik uygulanır.
* **Polybius karesi**, dört yöntemle:

  * **Temel** `+` — harf ↔ koordinat (satır-sütun), örn. `S` → `43`.
  * **Yöntem 1** `-` — karede S satır (veya sütun) Caesar tarzı kaydırma.
  * **Yöntem 2 – Bifid** `xS` — satır ve sütun koordinatları ayrı yazılır, sonra ikili gruplar halinde yeniden birleştirilir.
  * **Yöntem 3 – Bifid + Kaydırma** `½S` — Bifid sonrası koordinat dizisinin S adım sola kaydırılması.
* **Gizli `ğ` modları (İngilizce Polybius)** — metnin başına `ğ` eklemek davranışı değiştirir (koordinat sırası (y,x) olur, satır/sütun kaydırma değişir, Yöntem 3'te aşama seçilir). Sondaki `ğ` harfleri baştakileri iptal eder. Ayrıntılar uygulama içi rehberde.
* **Türkçe alfabe modu** 🇹🇷 — Atbash, Caesar, Vigenère, **A1Z29** ve **Polybius ver.:TR** (5×6 kare) için 29 harfli alfabe.
* **İki dilli arayüz** — arayüzü ve rehberleri 📖 EN/TR butonuyla İngilizce ile Türkçe arasında değiştirebilirsin.
* Her yöntem için **yerleşik rehber**.

### Kullanım

**Tarayıcıda**

1. `index.html` dosyasını herhangi bir modern tarayıcıda aç (kurulum veya internet gerekmez).
2. Metni yaz veya yapıştır, **Başla**'ya bas.
3. Bir yöntem seç, gerekirse S değerini / anahtar kelimeyi gir, ardından **Oluştur** veya **Çöz**'e bas.

### Teknik notlar

* Saf HTML/CSS/JavaScript, tek dosya, harici kütüphane yok.
* İngilizce Polybius, I ve J'nin aynı hücreyi (24) paylaştığı 5×5 kare kullanır: `ABCDE / FGHIK / LMNOP / QRSTU / VWXYZ`.
* Türkçe Polybius 5×6 kare kullanır: `ABCÇDE / FGĞHIİ / JKLMNO / ÖPRSŞT / UÜVYZ·`.

### ⚠️ Uyarı

Bunlar öğrenme, bulmaca ve eğlence amaçlı **klasik şifrelerdir**. **Güvenli değildir**; hassas bilgileri korumak için kullanılmamalıdır.

