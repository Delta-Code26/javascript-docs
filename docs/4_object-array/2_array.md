# 📚 Array di JavaScript

Array adalah struktur data di JavaScript yang digunakan untuk menyimpan banyak nilai dalam satu variabel. Array diakses dengan indeks numerik yang dimulai dari nol.

---

## 🧱 Cara Membuat Array

```javascript
let buah = ["Apel", "Jeruk", "Mangga"];
console.log(buah); // ["Apel", "Jeruk", "Mangga"]
````

---

## 🔁 Akses dan Manipulasi Elemen

```javascript
console.log(buah[0]); // Apel

buah[1] = "Pisang";
console.log(buah); // ["Apel", "Pisang", "Mangga"]
```

---

## 🔨 Method Umum Array

| Method      | Kegunaan                                  |
| ----------- | ----------------------------------------- |
| `push()`    | Menambahkan elemen di akhir               |
| `pop()`     | Menghapus elemen terakhir                 |
| `shift()`   | Menghapus elemen pertama                  |
| `unshift()` | Menambahkan elemen di awal                |
| `splice()`  | Menambah/menghapus di posisi tertentu     |
| `slice()`   | Mengambil sebagian array (tidak mengubah) |
| `forEach()` | Iterasi setiap elemen                     |
| `map()`     | Menghasilkan array baru dari transformasi |

---

## 🧪 Contoh:

```javascript
let angka = [1, 2, 3, 4, 5];

let kuadrat = angka.map(function(x) {
  return x * x;
});

console.log(kuadrat); // [1, 4, 9, 16, 25]
```

---

## 📦 Nested Array

Array bisa berisi array lain:

```javascript
let matriks = [
  [1, 2],
  [3, 4]
];

console.log(matriks[1][0]); // 3
```

---

## 🧠 Catatan

* Array di JavaScript bersifat **dinamis** (ukuran dapat berubah).
* Tipe data elemen bisa **campur** (number, string, objek, dll).
* Gunakan `Array.isArray()` untuk memeriksa apakah sebuah variabel adalah array.

```javascript
Array.isArray([1, 2, 3]); // true
```

---

⏭️ Selanjutnya: [Kontrol Alur Program](../5_kontrol/index.md)
