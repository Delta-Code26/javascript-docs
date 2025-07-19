# Fungsi Dasar dalam JavaScript

Fungsi (function) adalah blok kode yang dirancang untuk menjalankan tugas tertentu. Fungsi memungkinkan kita untuk menulis kode yang dapat digunakan kembali, modular, dan lebih mudah dipelihara.

## 1. Deklarasi Fungsi

### Sintaks Dasar

```javascript
function sapa() {
  console.log("Halo, dunia!");
}

sapa(); // Output: Halo, dunia!
````

## 2. Fungsi dengan Parameter

```javascript
function sapa(nama) {
  console.log(`Halo, ${nama}!`);
}

sapa("Marno"); // Output: Halo, Marno!
```

## 3. Fungsi dengan Return Value

```javascript
function tambah(a, b) {
  return a + b;
}

let hasil = tambah(3, 5);
console.log(hasil); // Output: 8
```

## 4. Function Expression

```javascript
const kali = function(x, y) {
  return x * y;
};

console.log(kali(4, 5)); // Output: 20
```

## 5. Arrow Function (ES6)

```javascript
const bagi = (a, b) => a / b;

console.log(bagi(10, 2)); // Output: 5
```

## Catatan:

* **Function Declaration** dikenali oleh JavaScript sebelum eksekusi (hoisting).
* **Function Expression** dan **Arrow Function** tidak dikenali sebelum baris eksekusi.

---

> Fungsi adalah jiwa dari modularitas dalam pemrograman. Menulislah seperti pujangga, panggillah seperti maestro.