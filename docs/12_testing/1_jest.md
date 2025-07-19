# 🧪 Pengenalan Jest

[Jest](https://jestjs.io/) adalah framework testing JavaScript yang powerful dan mudah digunakan. Dikembangkan oleh Meta (Facebook), Jest sangat populer dalam pengujian unit dan integrasi, khususnya dalam proyek React — tetapi juga bisa digunakan untuk aplikasi JavaScript murni (vanilla JS), Node.js, hingga TypeScript.

## 🚀 Fitur Unggulan Jest

- **Zero config** – langsung bisa digunakan.
- **Snapshot testing** – untuk menguji struktur output seperti HTML/JSON.
- **Mocking built-in** – mudah membuat mock fungsi/module.
- **Test coverage** – laporan seberapa banyak kode yang diuji.
- **Runs in parallel** – performa cepat dengan worker threads.

---

## 📦 Instalasi

```bash
npm install --save-dev jest
````

Tambahkan ke `package.json`:

```json
"scripts": {
  "test": "jest"
}
```

Untuk proyek `type: module`, tambahkan opsi:

```json
"type": "module",
"jest": {
  "testEnvironment": "node"
}
```

---

## 🧪 Contoh Pengujian Dasar

Misal kita punya fungsi:

```js
// sum.js
export function sum(a, b) {
  return a + b;
}
```

### Buat file test:

```js
// sum.test.js
import { sum } from './sum.js';

test('menjumlahkan 1 + 2 = 3', () => {
  expect(sum(1, 2)).toBe(3);
});
```

### Jalankan test:

```bash
npm test
```

---

## 🔍 Metode Expect Populer

| Fungsi         | Penjelasan                               |
| -------------- | ---------------------------------------- |
| `toBe()`       | Kecocokan identik (`===`)                |
| `toEqual()`    | Untuk objek/array (deep equality)        |
| `toBeTruthy()` | Nilai yang dianggap true                 |
| `toBeFalsy()`  | Nilai yang dianggap false                |
| `toContain()`  | Cek apakah array/string mengandung nilai |
| `toThrow()`    | Cek error dilempar atau tidak            |

---

## 🧪 Coverage Test

Untuk melihat cakupan pengujian:

```bash
npx jest --coverage
```

Akan muncul laporan detail berapa persen kode yang diuji.

---

## 📁 Struktur Proyek Rekomendasi

```
/project-root
  ├── src/
  │   └── sum.js
  ├── tests/
  │   └── sum.test.js
  └── package.json
```

---

## 🔗 Referensi Resmi

* [Jest Docs](https://jestjs.io/docs/getting-started)
* [Awesome Jest](https://github.com/jest-community/awesome-jest)

```