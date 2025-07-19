# 🔍 Seleksi Elemen DOM

DOM (Document Object Model) adalah representasi struktur halaman web yang dapat diakses dan dimanipulasi menggunakan JavaScript.

Langkah pertama untuk memanipulasi DOM adalah *menyeleksi elemen* yang ingin dimodifikasi.

---

## 📌 `document.getElementById()`

Menyeleksi elemen berdasarkan nilai `id`.

```javascript
const heading = document.getElementById("judul");
console.log(heading.textContent);
````

---

## 📌 `document.getElementsByClassName()`

Menyeleksi elemen berdasarkan class. Mengembalikan HTMLCollection (mirip array).

```javascript
const kotak = document.getElementsByClassName("kotak");
console.log(kotak[0]);
```

---

## 📌 `document.getElementsByTagName()`

Menyeleksi elemen berdasarkan tag HTML.

```javascript
const paragraf = document.getElementsByTagName("p");
console.log(paragraf.length);
```

---

## 📌 `document.querySelector()`

Menyeleksi elemen pertama yang cocok dengan selector CSS.

```javascript
const tombol = document.querySelector(".btn");
```

---

## 📌 `document.querySelectorAll()`

Menyeleksi semua elemen yang cocok dengan selector CSS. Mengembalikan NodeList.

```javascript
const semuaKotak = document.querySelectorAll(".kotak");
semuaKotak.forEach(k => console.log(k));
```

---

## 🧠 Perbedaan `getElement` vs `querySelector`

| Metode                     | Hasil          | Selector seperti CSS? |
| -------------------------- | -------------- | --------------------- |
| `getElementById()`         | 1 elemen (ID)  | ❌ Tidak               |
| `getElementsByClassName()` | HTMLCollection | ❌ Tidak               |
| `querySelector()`          | 1 elemen       | ✅ Ya                  |
| `querySelectorAll()`       | NodeList       | ✅ Ya                  |

---

## 🧪 Tips Tambahan

* NodeList dari `querySelectorAll()` bisa langsung di-*loop* pakai `.forEach()`.
* Gunakan `const`/`let` untuk menyimpan elemen agar bisa digunakan kembali.
* Hindari terlalu sering seleksi ulang DOM yang sama untuk efisiensi.

---

## 📚 Kesimpulan

Menyeleksi elemen adalah fondasi dalam memanipulasi DOM. Gunakan metode yang paling sesuai dengan kebutuhan: berdasarkan `id`, `class`, `tag`, atau selector CSS.