# ⚙️ Operator dalam JavaScript

Operator adalah **simbol atau keyword** yang digunakan untuk melakukan operasi terhadap satu atau lebih nilai (operand). Mulai dari penjumlahan hingga logika kompleks — semua bisa dilakukan dengan operator.

---

## ➕ Operator Aritmatika

Digunakan untuk perhitungan matematis:

| Operator | Fungsi          | Contoh           |
|----------|------------------|------------------|
| `+`      | Penjumlahan      | `5 + 3` → `8`     |
| `-`      | Pengurangan      | `10 - 4` → `6`    |
| `*`      | Perkalian        | `2 * 3` → `6`     |
| `/`      | Pembagian        | `10 / 2` → `5`    |
| `%`      | Modulus (sisa)   | `7 % 3` → `1`     |
| `**`     | Pangkat (ES6)    | `2 ** 3` → `8`    |

```javascript
let a = 10;
let b = 3;
console.log(a + b); // 13
console.log(a % b); // 1
````

---

## 🟰 Operator Penugasan (Assignment)

Digunakan untuk menetapkan nilai ke variabel:

| Operator | Contoh   | Sama dengan |
| -------- | -------- | ----------- |
| `=`      | `x = 10` | `10`        |
| `+=`     | `x += 5` | `x = x + 5` |
| `-=`     | `x -= 3` | `x = x - 3` |
| `*=`     | `x *= 2` | `x = x * 2` |
| `/=`     | `x /= 4` | `x = x / 4` |
| `%=`     | `x %= 2` | `x = x % 2` |

---

## 🔁 Operator Perbandingan

Digunakan untuk membandingkan dua nilai dan mengembalikan nilai boolean (`true` atau `false`).

| Operator | Fungsi                  | Contoh                |
| -------- | ----------------------- | --------------------- |
| `==`     | Sama nilai (tanpa tipe) | `"5" == 5` → `true`   |
| `===`    | Sama nilai & tipe       | `"5" === 5` → `false` |
| `!=`     | Tidak sama (tanpa tipe) | `"5" != 5` → `false`  |
| `!==`    | Tidak sama nilai/tipe   | `"5" !== 5` → `true`  |
| `>`      | Lebih besar             | `7 > 5` → `true`      |
| `<`      | Lebih kecil             | `3 < 2` → `false`     |
| `>=`     | Lebih besar atau sama   | `4 >= 4` → `true`     |
| `<=`     | Lebih kecil atau sama   | `6 <= 5` → `false`    |

---

## 🧠 Perbedaan `==` vs `===`

```javascript
console.log("5" == 5);  // true (tipe diabaikan)
console.log("5" === 5); // false (tipe diperiksa)
```

Gunakan `===` dan `!==` untuk **perbandingan yang lebih aman** (strict equality).

---

## ⚡ Operator Logika

Digunakan untuk ekspresi boolean kompleks:

| Operator | Nama | Contoh                    |    |        |   |                |
| -------- | ---- | ------------------------- | -- | ------ | - | -------------- |
| `&&`     | AND  | `true && false` → `false` |    |        |   |                |
| \`       |      | \`                        | OR | \`true |   | false`→`true\` |
| `!`      | NOT  | `!true` → `false`         |    |        |   |                |

```javascript
let isOnline = true;
let isLogin = false;

console.log(isOnline && isLogin); // false
console.log(isOnline || isLogin); // true
console.log(!isOnline);           // false
```

---

## 🔄 Operator Increment & Decrement

Digunakan untuk menambah atau mengurangi nilai 1.

```javascript
let x = 5;

x++; // x = x + 1
--x; // x = x - 1
```

> 💡 `x++` (post-increment) vs `++x` (pre-increment): hasilnya sama tapi timing evaluasi berbeda.

---

## ❓ Operator Ternary

Operator pendek untuk `if else`.

```javascript
let umur = 18;
let status = umur >= 17 ? "Dewasa" : "Anak-anak";
console.log(status); // Dewasa
```

---

## 🧪 Tantangan Cepat

1. Hitung sisa bagi dari 17 dibagi 4
2. Cek apakah angka `8` lebih besar dari `5` dan kurang dari `10`
3. Gunakan ternary untuk mengecek apakah nilai `nilai = 75` lulus atau tidak

```javascript
let sisa = 17 % 4;
let cek = 8 > 5 && 8 < 10;
let nilai = 75;
let status = nilai >= 70 ? "Lulus" : "Gagal";
```

---

> “Operator adalah jembatan logika antara niat kita dan hasil program.”

Selanjutnya: Kita akan bahas **struktur kontrol** seperti `if`, `else`, `switch`, dan `loop`.