## 📘 Optional Chaining (`?.`)

**Deskripsi:**
Optional chaining (`?.`) adalah fitur modern JavaScript yang diperkenalkan di **ES2020**, digunakan untuk **mengakses properti objek yang dalam** tanpa harus memeriksa apakah properti sebelumnya `null` atau `undefined`.

---

### 🔍 Masalah Umum Sebelum Optional Chaining:

Tanpa optional chaining, kita sering menulis pengecekan berlapis seperti:

```javascript
if (user && user.address && user.address.city) {
  console.log(user.address.city);
}
```

---

### ✅ Solusi dengan Optional Chaining:

```javascript
console.log(user?.address?.city);
```

Jika salah satu di antaranya `null` atau `undefined`, hasilnya otomatis `undefined` tanpa error.

---

### 🧪 Contoh Lain:

```javascript
let data = {
  profile: {
    name: 'Marno',
    contact: {
      email: 'marno@example.com'
    }
  }
};

console.log(data?.profile?.contact?.email); // ✅ 'marno@example.com'
console.log(data?.profile?.address?.city);  // ✅ undefined, tidak error
```

---

### ⚠️ Penting Diketahui:

* Optional chaining hanya menghentikan akses jika properti sebelumnya **nullish** (`null` atau `undefined`)
* Tidak mencegah error dari fungsi yang tidak ada, kecuali digunakan seperti:

```javascript
user?.sayHello?.();
```

---

### 📌 Kapan Digunakan?

Gunakan optional chaining saat:

* Mengakses data API yang bisa saja tidak lengkap
* Menelusuri properti bersarang dalam objek
* Menghindari penulisan `if` bertingkat yang tidak efisien

---