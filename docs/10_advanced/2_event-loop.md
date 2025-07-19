# ⏳ Event Loop di JavaScript

Event Loop adalah mekanisme di balik layar yang memungkinkan JavaScript (yang bersifat single-threaded) untuk menangani operasi asynchronous seperti pengambilan data dari server tanpa memblokir eksekusi kode lainnya.

## 🔁 Bagaimana Event Loop Bekerja?

1. **Call Stack**  
   Tempat eksekusi fungsi secara sinkron. Fungsi yang dipanggil dimasukkan ke stack, dan dikeluarkan setelah selesai.

2. **Web APIs / Node APIs**  
   Operasi async seperti `setTimeout`, `fetch`, atau event listener tidak langsung masuk ke call stack, tapi ke API lingkungan (browser/Node).

3. **Callback Queue**  
   Setelah operasi async selesai, callback-nya dikirim ke antrian ini, menunggu giliran untuk dieksekusi.

4. **Event Loop**  
   Tugasnya adalah memeriksa apakah call stack kosong. Jika kosong, callback dari queue dimasukkan ke stack untuk dieksekusi.

## 📜 Contoh Sederhana

```javascript
console.log('A');

setTimeout(() => {
  console.log('B');
}, 0);

console.log('C');
````

### Output:

```
A
C
B
```

Meskipun timeout-nya 0ms, callback `console.log('B')` tetap ditunda karena menunggu call stack kosong.

## 🎯 Microtask vs Macrotask

* **Macrotask Queue**: `setTimeout`, `setInterval`, I/O.
* **Microtask Queue**: `Promise.then`, `MutationObserver`.

Microtask selalu diproses sebelum macrotask dalam satu putaran event loop.

### Contoh Microtask vs Macrotask

```javascript
setTimeout(() => console.log('Timeout'), 0);
Promise.resolve().then(() => console.log('Promise'));
console.log('Sync');
```

### Output:

```
Sync
Promise
Timeout
```

## 🧠 Kesimpulan

* JavaScript tetap responsif berkat event loop.
* Microtask dieksekusi sebelum macrotask.
* Pahami event loop untuk debug async dan performa yang lebih baik.

---

```

Jika kamu ingin tambahan visualisasi atau diagram animasi untuk menjelaskan event loop, aku bisa bantu buatkan juga.
```
