# Struktur Kontrol dalam JavaScript

Struktur kontrol adalah dasar dalam membentuk alur program. JavaScript menyediakan berbagai macam struktur kontrol untuk membantu kita membuat keputusan dan mengulang perintah sesuai kondisi tertentu.

## 1. Pernyataan Kondisional (Conditional Statements)

### `if`, `else if`, dan `else`

```javascript
let nilai = 85;

if (nilai >= 90) {
  console.log("A");
} else if (nilai >= 80) {
  console.log("B");
} else {
  console.log("C");
}
````

### `switch`

```javascript
let hari = "Senin";

switch (hari) {
  case "Senin":
    console.log("Hari kerja");
    break;
  case "Sabtu":
  case "Minggu":
    console.log("Hari libur");
    break;
  default:
    console.log("Hari tidak valid");
}
```

## 2. Perulangan (Loops)

### `for`

```javascript
for (let i = 0; i < 5; i++) {
  console.log(`Iterasi ke-${i}`);
}
```

### `while`

```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

### `do...while`

```javascript
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```

## 3. `break` dan `continue`

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 3) continue; // lewati angka 3
  if (i === 7) break;    // hentikan loop saat i = 7
  console.log(i);
}
```

---

> Struktur kontrol membentuk pondasi dalam menciptakan logika program yang fleksibel dan cerdas.