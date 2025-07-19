# 💾 Variabel di JavaScript

Variabel adalah **wadah untuk menyimpan data** dalam program. Dalam JavaScript, kita dapat menyimpan teks, angka, boolean, objek, dan masih banyak lagi ke dalam sebuah variabel.

---

## 🏷️ Deklarasi Variabel

JavaScript menyediakan **tiga cara** untuk mendeklarasikan variabel:

```javascript
var nama = "Marno";
let usia = 21;
const negara = "Malaysia";
````

| Kata Kunci | Bisa Diubah Nilainya? | Lingkup (Scope) | Direkomendasikan |
| ---------- | --------------------- | --------------- | ---------------- |
| `var`      | Ya                    | Function scope  | ❌ Tidak          |
| `let`      | Ya                    | Block scope     | ✅ Ya             |
| `const`    | Tidak (konstan)       | Block scope     | ✅ Ya             |

> ⚠️ Hindari `var` karena dapat menyebabkan bug tak terduga akibat hoisting dan scope yang longgar.

---

## 📦 Contoh Penggunaan

```javascript
let nama = "Marno";
const umur = 22;

console.log("Halo, nama saya " + nama + " dan umur saya " + umur + " tahun.");
```

---

## 📚 Aturan Penamaan Variabel

* Gunakan huruf, angka, underscore `_`, atau dolar `$`.
* Tidak boleh diawali dengan angka.
* Case-sensitive: `Nama` dan `nama` dianggap berbeda.
* Gunakan camelCase untuk penulisan yang baik:

  ```javascript
  let totalHarga;
  let jumlahBarang;
  ```

---

## 🔁 Mengubah Nilai Variabel

```javascript
let kota = "Kuching";
kota = "Miri";  // OK

const negara = "Malaysia";
negara = "Indonesia"; // ❌ Error! const tidak bisa diubah
```

---

## 🧠 Hoisting

`var` akan **diangkat ke atas (hoisted)** dan dapat digunakan sebelum dideklarasikan, tapi nilainya `undefined`:

```javascript
console.log(nama); // undefined
var nama = "Rina";
```

Sedangkan `let` dan `const` **tidak bisa** digunakan sebelum dideklarasikan:

```javascript
console.log(nama); // ❌ ReferenceError
let nama = "Rina";
```

---

## 🧪 Tantangan Cepat

1. Buat variabel `produk`, `harga`, dan `stok`.
2. Cetak kalimat: `"Produk: Apel, Harga: 5000, Stok: 20"`

```javascript
let produk = "Apel";
let harga = 5000;
let stok = 20;

console.log("Produk: " + produk + ", Harga: " + harga + ", Stok: " + stok);
```

---

> “Variabel adalah bahasa manusia yang dimengerti oleh komputer.”

Selanjutnya: Mari kita pelajari jenis **tipe data** yang bisa disimpan ke dalam variabel.