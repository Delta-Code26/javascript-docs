## 🧱 CommonJS

CommonJS adalah sistem modul yang digunakan secara luas di Node.js sebelum ES6 Modules hadir. Modul CommonJS menggunakan `require()` untuk impor dan `module.exports` untuk ekspor.

---

### 📤 Ekspor

```javascript
// math.js
const PI = 3.14;

function tambah(a, b) {
  return a + b;
}

module.exports = {
  PI,
  tambah,
};
```

---

### 📥 Impor

```javascript
// main.js
const math = require('./math');

console.log(math.PI); // 3.14
console.log(math.tambah(2, 3)); // 5
```

---

### 📦 Sifat-sifat CommonJS

* **Sinkron**: Impor dilakukan secara sinkron, cocok untuk environment seperti server (Node.js).
* **Dijalankan sekali**: Ketika sebuah modul diimpor, kode di dalamnya hanya dijalankan sekali (cached).
* **Ekspor fleksibel**: Bisa mengekspor satu objek besar atau bagian-bagian tertentu saja.

---

### ⚠️ Perbedaan dengan ES6 Modules

| Fitur           | CommonJS         | ES6 Modules                 |
| --------------- | ---------------- | --------------------------- |
| Keyword Impor   | `require()`      | `import`                    |
| Keyword Ekspor  | `module.exports` | `export` / `export default` |
| Waktu Evaluasi  | Saat runtime     | Saat compile                |
| Lingkungan Umum | Node.js          | Browser, bundler            |

---

### 🎯 Kapan Menggunakan CommonJS?

* Saat membangun aplikasi Node.js yang tidak perlu bundler
* Saat menggunakan modul lama yang belum mendukung ES6

---

> ℹ️ Mulai Node.js v14+, ES Modules sudah lebih stabil. Tapi CommonJS masih sangat relevan dan banyak digunakan di ekosistem Node.js.
