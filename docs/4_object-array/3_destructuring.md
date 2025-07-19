# 🧩 Destructuring di JavaScript

Destructuring adalah fitur ES6 yang memungkinkan kita mengekstrak nilai dari array atau properti dari objek ke dalam variabel yang terpisah dengan sintaks yang lebih ringkas dan bersih.

---

## 📦 Array Destructuring

```javascript
const buah = ['apel', 'mangga', 'jeruk'];

const [buah1, buah2, buah3] = buah;

console.log(buah1); // apel
console.log(buah2); // mangga
console.log(buah3); // jeruk
````

### ✅ Skip item tertentu

```javascript
const [,, buahTerakhir] = buah;
console.log(buahTerakhir); // jeruk
```

---

## 🧱 Object Destructuring

```javascript
const user = {
  nama: "Budi",
  umur: 25,
  negara: "Indonesia"
};

const { nama, umur, negara } = user;

console.log(nama);   // Budi
console.log(umur);   // 25
console.log(negara); // Indonesia
```

### 🧪 Rename saat destructuring

```javascript
const { nama: namaLengkap } = user;
console.log(namaLengkap); // Budi
```

### 🧪 Default value

```javascript
const { pekerjaan = 'Belum diketahui' } = user;
console.log(pekerjaan); // Belum diketahui
```

---

## 🧠 Destructuring di Parameter Function

```javascript
function tampilkanProfil({ nama, umur }) {
  console.log(`Nama: ${nama}, Umur: ${umur}`);
}

tampilkanProfil(user);
// Output: Nama: Budi, Umur: 25
```

---

## 📚 Kesimpulan

Destructuring membuat kode JavaScript lebih ringkas, jelas, dan efisien, terutama saat bekerja dengan struktur data kompleks. Fitur ini sangat cocok digunakan dalam kombinasi dengan fungsi, array, dan objek besar.