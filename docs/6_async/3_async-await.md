## ⏳ Async & Await di JavaScript

`async` dan `await` adalah sintaks modern JavaScript untuk menangani operasi asynchronous yang lebih mudah dibaca dibandingkan dengan chaining `.then()` pada `Promise`.

---

### 🔧 Dasar Penggunaan

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const json = await response.json();
    console.log(json);
  } catch (error) {
    console.error('Terjadi error:', error);
  }
}
```

---

### 🧠 Penjelasan

* `async` digunakan untuk mendeklarasikan fungsi yang mengembalikan Promise.
* `await` hanya bisa digunakan di dalam fungsi async, menunggu promise selesai sebelum melanjutkan eksekusi.

---

### ⚠️ Catatan Penting

* Error harus ditangani dengan `try...catch`.
* Tidak bisa digunakan di luar fungsi async (kecuali di top-level async function, jika environment mendukung).

---

### 💡 Contoh Lain

```javascript
const getUser = async (id) => {
  const res = await fetch(`https://api.example.com/users/${id}`);
  return res.json();
};

getUser(2)
  .then(user => console.log(user))
  .catch(err => console.log(err));
```

---

### 📌 Kapan Digunakan?

Gunakan `async/await`:

* Jika kamu ingin membuat kode async tampak seperti kode sync
* Jika kamu ingin menghindari chaining `.then().then().catch()`