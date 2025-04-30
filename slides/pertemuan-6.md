---
title: Layout dengan CSS
version: 1.0.0
theme: default
header: Layout dengan CSS
footer: https://github.com/universitas-ibbi/ibbi-si-ii-m1
paginate: true
marp: true
---

<!--
_class: lead
_paginate: skip
-->

# Layout dengan CSS

![bg right cover](./images/pertemuan-6.avif)

---

### 🎯 **Judul dan Tujuan Pembelajaran**

- **Judul:** _Layout dengan CSS_
- **Tujuan Pembelajaran:**
  - Mahasiswa dapat memahami konsep layout menggunakan properti CSS: `position` dan `display`.
  - Mahasiswa mampu menerapkan properti tersebut untuk membuat tampilan halaman web yang rapi dan responsif.

---

<!--
_class: lead
_paginate: skip
-->

## Position

---

### **Konsep Dasar Positioning**

**Positioning** dalam CSS mengontrol bagaimana elemen ditempatkan di dalam dokumen HTML. Ada beberapa jenis positioning yang digunakan untuk mengatur posisi elemen, dan setiap jenis memiliki cara kerja yang berbeda dalam mengatur tata letak. Berikut adalah penjelasan lengkap dengan contoh untuk masing-masing tipe positioning:

---

### **`position: static;` (default)**

- Ini adalah nilai default untuk semua elemen HTML. Elemen dengan `position: static` akan ditempatkan di halaman sesuai dengan alur normal dokumen (flow normal).
- Elemen dengan `static` tidak terpengaruh oleh properti seperti `top`, `right`, `bottom`, atau `left`.
- Elemen tersebut akan ditempatkan sesuai dengan urutan dalam HTML.

---

```html
<div class="static-box">Static Box</div>
```

```css
.static-box {
  position: static;
  top: 20px; /* Tidak berpengaruh */
  left: 20px; /* Tidak berpengaruh */
  background-color: lightblue;
  padding: 20px;
}
```

- **Hasil:** Elemen akan mengikuti alur dokumen, artinya elemen tersebut tidak bergerak meskipun ada deklarasi `top` atau `left`.

---

### **`position: relative;`**

- Elemen dengan `position: relative` tetap berada di dalam alur dokumen normal, namun dapat dipindahkan relatif terhadap posisinya yang asli menggunakan properti `top`, `right`, `bottom`, atau `left`.
- Penggunaan `relative` seringkali digunakan untuk membuat elemen berpindah sedikit dari posisi normalnya.

---

```html
<div class="relative-box">Relative Box</div>
```

```css
.relative-box {
  position: relative;
  top: 20px; /* Pindahkan elemen 20px ke bawah dari posisi normal */
  left: 30px; /* Pindahkan elemen 30px ke kanan dari posisi normal */
  background-color: lightgreen;
  padding: 20px;
}
```

- **Hasil:** Elemen akan terlihat bergeser 20px ke bawah dan 30px ke kanan, tetapi tetap mempertahankan alur normalnya di dalam dokumen.

---

### **`position: absolute;`**

- Elemen dengan `position: absolute` akan diposisikan relatif terhadap elemen terdekat yang memiliki `position: relative`, `absolute`, atau `fixed`. Jika tidak ada elemen yang diposisikan, maka elemen akan diposisikan relatif terhadap elemen `<html>`.
- Elemen ini akan keluar dari alur dokumen dan tidak mempengaruhi posisi elemen lain di halaman.

---

```html
<div class="parent">
  <div class="absolute-box">Absolute Box</div>
</div>
```

```css
.parent {
  position: relative;
  height: 200px;
  background-color: lightgray;
}
.absolute-box {
  position: absolute;
  top: 50px; /* Posisikan 50px dari atas parent */
  left: 100px; /* Posisikan 100px dari kiri parent */
  background-color: lightcoral;
  padding: 20px;
}
```

- **Hasil:** Elemen `.absolute-box` akan diposisikan 50px dari atas dan 100px dari kiri elemen `.parent`. Elemen ini tidak akan mempengaruhi layout elemen lain.

---

### **`position: fixed;`**

- Elemen dengan `position: fixed` diposisikan relatif terhadap jendela tampilan (viewport). Artinya, elemen ini tetap berada di posisi yang sama saat halaman digulir (scroll) ke atas atau ke bawah.
- Posisi elemen `fixed` akan tetap di layar meskipun halaman digulir.

---

```html
<div class="fixed-box">Fixed Box</div>
```

```css
.fixed-box {
  position: fixed;
  top: 10px; /* Posisikan 10px dari atas viewport */
  right: 10px; /* Posisikan 10px dari kanan viewport */
  background-color: lightgoldenrodyellow;
  padding: 20px;
}
```

- **Hasil:** Elemen `.fixed-box` akan tetap berada di pojok kanan atas layar, meskipun halaman digulir ke bawah.

---

### **5. `position: sticky;`**

- Elemen dengan `position: sticky` bertindak seperti elemen dengan `relative` sampai halaman digulir melewati batas yang ditentukan. Setelah melewati batas, elemen tersebut akan "menempel" (sticky) pada posisi yang ditentukan, biasanya di bagian atas layar.
- Digunakan untuk elemen seperti header atau navbar yang ingin tetap terlihat saat scroll.

---

```html
<div class="sticky-box">Sticky Box</div>
<div class="content">Content...</div>
```

```css
.sticky-box {
  position: sticky;
  top: 0; /* Menempel di bagian atas viewport saat digulir */
  background-color: lightpink;
  padding: 20px;
}
.content {
  height: 2000px; /* Cukup panjang agar kita bisa menggulir */
  background-color: lightgray;
}
```

- **Hasil:** Elemen `.sticky-box` akan tetap berada di atas layar saat scroll, sampai posisi elemen tersebut melewati batas viewport, kemudian akan "menempel" di bagian atas layar.

---

### **Ringkasan Tabel Perbandingan**

| **Positioning Type** | **Pengaruh pada Layout**              | **Penjelasan**                                                                 |
| -------------------- | ------------------------------------- | ------------------------------------------------------------------------------ |
| `static`             | Tidak berubah                         | Elemen mengikuti alur normal dokumen                                           |
| `relative`           | Pindah relatif terhadap posisi semula | Elemen bergeser tapi tetap dalam alur dokumen                                  |
| `absolute`           | Keluar dari alur dokumen              | Elemen diposisikan relatif terhadap parent yang diposisikan atau `html`        |
| `fixed`              | Tetap di layar saat scroll            | Elemen diposisikan relatif terhadap viewport dan tidak terpengaruh oleh scroll |
| `sticky`             | Menempel di posisi tertentu           | Elemen berpindah dengan scroll, lalu "menempel" saat mencapai posisi tertentu  |

---

**Kesimpulan:**

- `position: static` adalah pengaturan default, sedangkan `relative`, `absolute`, `fixed`, dan `sticky` memberikan kontrol lebih lanjut atas bagaimana elemen diposisikan dan dipindahkan dalam halaman.
- Masing-masing positioning cocok untuk skenario yang berbeda, misalnya untuk membuat navbar tetap di atas (fixed), membuat elemen keluar dari alur dokumen (absolute), atau membuat elemen menempel saat scroll (sticky).

---

<!--
_class: lead
_paginate: skip
-->

# Display

---

### **`display: block;`**

Elemen dengan properti **`display: block;`** akan memulai baris baru (break line) dan mengambil seluruh lebar kontainer, dari kiri ke kanan.

- **Ciri-ciri:**

  - Membuat elemen menjadi _blok_, sehingga elemen lainnya akan muncul di bawahnya.
  - Menempati seluruh lebar kontainer.
  - Elemen ini bisa memiliki margin, padding, dan lebar yang diatur.

---

```html
<div class="box">Ini adalah box dengan display block</div>
<div class="box">Ini box lainnya dengan display block</div>
```

```css
.box {
  display: block;
  width: 80%;
  background-color: lightblue;
  padding: 20px;
  margin: 10px auto;
}
```

---

**Penjelasan:**  
Elemen `<div>` yang memiliki `display: block` akan ditempatkan di baris baru dan mengambil lebar 80% dari kontainer induknya.

---

### **`display: inline-block;`**

Elemen dengan **`display: inline-block;`** dapat berada di samping elemen lain, namun tetap mempertahankan sifat elemen blok (dapat diatur lebar dan tingginya).

- **Ciri-ciri:**

  - Elemen ini berperilaku seperti elemen **inline**, tetapi memungkinkan untuk diatur lebar dan tinggi.
  - Elemen-elemen dengan `inline-block` dapat berada di samping satu sama lain dalam satu baris.
  - Bisa digunakan untuk elemen yang butuh pengaturan ukuran seperti gambar atau tombol dalam satu baris.

---

```html
<div class="box">Box 1</div>
<div class="box">Box 2</div>
<div class="box">Box 3</div>
```

```css
.box {
  display: inline-block;
  width: 30%;
  background-color: lightgreen;
  padding: 20px;
  margin: 10px;
  text-align: center;
}
```

---

**Penjelasan:**  
Dengan `display: inline-block`, ketiga kotak akan berada dalam satu baris (inline), tetapi tetap bisa diatur lebar dan tingginya.

---

### **`display: none;`**

Elemen dengan **`display: none;`** tidak akan ditampilkan pada halaman dan tidak akan mempengaruhi layout sama sekali.

- **Ciri-ciri:**

  - Elemen tidak akan muncul di halaman dan tidak akan mengambil ruang di layout.
  - Biasanya digunakan untuk menyembunyikan elemen sementara menggunakan JavaScript.

---

```html
<div class="box">Box 1</div>
<div class="box hidden">Box 2 (disembunyikan)</div>
<div class="box">Box 3</div>
```

```css
.hidden {
  display: none;
}
.box {
  background-color: lightcoral;
  padding: 20px;
  margin: 10px;
}
```

---

**Penjelasan:**  
Box 2 tidak akan ditampilkan karena menggunakan `display: none`, sedangkan box 1 dan box 3 tetap tampil.

---

### **`display: flex;`**

Elemen dengan **`display: flex;`** membuat elemen anak di dalam kontainer untuk diatur menggunakan model Flexbox. Flexbox memberikan kontrol yang lebih besar terhadap penataan item dalam satu dimensi (horizontal atau vertikal).

- **Ciri-ciri:**

  - Elemen anak akan disusun dalam satu baris atau kolom.
  - Menggunakan properti seperti `justify-content`, `align-items`, dan `flex-direction` untuk mengontrol posisi elemen.
  - Lebih fleksibel dan responsif dibandingkan model layout tradisional seperti `float`.

---

```html
<div class="container">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>
```

```css
.container {
  display: flex;
  justify-content: space-between; /* Membagi ruang antar elemen */
}

.box {
  background-color: lightyellow;
  padding: 20px;
  width: 30%;
  text-align: center;
}
```

---

**Penjelasan:**  
Dengan `display: flex`, ketiga elemen `.box` akan berada dalam satu baris, dan ruang di antara mereka dibagi secara merata.

---

### **`display: grid;`**

Elemen dengan **`display: grid;`** memungkinkan pembuatan layout dua dimensi (baik baris dan kolom) yang lebih kompleks dan terstruktur.

- **Ciri-ciri:**

  - Menyusun elemen dalam grid dengan kolom dan baris yang bisa dikendalikan.
  - Lebih cocok untuk layout kompleks yang melibatkan pengaturan baik di horizontal maupun vertikal.
  - Menggunakan properti seperti `grid-template-rows`, `grid-template-columns`, `gap`, dan lainnya.

---

```html
<div class="container">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>
```

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr; /* Membagi kontainer menjadi 3 kolom */
  gap: 10px;
}

.box {
  background-color: lightpink;
  padding: 20px;
  text-align: center;
}
```

---

**Penjelasan:**  
Dengan `display: grid`, elemen `.box` disusun dalam tiga kolom yang memiliki lebar yang sama (menggunakan unit `fr` untuk fraksi dari lebar kontainer).

---

### **Perbandingan Singkat**

| **Property**                 | **Penjelasan**                                                                                      | **Contoh**                                |
| ---------------------------- | --------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| **`display: block;`**        | Elemen menempati seluruh lebar kontainer dan membuat baris baru.                                    | Digunakan untuk elemen seperti `<div>`.   |
| **`display: inline-block;`** | Elemen berada dalam satu baris, tetapi bisa diatur lebar dan tingginya.                             | Digunakan untuk tombol, gambar, dll.      |
| **`display: none;`**         | Elemen tidak ditampilkan dan tidak mempengaruhi layout.                                             | Menyembunyikan elemen.                    |
| **`display: flex;`**         | Membuat layout satu dimensi (horizontal atau vertikal) dengan kontrol lebih terhadap posisi elemen. | Digunakan untuk navbar, card layout, dll. |
| **`display: grid;`**         | Membuat layout dua dimensi (baris dan kolom) yang sangat fleksibel dan kuat.                        | Digunakan untuk layout kompleks, grid.    |

---

<!--
_class: lead
_paginate: skip
-->

# Layout

---

## 🎯 **Layout dengan Table, Float, Flex, dan Grid**

### **1. Layout dengan Table**

Layout menggunakan tabel adalah metode lama yang sering digunakan sebelum hadirnya CSS modern. Meskipun sudah tidak direkomendasikan untuk layout kompleks, tetapi masih berguna untuk memahami dasar-dasar tata letak.

---

### **2. Layout dengan Float**

Float adalah properti lama di CSS yang digunakan untuk mengatur elemen menjadi terletak di sebelah kiri atau kanan elemen lainnya.

---

### **3. Layout dengan Flexbox**

Flexbox adalah metode modern yang lebih fleksibel daripada float. Flexbox memudahkan pengaturan elemen dalam satu dimensi (vertikal atau horizontal).

---

### **4. Layout dengan Grid**

CSS Grid Layout adalah metode yang lebih canggih dan kuat, memungkinkan kita untuk mengatur elemen dalam dua dimensi (baris dan kolom).

---

### **Perbandingan Metode Layout**

| Metode      | Keunggulan                                      | Kelemahan                                             |
| ----------- | ----------------------------------------------- | ----------------------------------------------------- |
| **Table**   | Sederhana, mudah dipahami                       | Tidak fleksibel, tidak responsif, tidak modern        |
| **Float**   | Menyusun elemen secara horizontal/vertikal      | Sulit diatur ulang, kadang membutuhkan clear          |
| **Flexbox** | Fleksibel, mudah diatur secara responsif        | Hanya untuk layout satu dimensi (vertikal/horizontal) |
| **Grid**    | Sangat kuat untuk layout dua dimensi, fleksibel | Butuh pemahaman lebih mendalam                        |
