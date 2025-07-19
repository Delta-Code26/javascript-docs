# Closure di JavaScript

Closure adalah kombinasi antara fungsi dan lingkungan leksikal (lexical environment) di mana fungsi tersebut didefinisikan. Closure memungkinkan fungsi mengakses variabel dari luar cakupannya (scope) meskipun fungsi tersebut dieksekusi di luar scope aslinya.

## Mengapa Closure Penting?

Closure memungkinkan:
- Data tetap privat (encapsulation).
- Pembuatan fungsi dengan konfigurasi khusus (partial application).
- Penggunaan fungsi sebagai penghasil fungsi lainnya (function factory).

## Contoh Closure

```javascript
function pembuatPenghitung() {
  let hitung = 0;
  return function () {
    hitung++;
    return hitung;
  };
}

const tambah = pembuatPenghitung();

console.log(tambah()); // 1
console.log(tambah()); // 2
console.log(tambah()); // 3
````

Pada contoh di atas:

* `hitung` adalah variabel lokal dari `pembuatPenghitung`.
* Fungsi anonim yang dikembalikan tetap dapat mengakses `hitung` karena merupakan **closure**.

## Keunggulan Closure

* **Privasi**: Variabel di dalam closure tidak dapat diakses langsung dari luar.
* **Kontrol State**: Berguna dalam callback dan asynchronous programming.
* **Modularisasi**: Closure dapat digunakan untuk membuat module pattern.

## Kapan Menggunakan Closure?

* Saat ingin menyimpan state antar pemanggilan fungsi.
* Saat membuat fungsi yang dapat dikustomisasi.
* Saat ingin menjaga data agar tetap private.

> 📦 Closure adalah salah satu fitur paling kuat dan paling sering digunakan dalam JavaScript modern, terutama dalam pengembangan berbasis event-driven dan functional programming.