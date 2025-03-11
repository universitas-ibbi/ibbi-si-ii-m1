---
title: Intro
version: 1.0.0
theme: react
header: Intro
footer: https://github.com/universitas-ibbi/ibbi-si-ii-m1
paginate: true
marp: true
---

<!-- 
_class: lead 
_paginate: skip
-->

# Intro

---

# JIMMY, S.Kom, M.Kom
- Full Time Freelance Developer
- Part Time Lecturer - Universitas IBBI

![bg right](./images/linkedin.png)

---

## Web Design

Web design adalah proses merancang tampilan dan pengalaman pengguna (UI/UX) sebuah website, termasuk tata letak, warna, font, gambar, dan interaktivitasnya. Tujuan utama web design adalah menciptakan website yang menarik, fungsional, dan mudah digunakan oleh pengunjung.

---

## Cara Kerja Web

* **User Request** → Browser mengakses www.example.com.
* **DNS Resolving** → Mencari alamat IP domain.
* **HTTP Request** → Permintaan dikirim ke server.
* **Server Memproses** → Mengambil file HTML/CSS/JS atau query ke database.
* **HTTP Response** → Server mengirimkan halaman web.
* **Browser Render** → Menampilkan halaman ke pengguna.

---

## Repository

[https://github.com/universitas-ibbi/ibbi-si-ii-m1](https://github.com/universitas-ibbi/ibbi-si-ii-m1)

- Bahan Belajar
- Contoh Lab
- Info
  
---

## Tools

* **Editor** : Visual Studo Code (https://code.visualstudio.com)
* **Terminal** : Git Bash (https://git-scm.com/) 

---

## Stack

* HTML (HyperText Markup Language)
* CSS (Cascading Style Sheets)
* Javascript
* **Framework** : Bootstrap, BulmaCSS atau TailwindCSS

---

## HTML (HyperText Markup Language)

Bahasa markup yang digunakan untuk membuat struktur dasar halaman web.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Halaman Saya</title>
</head>
<body>
    <h1>Halo, Dunia!</h1>
    <p>Ini adalah paragraf pertama saya.</p>
</body>
</html>
```

---

## CSS (Cascading Style Sheets)

Digunakan untuk mengatur tampilan dan desain halaman web (warna, font, layout, dll.).

```css
body {
    background-color: lightblue;
    font-family: Arial, sans-serif;
}
h1 {
    color: darkblue;
}
```

---

## Javascript

JavaScript (JS) adalah bahasa pemrograman yang digunakan untuk membuat halaman web lebih interaktif dan dinamis.

---

## Fungsi utama JavaScript:

- **Menambahkan interaktivitas** → Contoh: tombol yang merespons saat diklik.
- **Memanipulasi elemen HTML & CSS** → Contoh: mengubah teks atau warna secara dinamis.
- **Mengontrol perilaku halaman web** → Contoh: validasi formulir sebelum dikirim.
- **Mengambil data dari server (AJAX/Fetch API)** → Contoh: memuat data tanpa harus me-refresh halaman.

---

```js
alert("Halo, selamat datang di website saya!");

document.getElementById("judul").innerHTML = "Teks telah berubah!";

document.getElementById("myButton").addEventListener("click", function() {
    alert("Tombol diklik!");
});

function validasiForm() {
    let nama = document.getElementById("nama").value;
    if (nama == "") {
        alert("Nama tidak boleh kosong!");
        return false;
    }
}
```