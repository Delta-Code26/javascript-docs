# Pewarisan (Inheritance)

Pewarisan adalah konsep di mana sebuah objek dapat mewarisi properti dan method dari objek lain. Di JavaScript, pewarisan sering digunakan untuk membangun hierarki objek, memungkinkan kita menulis kode yang lebih reusable dan terstruktur.

---

## 👨‍👩‍👧 Pewarisan Melalui Prototype

Setiap objek di JavaScript memiliki properti internal yang disebut `[[Prototype]]`, yang dapat diakses melalui `__proto__` atau lebih disarankan melalui `Object.getPrototypeOf()`.

```javascript
const manusia = {
  makan() {
    console.log("Sedang makan");
  }
};

const mahasiswa = {
  belajar() {
    console.log("Sedang belajar");
  }
};

Object.setPrototypeOf(mahasiswa, manusia);

mahasiswa.belajar(); // Sedang belajar
mahasiswa.makan();   // Sedang makan (diturunkan dari manusia)
````

---

## 🏗️ Pewarisan dengan Function Constructor

```javascript
function Kendaraan(merk) {
  this.merk = merk;
}
Kendaraan.prototype.hidupkan = function () {
  console.log(`${this.merk} dinyalakan`);
};

function Mobil(merk, tipe) {
  Kendaraan.call(this, merk);
  this.tipe = tipe;
}
Mobil.prototype = Object.create(Kendaraan.prototype);
Mobil.prototype.constructor = Mobil;

const civic = new Mobil("Honda", "Civic");
civic.hidupkan(); // Honda dinyalakan
```

---

## 🧬 Pewarisan dengan ES6 Class

ES6 memperkenalkan sintaks `class` yang membuat pewarisan lebih bersih dan mudah dibaca.

```javascript
class Hewan {
  constructor(nama) {
    this.nama = nama;
  }

  suara() {
    console.log(`${this.nama} bersuara`);
  }
}

class Kucing extends Hewan {
  suara() {
    console.log(`${this.nama} meong~`);
  }
}

const pus = new Kucing("Pus");
pus.suara(); // Pus meong~
```

---

## 🧠 `super()` dan Overriding

Method `super()` digunakan untuk memanggil constructor atau method dari parent class.

```javascript
class Kendaraan {
  constructor(merk) {
    this.merk = merk;
  }

  info() {
    return `Kendaraan: ${this.merk}`;
  }
}

class Motor extends Kendaraan {
  constructor(merk, cc) {
    super(merk); // memanggil constructor Kendaraan
    this.cc = cc;
  }

  info() {
    return `${super.info()} - ${this.cc} cc`;
  }
}

const vixion = new Motor("Yamaha", 150);
console.log(vixion.info()); // Kendaraan: Yamaha - 150 cc
```

---

## ✨ Catatan Penting

* Gunakan `class` jika kamu ingin kode yang lebih modern dan rapi.
* Pewarisan dapat membuat kode kompleks jika digunakan berlebihan — gunakan dengan bijak.
* Komposisi bisa menjadi alternatif yang lebih fleksibel dibanding pewarisan.

---

> "Favor composition over inheritance." – Prinsip penting dalam desain perangkat lunak modern.

```