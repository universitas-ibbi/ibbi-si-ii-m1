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

## Repository

[https://github.com/universitas-ibbi/ibbi-si-ii-m1](https://github.com/universitas-ibbi/ibbi-si-ii-m1)

- Bahan Belajar
- Contoh Lab
- Info

![bg right](./images/repository.png)
  
---

## Web Development  

Dalam web development, ada tiga jenis developer utama: **Frontend Developer, Backend Developer, dan Fullstack Developer**. Berikut penjelasannya:  

---

## **1️⃣ Frontend Developer**  
👉 **Tugas**: Membangun tampilan dan interaksi yang bisa dilihat serta digunakan oleh pengguna di browser.  
👉 **Fokus**: UI (User Interface) & UX (User Experience).  
👉 **Teknologi yang digunakan**:  
   - **HTML** → Membuat struktur halaman web.  
   - **CSS** → Memberikan desain dan tata letak halaman web.  
   - **JavaScript** → Menambahkan interaktivitas pada halaman.  
   - **Framework**: React.js, Vue.js, Angular.  

---

👉 **Contoh Pekerjaan**:  
   ✅ Desain tombol dan navigasi website.  
   ✅ Membuat website responsif.  
   ✅ Menampilkan data dari backend di browser.  

---

## **2️⃣ Backend Developer**  
👉 **Tugas**: Mengelola logika bisnis, database, server, dan API.  
👉 **Fokus**: Menyimpan, memproses, dan mengelola data dari frontend.  
👉 **Teknologi yang digunakan**:  
   - **Bahasa pemrograman**: PHP, Python, Node.js, Ruby, Java.  
   - **Database**: MySQL, PostgreSQL, MongoDB.  
   - **Framework**: Laravel (PHP), Express.js (Node.js), Django (Python).  
  
---

👉 **Contoh Pekerjaan**:  
   ✅ Membuat sistem login dan autentikasi.  
   ✅ Menyimpan data pengguna di database.  
   ✅ Mengelola transaksi di website e-commerce.  

---

## **3️⃣ Fullstack Developer**  
👉 **Tugas**: Mengembangkan frontend dan backend sekaligus.  
👉 **Fokus**: Bisa menangani tampilan UI dan pengolahan data di server.  
👉 **Teknologi yang digunakan**:  
   - **Frontend**: HTML, CSS, JavaScript, React.js, Vue.js.  
   - **Backend**: Node.js, PHP, Python, Laravel, Django.  
   - **Database**: MySQL, MongoDB, Firebase.  

---

👉 **Contoh Pekerjaan**:  
   ✅ Membangun website lengkap dari frontend hingga backend.  
   ✅ Mengembangkan sistem login dan dashboard pengguna.  
   ✅ Mengelola API dan tampilan website sekaligus.  

---

### **Kesimpulan**  
🔹 **Frontend Developer** → Fokus pada tampilan website.  
🔹 **Backend Developer** → Fokus pada server, database, dan logika bisnis.  
🔹 **Fullstack Developer** → Menguasai frontend & backend sekaligus.  

---

## Cara Kerja Web

* **User Request** → Browser mengakses www.example.com.
* **DNS Resolving** → Mencari alamat IP domain.
* **HTTP Request** → Permintaan dikirim ke server.
* **Server Memproses** → Mengambil file HTML/CSS/JS atau query ke database.
* **HTTP Response** → Server mengirimkan halaman web.
* **Browser Render** → Menampilkan halaman ke pengguna.

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