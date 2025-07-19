# 🔄 Callback di JavaScript

Callback adalah fungsi yang dikirimkan sebagai argumen ke fungsi lain dan dieksekusi setelah suatu proses selesai. Ini merupakan dasar dari asynchronous programming di JavaScript.

## Kenapa Callback?

Karena JavaScript bersifat non-blocking dan asynchronous, callback digunakan untuk menangani operasi yang memakan waktu, seperti:

- Pembacaan file
- Permintaan HTTP
- Timeout dan interval

## Contoh Sederhana

```javascript
function halo(nama, callback) {
  console.log("Halo, " + nama);
  callback();
}

function selesai() {
  console.log("Selesai dipanggil.");
}

halo("Marno", selesai);
````

## Callback dengan setTimeout

```javascript
console.log("Mulai");

setTimeout(function() {
  console.log("Tertunda 2 detik");
}, 2000);

console.log("Selesai");
```

Output:

```
Mulai
Selesai
Tertunda 2 detik
```

## Callback pada Array

```javascript
const angka = [1, 2, 3, 4];

angka.forEach(function(nilai) {
  console.log(nilai);
});
```

## Callback Hell 😵

Terlalu banyak callback bersarang dapat membuat kode susah dibaca:

```javascript
loginUser("user", function(user) {
  ambilData(user.id, function(data) {
    simpanData(data, function(res) {
      console.log("Selesai", res);
    });
  });
});
```

Solusi:

* Gunakan **Promise**
* Gunakan **Async/Await**

---

📌 **Tips**:

* Callback sebaiknya ditulis sebagai named function jika akan digunakan ulang.
* Gunakan teknik modern seperti Promise atau Async/Await untuk kode lebih bersih. 