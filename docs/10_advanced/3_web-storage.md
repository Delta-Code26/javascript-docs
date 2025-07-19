# 🗄️ Web Storage di JavaScript

Web Storage API menyediakan cara untuk menyimpan data secara lokal di browser pengguna. Ada dua jenis utama: `localStorage` dan `sessionStorage`.

---

## 🧱 Perbedaan localStorage dan sessionStorage

| Fitur             | localStorage                          | sessionStorage                        |
|------------------|----------------------------------------|----------------------------------------|
| Durasi Penyimpanan | Permanen (hingga dihapus manual)       | Hanya selama sesi browser aktif        |
| Akses Antar Tab   | Ya, dapat diakses di tab yang berbeda  | Tidak, hanya di tab asal               |
| Ukuran Maksimal   | Sekitar 5–10 MB                        | Sekitar 5 MB                           |

---

## 📦 Cara Menggunakan localStorage

```javascript
// Menyimpan data
localStorage.setItem('nama', 'Marno');

// Mengambil data
const nama = localStorage.getItem('nama');
console.log(nama); // Marno

// Menghapus data
localStorage.removeItem('nama');

// Menghapus semua data
localStorage.clear();
````

---

## 🧭 Cara Menggunakan sessionStorage

```javascript
sessionStorage.setItem('loginStatus', 'true');

const status = sessionStorage.getItem('loginStatus');
console.log(status); // true

sessionStorage.removeItem('loginStatus');
```

---

## 🛡️ Kapan Menggunakan localStorage vs sessionStorage?

* Gunakan `localStorage` untuk data jangka panjang (seperti preferensi tema, token login).
* Gunakan `sessionStorage` untuk data sementara yang hanya berlaku selama tab terbuka (seperti data form sementara).

---

## ⚠️ Catatan Keamanan

* **Jangan menyimpan data sensitif (seperti password atau token akses) di localStorage/sessionStorage** karena dapat diakses oleh JavaScript dan rawan XSS.
* Gunakan **HTTP-only cookies** jika perlu menyimpan token secara aman.

---

## 📚 Kesimpulan

Web Storage sangat berguna untuk menyimpan data kecil secara lokal tanpa memerlukan server, namun harus digunakan dengan bijak dan aman.

```

---

Kalau kamu ingin saya buatkan juga bagian lanjutan seperti IndexedDB atau mengintegrasikan storage dengan aplikasi real-time, tinggal bilang saja!
```
