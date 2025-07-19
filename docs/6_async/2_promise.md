# 💬 Promise di JavaScript

`Promise` adalah objek yang merepresentasikan **selesainya (atau gagalnya)** sebuah operasi asynchronous di masa depan.

Promise memberikan cara yang lebih bersih dan elegan dibanding callback, terutama untuk menghindari callback hell.

---

## 🧠 Konsep Dasar

Sebuah `Promise` memiliki 3 status:

- `pending`: masih dalam proses
- `fulfilled`: berhasil
- `rejected`: gagal

```javascript
const janji = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Berhasil!");
  } else {
    reject("Gagal!");
  }
});
````

---

## ✅ Menangani Promise

```javascript
janji
  .then((hasil) => {
    console.log("Berhasil:", hasil);
  })
  .catch((error) => {
    console.log("Gagal:", error);
  });
```

---

## 🕰 Contoh Asynchronous

```javascript
function ambilData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const berhasil = true;

      if (berhasil) {
        resolve("Data berhasil diambil");
      } else {
        reject("Terjadi kesalahan");
      }
    }, 2000);
  });
}

ambilData()
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

---

## 🔗 Promise Chaining

```javascript
function proses1() {
  return Promise.resolve("Langkah 1");
}

function proses2(data) {
  return Promise.resolve(data + " -> Langkah 2");
}

proses1()
  .then(proses2)
  .then((hasil) => console.log(hasil));
```

---

## 🧯 Promise.all

Menjalankan beberapa promise sekaligus:

```javascript
const p1 = Promise.resolve("Satu");
const p2 = Promise.resolve("Dua");
const p3 = Promise.resolve("Tiga");

Promise.all([p1, p2, p3]).then((nilai) => {
  console.log(nilai); // ['Satu', 'Dua', 'Tiga']
});
```

---

📌 **Tips:**

* Gunakan `.finally()` untuk menjalankan sesuatu setelah `then`/`catch` selesai.
* Lebih baik gunakan async/await untuk meningkatkan keterbacaan.

➡️ Selanjutnya: [`Async/Await`](./3_async-await.md)