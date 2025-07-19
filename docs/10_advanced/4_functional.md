# 🔁 Pemrograman Fungsional di JavaScript

Pemrograman fungsional (Functional Programming/FP) adalah paradigma pemrograman yang berfokus pada penggunaan fungsi murni, imutabilitas data, dan penghindaran efek samping.

---

## 📐 Ciri-ciri Pemrograman Fungsional

- **Fungsi murni (pure function)**: tidak mengubah data di luar dirinya dan selalu mengembalikan hasil yang sama untuk input yang sama.
- **Imutabilitas**: data tidak diubah setelah dibuat.
- **Fungsi sebagai first-class citizen**: fungsi bisa disimpan dalam variabel, dikirim sebagai parameter, atau dikembalikan dari fungsi lain.
- **Deklaratif, bukan imperatif**: fokus pada *apa* yang dilakukan, bukan *bagaimana*.

---

## 🔍 Contoh Fungsi Murni

```javascript
// Fungsi murni
function tambah(a, b) {
  return a + b;
}

// Bukan fungsi murni (karena memodifikasi variabel di luar dirinya)
let total = 0;
function tambahGlobal(a) {
  total += a;
}
````

---

## 🧰 Higher-Order Function

Fungsi yang menerima fungsi lain sebagai argumen atau mengembalikan fungsi lain.

```javascript
function repeat(fn, n) {
  for (let i = 0; i < n; i++) {
    fn();
  }
}

repeat(() => console.log("Halo!"), 3);
```

---

## 🧼 Method Array: map, filter, reduce

### `map`: transformasi elemen

```javascript
const angka = [1, 2, 3];
const kuadrat = angka.map(n => n * n);
console.log(kuadrat); // [1, 4, 9]
```

### `filter`: menyaring elemen

```javascript
const ganjil = angka.filter(n => n % 2 === 1);
console.log(ganjil); // [1, 3]
```

### `reduce`: akumulasi elemen

```javascript
const total = angka.reduce((acc, cur) => acc + cur, 0);
console.log(total); // 6
```

---

## 🔄 Imutabilitas

Gunakan spread operator atau metode `Array.prototype` untuk menjaga data tetap tidak berubah:

```javascript
const buah = ['apel', 'jeruk'];
const buahBaru = [...buah, 'mangga']; // Tidak mengubah array asli
```

---

## 🧪 Contoh chaining FP

```javascript
const hasil = [1, 2, 3, 4, 5]
  .map(n => n * 2)
  .filter(n => n > 5)
  .reduce((a, b) => a + b, 0);

console.log(hasil); // 18
```

---

## 📎 Kesimpulan

Pemrograman fungsional membantu membuat kode lebih modular, bersih, dan mudah diuji. JavaScript bukan bahasa FP murni, tetapi sangat mendukung gaya ini melalui `map`, `filter`, `reduce`, dan first-class function.

```