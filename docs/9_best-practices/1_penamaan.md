## ✍️ Praktik Terbaik: Penamaan (Naming)

Penamaan yang baik adalah kunci dari kode yang mudah dibaca dan dipelihara. JavaScript tidak mewajibkan format tertentu, tapi ada konvensi umum yang disarankan oleh komunitas.

---

### 📌 Aturan Umum Penamaan

* **Gunakan nama yang deskriptif dan jelas**

  ```js
  let jumlahSiswa = 30; // ✅ jelas
  let x = 30;           // ❌ tidak informatif
  ```

* **Gunakan Bahasa Inggris**

  ```js
  let studentCount = 30; // ✅
  let jumlahSiswa = 30;  // ❌ campur aduk
  ```

* **Hindari singkatan kecuali sudah umum**

  ```js
  let isValid = true;     // ✅
  let iv = true;          // ❌
  ```

---

### 🧱 Konvensi Penamaan Berdasarkan Jenis

| Jenis               | Format       | Contoh                     |
| ------------------- | ------------ | -------------------------- |
| Variabel            | camelCase    | `totalAmount`, `userName`  |
| Fungsi              | camelCase    | `getData()`, `sendEmail()` |
| Konstanta           | UPPER\_SNAKE | `MAX_USERS`, `API_KEY`     |
| Class / Constructor | PascalCase   | `UserProfile`, `Invoice`   |
| File / Modul        | kebab-case   | `user-service.js`          |

---

### 🤔 Nama yang Buruk vs Nama yang Baik

| Buruk  | Baik        | Alasan                   |
| ------ | ----------- | ------------------------ |
| `d`    | `duration`  | Lebih deskriptif         |
| `data` | `userList`  | Spesifik terhadap isi    |
| `val1` | `startDate` | Representasi makna jelas |

---

### ✨ Tips Bonus

* Gunakan kata kerja untuk nama fungsi → `getUser()`, `sendEmail()`
* Gunakan kata benda untuk variabel → `user`, `invoiceData`
* Jangan ragu membuat nama agak panjang asal jelas
* Konsisten dalam penamaan di seluruh proyek

---

> 📖 “Code is read more often than it is written.”
> — Robert C. Martin (Clean Code)
