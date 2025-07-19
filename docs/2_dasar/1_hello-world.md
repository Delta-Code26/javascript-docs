# 👋 Hello, World!

Mari kita mulai perjalanan kita dalam dunia JavaScript dengan sesuatu yang klasik: mencetak **Hello, World!** ke layar.

---

## 📌 Tujuan

- Memahami cara menjalankan kode JavaScript
- Mengenal console dan cara interaksi dengan output
- Menjalankan JavaScript di browser dan juga Node.js

---

## 🖥 Menjalankan JavaScript di Browser

Buka browser favoritmu (Chrome, Firefox, Edge), lalu tekan `F12` untuk membuka **Developer Tools**, lalu pilih tab **Console**.

Ketikkan kode berikut:

```javascript
console.log("Hello, World!");
````

Lalu tekan `Enter`.

> 💡 `console.log()` adalah cara paling umum untuk menampilkan output di JavaScript.

---

## 🌐 Menyisipkan JavaScript di HTML

Buat file HTML seperti berikut:

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Hello JavaScript</title>
</head>
<body>
  <h1>Belajar JavaScript</h1>

  <script>
    console.log("Hello dari file HTML!");
    alert("Halo Dunia!");
  </script>
</body>
</html>
```

Saat file dibuka di browser, kamu akan melihat:

* Pesan pop-up dari `alert()`
* Output `console.log()` muncul di console (Developer Tools)

---

## ⚙️ Menjalankan JavaScript di Node.js

Jika kamu menggunakan **Node.js**, simpan kode berikut di file `hello.js`:

```javascript
console.log("Hello dari Node.js!");
```

Lalu jalankan di terminal:

```bash
node hello.js
```

Output:

```
Hello dari Node.js!
```

---

## 🧠 Catatan

| Fungsi             | Keterangan                                          |
| ------------------ | --------------------------------------------------- |
| `console.log()`    | Menampilkan teks ke console (debugging)             |
| `alert()`          | Menampilkan pesan pop-up (khusus browser)           |
| `document.write()` | Menulis langsung ke halaman HTML (tidak disarankan) |

---

## 🧪 Tantangan Cepat

1. Tampilkan nama kamu dengan `console.log()`
2. Tampilkan dua kalimat dalam satu output
3. Tampilkan angka, boolean, dan string

```javascript
console.log("Nama saya Marno");
console.log("Saya belajar JavaScript dengan semangat!");
console.log(123, true, "Belajar itu menyenangkan");
```

---
> Perjalanan seribu baris kode dimulai dari satu `console.log`.

Selanjutnya, kita akan belajar tentang **variabel** dan bagaimana cara menyimpan data dalam JavaScript.