# 🎯 Event pada DOM

Event adalah aksi yang terjadi di dalam browser, seperti klik, hover, input, atau submit. JavaScript memungkinkan kita untuk merespon event tersebut melalui event listener.

## Dasar Event Listener

Gunakan `addEventListener` untuk menambahkan event handler:

```javascript
const tombol = document.querySelector("button");

tombol.addEventListener("click", function() {
  alert("Tombol diklik!");
});
````

## Jenis-Jenis Event Umum

| Event       | Kapan Terjadi                           |
| ----------- | --------------------------------------- |
| `click`     | Saat elemen diklik                      |
| `mouseover` | Saat kursor berada di atas elemen       |
| `mouseout`  | Saat kursor keluar dari elemen          |
| `keydown`   | Saat tombol keyboard ditekan            |
| `submit`    | Saat form dikirim                       |
| `change`    | Saat input atau select berubah          |
| `load`      | Saat halaman atau elemen selesai dimuat |

## Contoh: Event Input

```javascript
const input = document.querySelector("input");
input.addEventListener("input", function() {
  console.log("Isi input:", input.value);
});
```

## Menghapus Event Listener

Gunakan fungsi terpisah agar bisa dihapus:

```javascript
function handlerKlik() {
  alert("Event aktif");
}

tombol.addEventListener("click", handlerKlik);
tombol.removeEventListener("click", handlerKlik);
```

## Event Object

Event listener dapat menerima objek event sebagai parameter untuk informasi tambahan:

```javascript
tombol.addEventListener("click", function(e) {
  console.log("Elemen yang diklik:", e.target);
});
```

## Event Delegation

Gunakan event delegation untuk efisiensi (terutama pada elemen dinamis):

```javascript
document.querySelector("ul").addEventListener("click", function(e) {
  if (e.target.tagName === "LI") {
    alert("Item: " + e.target.textContent);
  }
});
```

---

📌 **Tips**:

* Gunakan event delegation untuk performa dan manajemen yang lebih baik.
* Hindari penggunaan `onclick="..."` langsung di HTML (inline handler), gunakan JavaScript murni.