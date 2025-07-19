# ✨ Manipulasi DOM

Manipulasi DOM (Document Object Model) adalah proses mengubah struktur, konten, atau gaya halaman web menggunakan JavaScript. Ini memungkinkan kita untuk membuat halaman web yang dinamis dan interaktif.

## Mengubah Teks atau HTML

Gunakan properti `.innerText` atau `.innerHTML` untuk mengubah isi elemen.

```javascript
const judul = document.getElementById("judul");
judul.innerText = "Selamat Datang!";
judul.innerHTML = "<em>Selamat Datang!</em>";
````

## Mengubah Atribut

Gunakan `.setAttribute()` atau properti langsung seperti `.href`, `.src`, dll.

```javascript
const link = document.querySelector("a");
link.setAttribute("href", "https://www.google.com");
link.href = "https://www.google.com";
```

## Mengubah Gaya (Style)

```javascript
const box = document.querySelector(".box");
box.style.backgroundColor = "blue";
box.style.fontSize = "20px";
```

## Menambahkan atau Menghapus Kelas

Gunakan `classList` untuk manipulasi kelas:

```javascript
const tombol = document.querySelector("button");
tombol.classList.add("aktif");
tombol.classList.remove("nonaktif");
tombol.classList.toggle("aktif");
```

## Menambahkan atau Menghapus Elemen

### Menambahkan Elemen

```javascript
const list = document.querySelector("ul");
const itemBaru = document.createElement("li");
itemBaru.textContent = "Item Baru";
list.appendChild(itemBaru);
```

### Menghapus Elemen

```javascript
const itemHapus = document.querySelector("li");
itemHapus.remove();
```

## Menyalin Elemen

```javascript
const original = document.querySelector(".kotak");
const salinan = original.cloneNode(true);
document.body.appendChild(salinan);
```

---

📌 **Tips:**

* Gunakan `appendChild`, `insertBefore`, atau `replaceChild` untuk manipulasi tingkat lanjut.
* Hindari manipulasi DOM secara berlebihan untuk performa yang optimal.