## 📦 ES6 Modules

Sejak ES6, JavaScript mendukung modularisasi secara native melalui `import` dan `export`. Ini memungkinkan kita untuk memisahkan kode ke dalam file yang lebih kecil dan lebih terorganisir.

---

### 🚀 Export

Kita bisa mengekspor variabel, fungsi, atau class dari suatu file agar dapat digunakan di file lain.

```javascript
// math.js
export const PI = 3.14;

export function tambah(a, b) {
  return a + b;
}

export class Kalkulator {
  static kurang(a, b) {
    return a - b;
  }
}
```

---

### 📥 Import

Gunakan `import` untuk mengambil kode dari file lain.

```javascript
// main.js
import { PI, tambah, Kalkulator } from './math.js';

console.log(PI); // 3.14
console.log(tambah(2, 3)); // 5
console.log(Kalkulator.kurang(10, 3)); // 7
```

---

### 🧩 Default Export

Kita juga bisa mengekspor satu nilai default dari sebuah modul.

```javascript
// message.js
export default function hello() {
  console.log("Hello dari modul!");
}
```

```javascript
// app.js
import hello from './message.js';

hello(); // Hello dari modul!
```

---

### ⚠️ Catatan

* File harus menggunakan ekstensi `.js` dan dijalankan dalam environment yang mendukung ES Module (misalnya melalui bundler seperti Webpack/Vite, atau pakai `type="module"` di HTML).
* Path relatif (./, ../) wajib saat mengimport file lokal.

---

### ✅ Kapan Menggunakan?

Gunakan modularisasi jika:

* Proyek mulai membesar dan banyak file
* Ingin memisahkan tanggung jawab kode
* Mempermudah testing dan pemeliharaan