# 🧬 Tipe Data di JavaScript

JavaScript adalah bahasa yang **dinamis**, artinya tipe data variabel bisa berubah tergantung nilainya. Di awal belajar, penting untuk mengenali tipe-tipe data **primitif** dan **non-primitif (referensi)**.

---

## 🧪 Tipe Data Primitif

Tipe data primitif adalah data yang **tidak bisa dipecah lagi**. Mereka disimpan langsung di memori.

| Tipe         | Contoh                   |
|--------------|---------------------------|
| `string`     | `"Halo Dunia"`            |
| `number`     | `42`, `3.14`              |
| `boolean`    | `true`, `false`           |
| `undefined`  | variabel belum diisi      |
| `null`       | tidak ada nilai            |
| `symbol`     | simbol unik (jarang dipakai) |
| `bigint`     | angka besar (ES2020+)     |

```javascript
let nama = "Marno";         // string
let umur = 21;              // number
let aktif = true;           // boolean
let pekerjaan;              // undefined
let kosong = null;          // null
````

> 🧠 `typeof null` akan menghasilkan `"object"` — ini adalah bug historis di JavaScript.

---

## 🔢 Number

Semua angka di JavaScript, baik bilangan bulat maupun desimal, masuk ke dalam tipe `number`.

```javascript
let x = 10;
let y = 3.14;
let total = x + y;
```

> 💡 Tidak ada `int` atau `float` di JavaScript. Semua disebut `number`.

---

## 📛 String

String adalah teks yang dibungkus dengan tanda kutip `' '`, `" "`, atau `` ` ` `` (backtick).

```javascript
let nama = "Marno";
let salam = `Halo, ${nama}!`; // Template literal
```

---

## 🧭 Boolean

Digunakan untuk menyatakan benar (`true`) atau salah (`false`):

```javascript
let sudahBayar = true;
let masihAktif = false;
```

---

## 🕳 Null vs Undefined

```javascript
let kosong = null;      // Disengaja kosong
let belumIsi;           // Undefined secara default
```

---

## 🧮 BigInt (ES2020+)

Untuk angka **sangat besar** melebihi batas `Number.MAX_SAFE_INTEGER`:

```javascript
let big = 1234567890123456789012345678901234567890n;
```

> BigInt tidak bisa dicampur langsung dengan `number` biasa.

---

## 🔰 Tipe Data Referensi (Non-Primitif)

Selain tipe data primitif, JavaScript punya tipe data **kompleks** seperti:

* **Object**: Struktur data berbentuk pasangan `key-value`.
* **Array**: Kumpulan nilai dalam urutan.
* **Function**: Juga dianggap objek di JavaScript.

```javascript
let orang = {
  nama: "Marno",
  umur: 22
};

let hobi = ["ngoding", "ngopi", "ngonten"];
```

---

## 🔍 typeof Operator

Gunakan `typeof` untuk mengecek tipe data:

```javascript
typeof "Halo"      // string
typeof 42          // number
typeof true        // boolean
typeof undefined   // undefined
typeof null        // object (bug bawaan!)
typeof {}          // object
typeof []          // object
typeof function(){} // function
```

---

## 🧪 Tantangan Cepat

1. Buat variabel: `nama`, `umur`, `menikah`, `anak`, `tinggi`.
2. Gunakan `typeof` untuk mengecek tipe datanya.

```javascript
let nama = "Budi";
let umur = 30;
let menikah = false;
let anak = null;
let tinggi;

console.log(typeof nama);     // string
console.log(typeof umur);     // number
console.log(typeof menikah);  // boolean
console.log(typeof anak);     // object
console.log(typeof tinggi);   // undefined
```

---

> “Tipe data adalah bentuk wujud dari informasi yang kita kelola.”

Selanjutnya: Mari kita bahas tentang **operator** — alat utama untuk memproses data!