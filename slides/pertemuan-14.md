---
title: Customize Bootstrap
version: 1.0.0
theme: default
header: Customize Bootstrap
footer: https://github.com/universitas-ibbi/ibbi-si-ii-m1
paginate: true
marp: true
---

<!--
_class: lead
_paginate: skip
-->

# Customize Bootstrap

---

### **Pengenalan Kustomisasi di Bootstrap 5**

Bootstrap 5 sangat fleksibel dan memungkinkan kustomisasi tampilan dengan berbagai cara, antara lain:

- Mengganti warna, ukuran, atau bentuk komponen.
- Menambahkan utilitas baru.
- Membuang komponen yang tidak dipakai.

---

**Tingkat kustomisasi:**

- _Dasar:_ Override CSS.
- _Lanjutan:_ Gunakan file Sass untuk mengubah variabel, utility API, dan build sendiri Bootstrap.

---

### **Kustomisasi Dasar (Tanpa Build Tools)**

#### ✅ Override Kelas Bootstrap

**Contoh: Ubah warna tombol primary**

```html
<!-- Default Bootstrap -->
<button class="btn btn-primary">Klik Saya</button>

<!-- Override CSS -->
<style>
  .btn-primary {
    background-color: #ff5722; /* Orange */
    border-color: #ff5722;
  }
</style>
```

> **Catatan:** Tempatkan CSS override Anda **setelah** `bootstrap.min.css` agar efektif.

---

## 🔷 **Colors (Warna Tema)**

Digunakan di tombol, teks, latar belakang, border, dan komponen lain.

```scss
$primary: #0d6efd;
$secondary: #6c757d;
$success: #198754;
```

```scss
$theme-colors: (
  "primary": $primary,
  "secondary": $secondary,
  "success": $success,
);
```

---

## 🔷 **Spacers (Jarak)**

Digunakan untuk padding dan margin utility seperti `.p-3`, `.m-2`.

```scss
$spacer: 1rem;

$spacers: (
  0: 0,
  1: $spacer * 0.25,
  2: $spacer * 0.5,
  3: $spacer,
  4: $spacer * 1.5,
  5: $spacer * 3,
);
```

---

### **Kustomisasi Lanjutan (Sass & Build Sendiri)**

#### ✅ Setup Proyek Bootstrap via Source

1. **Inisialisasi Proyek**

```bash
npm init -y
npm install bootstrap@5.3.0 sass
```

2. **Struktur Folder**

```
/scss
  - custom.scss
/dist
  - style.css (hasil kompilasi)
```

---

#### ✅ Mengubah Variabel Sass

File `custom.scss`:

```scss
// Override
$primary: #ff5722; // Warna oranye sebagai primary

// Import seluruh Bootstrap
@import "node_modules/bootstrap/scss/bootstrap";
```

Lalu compile:

```bash
npx sass scss/custom.scss dist/style.css
```

---

#### Menambah Warna Tema (Color Palette)

```scss
$custom-color: #ffcc00;

$theme-colors: (
  "custom": $custom-color,
);

@import "node_modules/bootstrap/scss/bootstrap";
```

```html
<button class="btn btn-custom">Tombol Kuning</button>
```

---

#### ✅ Tambahkan Utility Kustom

```scss
$utilities: map-merge(
  $utilities,
  (
    "rotate": (
      property: transform,
      class: rotate,
      values: (
        0: rotate(0deg),
        45: rotate(45deg),
        90: rotate(90deg),
      ),
    ),
  )
);
```

Lalu gunakan seperti:

```html
<div class="rotate-45">Saya diputar</div>
```
