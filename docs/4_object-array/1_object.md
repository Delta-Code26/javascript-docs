# 🧱 Object dalam JavaScript

Object adalah salah satu tipe data paling penting dan fleksibel di JavaScript. Ia digunakan untuk menyimpan data dalam bentuk pasangan *key-value*.

---

## 1. Pengenalan Object

Object adalah koleksi properti, di mana setiap properti terdiri dari **key (nama properti)** dan **value (nilai)**.

```javascript
const orang = {
  nama: "Marno",
  umur: 22,
  pekerjaan: "Programmer",
};
````

---

## 2. Mengakses Properti

### a. Dot Notation

```javascript
console.log(orang.nama); // Output: Marno
```

### b. Bracket Notation

```javascript
console.log(orang["umur"]); // Output: 22
```

> Gunakan bracket notation saat key disimpan sebagai variabel atau mengandung spasi/simbol.

---

## 3. Menambah & Mengubah Properti

```javascript
orang.alamat = "Malaysia";         // Menambah
orang.umur = 23;                   // Mengubah
```

---

## 4. Menghapus Properti

```javascript
delete orang.pekerjaan;
```

---

## 5. Object di Dalam Object (Nested Object)

```javascript
const user = {
  nama: "Budi",
  kontak: {
    email: "budi@email.com",
    telp: "08123456789"
  }
};

console.log(user.kontak.email);
```

---

## 6. Object Method

Fungsi di dalam object disebut **method**:

```javascript
const kalkulator = {
  tambah: function(a, b) {
    return a + b;
  }
};

console.log(kalkulator.tambah(3, 4)); // Output: 7
```

---

## 7. Shorthand Property & Method (ES6)

```javascript
const nama = "Siti";
const umur = 20;

const user = {
  nama,
  umur,
  sapa() {
    return `Halo, saya ${this.nama}`;
  }
};
```

---

## 8. Iterasi Properti Object

Gunakan `for...in` untuk iterasi key:

```javascript
for (let key in orang) {
  console.log(`${key}: ${orang[key]}`);
}
```

---

## Tantangan Cepat

1. Buat object `produk` dengan properti `nama`, `harga`, dan `stok`.
2. Tambahkan method `infoProduk()` yang mencetak informasi produk.

```javascript
const produk = {
  nama: "Kopi Robusta",
  harga: 25000,
  stok: 50,
  infoProduk() {
    return `${this.nama} - Rp${this.harga} (Stok: ${this.stok})`;
  }
};

console.log(produk.infoProduk());
```

---

> “Object adalah cara JavaScript memberi makna pada data.” – Anonymous