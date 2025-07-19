# Scope dan Hoisting dalam JavaScript

Memahami bagaimana **scope** dan **hoisting** bekerja adalah kunci menulis kode JavaScript yang bersih dan bebas bug.

---

## 1. Apa Itu Scope?

**Scope** adalah konteks di mana variabel didefinisikan dan diakses. Ada dua jenis utama:

### a. Global Scope

Variabel yang dideklarasikan di luar fungsi memiliki cakupan global.

```javascript
let nama = "Marno";

function tampilkanNama() {
  console.log(nama); // Bisa diakses karena berada di scope global
}
````

### b. Function / Local Scope

Variabel yang dideklarasikan di dalam fungsi hanya bisa diakses dalam fungsi itu.

```javascript
function halo() {
  let pesan = "Selamat datang!";
  console.log(pesan);
}

console.log(pesan); // ❌ Error: pesan is not defined
```

---

## 2. Block Scope (`let` dan `const`)

`let` dan `const` hanya berlaku di dalam blok ({}), tidak seperti `var`.

```javascript
{
  let x = 10;
  const y = 20;
}

console.log(x); // ❌ Error
```

---

## 3. Hoisting

**Hoisting** adalah perilaku JavaScript yang "mengangkat" deklarasi variabel dan fungsi ke bagian atas scope-nya sebelum kode dijalankan.

### a. Hoisting dengan `var`

```javascript
console.log(nama); // Output: undefined
var nama = "Andi";
```

> Variabel `nama` di-"hoist", tetapi nilainya `undefined` sampai baris penugasan dijalankan.

### b. Tidak Hoisting dengan `let` dan `const`

```javascript
console.log(nama); // ❌ Error: Cannot access 'nama' before initialization
let nama = "Budi";
```

---

## 4. Hoisting pada Fungsi

### Function Declaration

```javascript
sayHi(); // Output: Halo!

function sayHi() {
  console.log("Halo!");
}
```

### Function Expression

```javascript
sayHi(); // ❌ Error: sayHi is not a function

const sayHi = function() {
  console.log("Halo!");
};
```

---

> Dalam dunia JavaScript, variabel bisa muncul sebelum waktunya—itulah hoisting. Namun, jangan terlena. Disiplin deklarasi tetap yang utama.