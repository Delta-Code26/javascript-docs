## 🧼 Praktik Terbaik: Clean Code di JavaScript

Menulis *clean code* bukan sekadar membuat kode bisa jalan, tapi membuatnya **mudah dipahami, diperbaiki, dan dikembangkan**. Tujuan utama clean code adalah **komunikasi**, bukan hanya instruksi ke mesin.

---

### 📌 Prinsip-Prinsip Clean Code

#### 1. **Tulislah kode seolah-olah orang lain yang akan membacanya adalah seorang psikopat yang tahu di mana kamu tinggal.**

* Artinya: Buat kode yang jelas, aman, dan mudah dimengerti 😄

---

#### 2. **Gunakan Nama yang Jelas dan Deskriptif**

```js
// ❌ Buruk
let a = true;

// ✅ Baik
let isLoggedIn = true;
```

---

#### 3. **Fungsi Harus Melakukan Satu Tugas Spesifik**

```js
// ❌ Buruk
function handleUser(user) {
  validate(user);
  saveToDB(user);
  sendEmail(user);
}

// ✅ Baik
function validateUser(user) { ... }
function saveUserToDB(user) { ... }
function sendWelcomeEmail(user) { ... }
```

---

#### 4. **Hindari Duplikasi**

> "Duplication is the root of all evil." – *Don’t Repeat Yourself (DRY)*

Gunakan fungsi atau modul untuk bagian kode yang berulang.

---

#### 5. **Gunakan Default Parameter & Destructuring**

```js
// ❌ Buruk
function createUser(data) {
  let name = data.name || 'Unknown';
}

// ✅ Baik
function createUser({ name = 'Unknown' }) { ... }
```

---

#### 6. **Gunakan Early Return**

```js
// ❌ Buruk
function isEligible(age) {
  if (age >= 18) {
    return true;
  } else {
    return false;
  }
}

// ✅ Baik
function isEligible(age) {
  return age >= 18;
}
```

---

#### 7. **Komentar Bukan Solusi, Tapi Pilihan Terakhir**

Komentar bagus, tapi kode yang jelas **lebih baik daripada komentar**.

```js
// ❌ Buruk
// Mengecek apakah umur pengguna lebih dari 18
if (user.age > 18) { ... }

// ✅ Baik
const isAdult = user.age > 18;
if (isAdult) { ... }
```

---

### ✨ Kesimpulan

> Clean code adalah soal **komunikasi**.
> Kode yang bersih menjelaskan niat programmer, membantu kolaborasi tim, dan mengurangi biaya perawatan. Jangan sekadar membuatnya bekerja — buatlah ia **berarti**.

---

> 🧠 “Clean code always looks like it was written by someone who cares.”
> — *Michael Feathers*
