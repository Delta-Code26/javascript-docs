## 🐞 Debugging di JavaScript

Debugging adalah proses menemukan dan memperbaiki bug atau kesalahan dalam kode. JavaScript menyediakan berbagai alat dan teknik untuk membantu proses ini.

---

### 🔍 Teknik Debugging Umum

#### 1. `console.log()`

Cara termudah dan paling umum:

```javascript
let hasil = hitungNilai(5);
console.log('Nilai hasil:', hasil);
```

---

#### 2. `console.error()` & `console.warn()`

Untuk menandai error atau peringatan:

```javascript
console.error('Terjadi kesalahan!');
console.warn('Peringatan: nilai tidak valid!');
```

---

#### 3. Menggunakan `debugger`

Perintah `debugger` akan menghentikan eksekusi saat titik itu, jika DevTools terbuka.

```javascript
function hitung(a, b) {
  debugger;
  return a + b;
}
```

---

#### 4. Browser DevTools

Gunakan **Developer Tools** di browser:

* **Console**: melihat log/error
* **Sources**: set breakpoint, jalankan step-by-step
* **Network**: pantau permintaan HTTP

---

### 🧠 Tips Debugging Efektif

* Reproduksi bug secara konsisten
* Cek log step-by-step
* Gunakan breakpoint di bagian penting
* Cek alur data dan nilai variabel
* Jangan buru-buru menyalahkan framework—coba isolasi kasusnya

---

### 📦 Tools Tambahan

* **VS Code Debugger**: integrasi debugging langsung di editor
* **Linting tools** (ESLint): mendeteksi potensi bug saat mengetik
* **Testing tools**: Jest, Mocha untuk uji otomatis

---

> 🎯 Debugging bukan hanya mencari kesalahan, tapi memahami bagaimana kode bekerja — dan mengapa ia gagal.
