# ⏳ Top-level Await

Sejak ES2022, JavaScript mendukung penggunaan `await` di level atas modul (top-level), tanpa harus berada dalam fungsi async. Ini memberikan fleksibilitas lebih dalam modul modern (ES Modules / ESM).

## ⚙️ Syarat Penggunaan

Top-level `await` hanya dapat digunakan di dalam **ES Modules (ESM)**. Jadi, file JavaScript kamu harus memiliki `"type": "module"` di `package.json`, atau berekstensi `.mjs`.

```json
// package.json
{
  "type": "module"
}
````

Atau:

```bash
node --input-type=module
```

## 📥 Contoh Penggunaan

```js
// fetch-data.js
const response = await fetch('https://api.example.com/data');
const data = await response.json();

console.log(data);
```

Tanpa perlu membungkusnya dalam fungsi async!

## 🔄 Dampak Terhadap Modul Lain

Karena `await` bersifat asynchronous, modul lain yang mengimpor file ini harus menunggu hingga `await` selesai.

```js
// main.js
import './fetch-data.js'; // Akan menunggu hingga data selesai di-fetch
```

## ❗Catatan Penting

* Tidak bisa digunakan dalam script biasa (`<script>` di HTML) kecuali dengan `type="module"`.
* Jika digunakan di CommonJS (`require`), akan error.

## ✅ Kapan Digunakan?

Gunakan top-level await ketika:

* Kamu perlu load data sebelum modul siap digunakan.
* Kamu menulis utilitas modular berbasis async.
* Kamu menggunakan bundler/modul modern (Vite, ESBuild, Webpack ESM, dll).

## 📚 Referensi

* [MDN Web Docs - Top-level await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await#top-level_await)
* [TC39 Proposal](https://github.com/tc39/proposal-top-level-await)

```

---

Siap lanjut ke materi berikutnya? Mungkin `fetch` atau `API` eksternal?
```
