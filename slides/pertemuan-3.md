---
title: CSS
version: 1.0.0
theme: default
header: CSS
footer: https://github.com/universitas-ibbi/ibbi-si-ii-m1
paginate: true
marp: true
---

<!-- 
_class: lead 
_paginate: skip
-->

# CSS (Cascading Style Sheets)

---

## **Pengenalan CSS**  
- CSS (Cascading Style Sheets) adalah bahasa untuk mengatur tampilan halaman web.  
- Memisahkan konten (HTML) dari desain.  
- Memungkinkan perubahan desain tanpa mengubah struktur HTML.  
- Contoh penggunaan CSS:  
  ```css
  p {
    color: blue;
    font-size: 16px;
  }
  ```

---

## **Cara Menyisipkan CSS**  

---

### **1. Inline CSS**  
- Langsung dalam tag HTML menggunakan atribut `style`.  
- Contoh:  
  ```html
  <p style="color: red;">Teks berwarna merah</p>
  ```

---

### **2. Internal CSS**  
- Ditulis di dalam `<style>` dalam `<head>`.  
- Contoh:  
  ```html
  <style>
    p { color: blue; }
  </style>
  ```

---

### **3. External CSS**  
- Ditulis dalam file terpisah (`style.css`).  
- Dipanggil dalam HTML dengan `<link>`.  
- Contoh:  
  ```html
  <link rel="stylesheet" href="style.css">
  ```

---

## **Styling Text**  
- Properti penting:  
  - `color`: Warna teks  
  - `font-family`: Jenis font  
  - `font-size`: Ukuran font  
  - `font-weight`: Ketebalan teks  
  - `text-align`: Posisi teks  

---

- Contoh:  
  ```css
  h1 {
    color: green;
    font-size: 24px;
    text-align: center;
  }
  ```

---

## **Combining Selectors**  
- Menggabungkan beberapa selector untuk efisiensi.  
- Contoh:  
  ```css
  h1, h2, p {
    color: blue;
  }
  ```

---

## **Class dan ID Selectors**  
- **Class Selector (`.`)**: Bisa digunakan pada banyak elemen.  
- **ID Selector (`#`)**: Unik, hanya untuk satu elemen.  
- Contoh:  
  ```css
  .judul {
    font-size: 20px;
    color: red;
  }
  
  #utama {
    background-color: yellow;
  }
  ```

---

## **Working with Colors**  
- **Warna dalam CSS bisa ditulis sebagai:**  
  - Nama warna: `red, blue`  
  - Hexadecimal: `#ff0000`  
  - RGB: `rgb(255, 0, 0)`  
  - HSL: `hsl(0, 100%, 50%)`  

---

- Contoh penggunaan:  
  ```css
  body {
    background-color: #f0f0f0;
    color: #333;
  }
  ```

---

## **Pseudo Classes**  
- Digunakan untuk memilih elemen berdasarkan statusnya.  
- Contoh:  
  ```css
  a:hover {
    color: red;
  }
  input:focus {
    background-color: yellow;
  }
  ```

---

## **Styling Hyperlinks**  
- Warna link berubah saat hover, aktif, dan dikunjungi.  
- Contoh:  
  ```css
  a:link {
    color: blue;
  }
  a:visited {
    color: purple;
  }
  a:hover {
    color: red;
  }
  ```

---

## **Using Chrome DevTools**  
- Alat debugging bawaan Chrome.  
- Bisa digunakan untuk melihat dan mengedit CSS langsung di browser.  

---

## **Urutan Selector**  
- **Spesifisitas menentukan selector mana yang menang.**  
- Urutan dari rendah ke tinggi:  
  - Elemen (`p`)  
  - Class (`.judul`)  
  - ID (`#utama`)  
  - Inline (`style="..."`)  
  - `!important`  

---

- Contoh konflik:  
  ```css
  p { color: blue; } 
  .paragraf { color: red; } 
  #teks { color: green; }
  ```

---

## **Inheritance dan Universal Selector (`*`)**  
- **Inheritance**: Properti teks diwariskan oleh elemen anak.  
- **Universal Selector (`*`)**: Menerapkan gaya ke semua elemen.  
- Contoh:  
  ```css
  * {
    font-family: Arial, sans-serif;
  }
  ```

---

## **CSS Box Model**  
- **Elemen dalam CSS terdiri dari:**  
  - **Content**: Isi elemen  
  - **Padding**: Ruang dalam sebelum border  
  - **Border**: Batas elemen  
  - **Margin**: Jarak dengan elemen lain  

---

- Contoh visualisasi:  
  ```css
  div {
    width: 200px;
    padding: 10px;
    border: 5px solid black;
    margin: 20px;
  }
  ```

---

## **Margin dan Padding**  
- **Margin**: Jarak luar elemen.  
- **Padding**: Jarak antara isi dan batas elemen.  
- Contoh:  
  ```css
  div {
    margin: 20px;
    padding: 10px;
  }
  ```

---

## **Menambahkan Dimensi**  
- Properti `width` dan `height` menentukan ukuran elemen.  
- Contoh:  
  ```css
  div {
    width: 300px;
    height: 200px;
  }
  ```

---

## **Types of Boxes**  
- **Block Elements**: `div, p, h1, ul, li`  
- **Inline Elements**: `span, a, img`  
- **Inline-block**: Kombinasi inline & block  

---

## **Pseudo Elements**  
- Menambahkan elemen tambahan tanpa mengubah HTML.  
- Contoh:  
  ```css
  p::first-letter {
    font-size: 2em;
    color: red;
  }
  ```

---

## Referensi

- [https://www.w3schools.com/css/](https://www.w3schools.com/css/)