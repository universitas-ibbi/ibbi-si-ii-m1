---
title: HTML
version: 1.0.0
theme: default
header: HTML
footer: https://github.com/universitas-ibbi/ibbi-si-ii-m1
paginate: true
marp: true
---

<!-- 
_class: lead 
_paginate: skip
-->

# HTML

---

## **HTML?**

HTML (HyperText Markup Language) adalah bahasa markup yang digunakan untuk membuat halaman web. HTML menyediakan struktur dasar sebuah halaman web dengan menggunakan elemen-elemen yang disebut **tag**.

---

**Contoh sederhana HTML:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Contoh Halaman</title>
</head>
<body>
    <h1>Selamat Datang di HTML</h1>
    <p>Ini adalah contoh halaman HTML sederhana.</p>
</body>
</html>
```

---

## **Anatomy of an HTML Element**

Setiap elemen HTML memiliki **anatomi** dasar, yaitu:
- **Opening tag**: `<p>`
- **Content**: "Ini adalah paragraf"
- **Closing tag**: `</p>`

**Contoh:**
```html
<p>Ini adalah paragraf.</p>
```

---

Beberapa elemen juga memiliki **atribut**, misalnya:
```html
<a href="https://example.com">Klik di sini</a>
```
Di sini, `href` adalah atribut yang menentukan tujuan tautan.

---

## **HTML Document Structure**

Struktur dasar dokumen HTML terdiri dari:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Judul Halaman</title>
</head>
<body>
    <h1>Judul Utama</h1>
    <p>Konten halaman.</p>
</body>
</html>
```

---

Bagian penting:
- `<!DOCTYPE html>`: Menentukan tipe dokumen HTML5.
- `<html>`: Elemen utama yang membungkus seluruh halaman.
- `<head>`: Berisi metadata seperti judul dan karakter encoding.
- `<body>`: Berisi konten utama halaman.

---

## **Text Elements**

HTML menyediakan berbagai elemen untuk menampilkan teks, seperti:
- **Heading (Judul)**: `<h1>` hingga `<h6>`
- **Paragraf**: `<p>`
- **Tebal** (`<strong>`) dan Miring (`<em>`)

**Contoh:**
```html
<h1>Judul Besar</h1>
<p>Ini adalah teks <strong>tebal</strong> dan <em>miring</em>.</p>
```

---

## **Lists (Daftar)**
HTML memiliki dua jenis daftar utama:
1. **Ordered List (Daftar Berurutan)** - `<ol>`:
```html
<ol>
    <li>Pertama</li>
    <li>Kedua</li>
    <li>Ketiga</li>
</ol>
```

---

2. **Unordered List (Daftar Tidak Berurutan)** - `<ul>`:
```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

---

## **Image and Attributes**

Untuk menampilkan gambar di HTML, gunakan tag `<img>` dengan atribut:
- `src`: Sumber gambar.
- `alt`: Deskripsi alternatif gambar.

**Contoh:**
```html
<img src="gambar.jpg" alt="Deskripsi gambar">
```

---

## **Hyperlinks**
Hyperlink digunakan untuk menghubungkan halaman menggunakan tag `<a>`.

**Contoh tautan ke situs eksternal:**
```html
<a href="https://www.example.com">Kunjungi Situs</a>
```

**Contoh tautan ke halaman lain dalam situs:**
```html
<a href="about.html">Tentang Kami</a>
```

---

## **Structuring Our Page**
Untuk membuat halaman lebih terstruktur, gunakan elemen seperti:
- `<header>`: Bagian atas halaman (logo, menu).
- `<nav>`: Navigasi.
- `<section>`: Bagian konten utama.
- `<article>`: Artikel independen.
- `<aside>`: Konten sampingan.
- `<footer>`: Bagian bawah halaman.

---

**Contoh:**
```html
<header>
    <h1>Nama Situs</h1>
</header>
<nav>
    <a href="index.html">Beranda</a>
    <a href="about.html">Tentang</a>
</nav>
<section>
    <h2>Artikel Utama</h2>
    <p>Ini adalah konten utama halaman.</p>
</section>
<footer>
    <p>&copy; 2025 Nama Anda</p>
</footer>
```

---

## **Note on Semantic HTML**

**Semantic HTML** adalah penggunaan elemen HTML sesuai dengan arti atau fungsinya.

**Contoh elemen non-semantik vs semantik:**
- **Non-semantik**: `<div>` dan `<span>` (tidak menunjukkan arti spesifik).
- **Semantik**: `<article>`, `<section>`, `<header>`, `<footer>`, dll.

Menggunakan **Semantic HTML** membantu SEO dan aksesibilitas.

---

**Contoh penggunaan yang benar:**
```html
<article>
    <h2>Judul Artikel</h2>
    <p>Konten artikel.</p>
</article>
```

---

## **Kesimpulan**
- HTML adalah bahasa markup untuk membangun struktur halaman web.
- Elemen HTML terdiri dari tag pembuka, isi, dan tag penutup.
- Struktur dokumen HTML harus sesuai dengan standar.
- Gunakan **Semantic HTML** untuk meningkatkan aksesibilitas dan SEO.

---

## **References**

- [https://www.w3schools.com/html/default.asp](https://www.w3schools.com/html/default.asp)
- [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)