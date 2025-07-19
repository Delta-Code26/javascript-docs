# Nullish Coalescing (`??`)
description: Memahami operator nullish coalescing (`??`) di JavaScript untuk menangani nilai `null` atau `undefined` dengan cara yang lebih aman dan jelas.

---

## ❓ Apa Itu Nullish Coalescing (`??`)

Nullish coalescing operator (`??`) adalah fitur JavaScript modern yang digunakan untuk memberikan **nilai default** jika suatu ekspresi bernilai `null` atau `undefined`.

> 🧠 Diperkenalkan di **ES2020**, operator ini sering digunakan bersamaan dengan optional chaining (`?.`).

---

## 🔍 Perbedaan dengan Operator `||`

Sebelum adanya `??`, kita sering menggunakan `||` untuk fallback:

```javascript
let username = input || 'Guest';
````

Namun `||` akan **menganggap semua falsy value** (seperti `0`, `''`, `false`) sebagai alasan untuk menggunakan default.

Contoh:

```javascript
let count = 0;
console.log(count || 10); // 10 ❌ (padahal 0 adalah nilai valid)
```

---

## ✅ Solusi dengan `??`

```javascript
let count = 0;
console.log(count ?? 10); // 0 ✅ (karena count bukan null/undefined)
```

---

## 🧪 Contoh Penggunaan

```javascript
let userInput;
let finalValue = userInput ?? 'Default';
console.log(finalValue); // "Default"
```

```javascript
let value = null;
console.log(value ?? 'Fallback'); // "Fallback"
```

```javascript
let zero = 0;
console.log(zero ?? 100); // 0 ✅
```

---

## ⚠️ Hanya Berlaku untuk `null` dan `undefined`

Operator `??` **tidak** menganggap `''`, `false`, atau `0` sebagai nullish:

| Nilai                | `??` Akan Gunakan Default? |
| -------------------- | -------------------------- |
| `null`               | ✅ Ya                       |
| `undefined`          | ✅ Ya                       |
| `false`              | ❌ Tidak                    |
| `0`                  | ❌ Tidak                    |
| `''` (string kosong) | ❌ Tidak                    |

---

## 🔄 Kombinasi dengan Optional Chaining

```javascript
let city = user?.address?.city ?? 'Belum Diatur';
console.log(city);
```

---

## 📌 Kapan Digunakan?

Gunakan `??` saat:

* Ingin memberikan nilai default hanya ketika `null` atau `undefined`
* Menghindari fallback yang salah ketika nilai seperti `0`, `false`, atau `''` masih valid

---

## 📎 Catatan Tambahan

* Jangan mencampur `??` dengan `||` atau `&&` tanpa tanda kurung, karena bisa menimbulkan error parsing:

```javascript
// ❌ SyntaxError
// let x = a || b ?? c;

// ✅ Gunakan tanda kurung
let x = (a || b) ?? c;
```

---

🧠 **Kesimpulan:**
Gunakan `??` ketika kamu ingin memberikan nilai cadangan yang **aman dan akurat**, hanya saat nilai benar-benar tidak tersedia (`null` atau `undefined`).

```