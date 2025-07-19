## 🛠️ Try-Catch

`try-catch` adalah struktur kontrol di JavaScript untuk menangani error atau pengecualian (exception) tanpa menghentikan eksekusi program.

---

### 🧪 Struktur Dasar

```javascript
try {
  // kode yang berpotensi error
} catch (error) {
  // penanganan error
}
```

---

### 📌 Contoh Penggunaan

```javascript
try {
  let hasil = 10 / 0;
  console.log(hasil);

  tidakAdaFungsi(); // ini akan menyebabkan error
} catch (err) {
  console.error('Terjadi error:', err.message);
}
```

---

### 🔁 Blok Finally

Blok `finally` akan selalu dijalankan, baik terjadi error maupun tidak.

```javascript
try {
  console.log('Mulai');
  JSON.parse('ini bukan json');
} catch (e) {
  console.error('Kesalahan parsing:', e.message);
} finally {
  console.log('Selesai mencoba!');
}
```

---

### 📙 Properti Objek Error

* `message`: Pesan error
* `name`: Nama error (`ReferenceError`, `SyntaxError`, dll)
* `stack`: Informasi stack trace

---

### ❗ Penting

* Jangan gunakan `try-catch` untuk kontrol alur program biasa.
* Gunakan untuk menangani kemungkinan error eksternal: parsing data, operasi file, koneksi API, dll.

---

> ✅ Gunakan `try-catch` untuk membuat program Anda lebih tahan banting terhadap kondisi tak terduga.
