# Laporan Praktikum 4 — CSS Lanjutan

**Nama:** Raisyal Fuzi Ghazali
**NIM:** 312510279
**Program Studi:** Teknik Informatika  
**Mata Kuliah:** Pemrograman Web  
**Praktikum:** Modul 4 — CSS Lanjutan

## 1. Membuat Box Element

Pada tahap pertama, saya membuat file `lab4_box.html` yang berisi judul Box Element dan tiga elemen Div. Setiap Div diberi warna latar yang berbeda menggunakan CSS.

**Kode HTML:**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Box Element</title>
  </head>
  <body>
    <header>
      <h1>Box Element</h1>
    </header>
  </body>
</html>
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
</section>
```

**Kode CSS:**

```css
div {
  float: left;
  padding: 10px;
}

.div1 {
  background: red;
}

.div2 {
  background: yellow;
}

.div3 {
  background: green;
}
```

**Screenshot codingan:**
![Codingan Langkah 1](images/codingan%201.png)
**Screenshot codingan:**
![Codingan Langkah 1.2](images/codingan%201.2.png)

**Screenshot hasil browser:**

![Hasil-browser langkah 1](images/hasil-browser%201.png)

## 2. Mengatur Clearfix Element

Pada tahap ini, saya menambahkan Div 4 setelah Div 3. Properti `clear` digunakan agar elemen tersebut tidak mengikuti posisi float sebelumnya.

**Kode HTML:**

```html
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
  <div class="div4">Div 4</div>
</section>
```

**Kode CSS:**

```css
.div4 {
  background-color: blue;
  clear: left;
  float: none;
}
```

Saya juga mencoba nilai `left`, `both`, dan `right` pada properti `clear` untuk melihat perbedaan posisinya.

**Screenshot codingan:**
![Codingan Langkah 2](images/codingan%202.png)
**Screenshot codingan:**
![Codingan Langkah 2.1](images/codingan%202.1.png)
**Screenshot hasil browser:**
**Screenshot codingan:**
![hasil-browser 2](images/hasil-browser%202.png)

## 3. Membuat Layout Sederhana

Saya membuat folder `lab4_layout` yang berisi file `home.html` dan `style.css`. Kedua file tersebut digunakan untuk membuat halaman web sederhana.

**Kode HTML awal:**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div id="container"></div>
    <header>
      <h1>Layout Sederhana</h1>
    </header>
    <nav>
      <a href="home.html" class="active">Home</a>
      <a href="artikel.html">Artikel</a>
      <a href="about.html">About</a>
      <a href="kontak.html">Kontak</a>
    </nav>
    <section id="hero"></section>
    <section id="wrapper">
      <section id="main"></section>
      <aside id="sidebar"></aside>
    </section>
    <footer>
      <p>&copy; 2021 - Universitas Pelita Bangsa</p>
    </footer>
  </body>
</html>
```

**Screenshot codingan:**
![Codingan Langkah 3](images/codingan%203.png)

**Screenshot hasil browser:**
![Hasil-browser Langkah 3](images/hasil-browser%203.png)

## 4. Mengatur CSS dan Header

Pada tahap ini, saya menambahkan CSS dasar untuk mengatur font, margin, padding, lebar container, dan tampilan header.

**Kode CSS:**

```css
* {
  margin: 0;
  padding: 0;
}

body {
  line-height: 1;
  font-size: 100%;
  font-family: "Open Sans", sans-serif;
  color: #5a5a5a;
}

#container {
  width: 980px;
  margin: 0 auto;
  box-shadow: 0 0 1em #cccccc;
}

header {
  padding: 20px;
}

header h1 {
  margin: 20px 10px;
  color: #b5b5b5;
}
```

**Screenshot codingan:**
![Codingan Langkah 4](images/codingan%204.png)

**Screenshot hasil browser:**
![Hasil-browser Langkah 4](images/hasil-browser%204.png)

## 5. Membuat Navigasi

Navigasi dibuat dengan empat menu, yaitu Home, Artikel, About, dan Kontak. Menu Home diberi class `active`.

**Kode HTML:**

```html
<nav>
  <a href="home.html" class="active">Home</a>
  <a href="artikel.html">Artikel</a>
  <a href="about.html">About</a>
  <a href="kontak.html">Kontak</a>
</nav>
```

**Kode CSS:**

```css
nav {
  display: block;
  background-color: #1f5faa;
}

nav a {
  padding: 15px 30px;
  display: inline-block;
  color: #ffffff;
  font-size: 14px;
  text-decoration: none;
  font-weight: bold;
}

nav a.active,
nav a:hover {
  background-color: #2b83ea;
}
```

**Screenshot codingan:**
![Codingan Langkah 5](images/codingan%205.png)

**Screenshot hasil browser:**
![Hasil-codingan Langkah 5](images/hasil-browser%205.png)

## 6. Membuat Hero Panel

Hero panel berisi judul Hello World!, paragraf, dan tautan Learn more.

**Kode HTML:**

```html
<section id="hero">
  <h1>Hello World!</h1>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu.
  </p>
  <a href="home.html" class="btn btn-large"> Learn more &raquo; </a>
</section>
```

**Kode CSS:**

```css
#hero {
  background-color: #e4e4e5;
  padding: 50px 20px;
  margin-bottom: 20px;
}

#hero h1 {
  margin-bottom: 20px;
  font-size: 35px;
}

#hero p {
  margin-bottom: 20px;
  font-size: 18px;
  line-height: 25px;
}
```

**Screenshot codingan:**
![Codingan Langkah 6](images/codingan%206.png)

**Screenshot hasil browser:**
![Hasil-browser Langkah 6](images/hasil-browser%206.png)

## 7. Mengatur Layout Main dan Sidebar

Pada tahap ini, saya mengatur posisi konten utama dan sidebar menggunakan properti `float`.

**Kode CSS:**

```css
#wrapper {
  margin: 0;
}

#main {
  float: left;
  width: 640px;
  padding: 20px;
}

#sidebar {
  float: left;
  width: 260px;
  padding: 20px;
}
```

**Screenshot codingan:**
![Codingan Langkah 7](images/codingan%206.png)

**Screenshot hasil browser:**
![Codingan Langkah 7](images/hasil-browser%207.png)

## 8. Membuat Sidebar Widget

Sidebar berisi widget header dengan lima tautan dan widget teks.

**Kode HTML:**

```html
<aside id="sidebar">
  <div class="widget-box">
    <h3 class="title">Widget Header</h3>
    <ul>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
    </ul>
  </div>

  <div class="widget-box">
    <h3 class="title">Widget Text</h3>
    <p>
      Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.
      Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
      pharetra est nunc, nec pretium nunc pretium ac.
    </p>
  </div>
</aside>
```

**Kode CSS:**

```css
.widget-box {
  border: 1px solid #eee;
  margin-bottom: 20px;
}

.widget-box .title {
  padding: 10px 16px;
  background-color: #428bca;
  color: #fff;
}

.widget-box ul {
  list-style-type: none;
}

.widget-box li {
  border-bottom: 1px solid #eee;
}

.widget-box li a {
  padding: 10px 16px;
  color: #333;
  display: block;
  text-decoration: none;
}

.widget-box li:hover a {
  background-color: #eee;
}

.widget-box p {
  padding: 15px;
  line-height: 25px;
}
```

**Screenshot codingan:**
![Codingan Langkah 8](images/codingan%208.png)

**Screenshot hasil browser:**
![Hasil-browser Langkah 8](images/hasil-browser%208.png)

## 9. Mengatur Footer

Footer digunakan untuk menampilkan informasi hak cipta pada bagian bawah halaman.

**Kode HTML:**

```html
<footer>
  <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
```

**Kode CSS:**

```css
footer {
  clear: both;
  background-color: #1d1d1d;
  padding: 20px;
  color: #eee;
}
```

**Screenshot codingan:**
![Codingan Langkah 9](images/codingan%209.png)

**Screenshot hasil browser:**
![Hasil-browser Langkah 9](images/hasil-browser%209.png)

## 10. Menambahkan Elemen pada Main Content

Saya menambahkan tiga kotak konten yang berisi gambar, judul, paragraf, dan tautan View detail.

**Kode HTML:**

```html
<section id="main">
  <div class="row">
    <div class="box">
      <img
        src="https://dummyimage.com/120/db7d25/fff.png"
        alt=""
        class="image-circle"
      />
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-default">View detail</a>
    </div>
    <div class="box">
      <img
        src="https://dummyimage.com/120/3e73e6/fff.png"
        alt=""
        class="image-circle"
      />
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-default">View detail</a>
    </div>
    <div class="box">
      <img
        src="https://dummyimage.com/120/71e6d4/fff.png"
        alt=""
        class="image-circle"
      />
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-default">View detail</a>
    </div>
  </div>
</section>
```

Kode kotak tersebut diulang hingga terdapat tiga kotak, menggunakan gambar yang berbeda seperti pada modul.

**Kode CSS:**

```css
.box {
  display: block;
  float: left;
  width: 33.333333%;
  box-sizing: border-box;
  padding: 0 10px;
  text-align: center;
}

.box h3 {
  margin: 15px 0;
}

.box p {
  line-height: 20px;
  font-size: 14px;
  margin-bottom: 15px;
}

.image-circle {
  border-radius: 50%;
}

.row {
  margin: 0 -10px;
  box-sizing: border-box;
}

.row:after,
.row:before,
.entry:after,
.entry:before {
  content: "";
  display: table;
}

.row:after,
.entry:after {
  clear: both;
}
```

**Screenshot codingan:**
![Codingan Langkah 10](images/codingan%2010.2.png)

**Screenshot codingan:**
![Codingan Langkah 10.2](images/codingan%2010.png)

**Screenshot hasil browser:**
![Codingan Langkah 10](images/hasil-browser%2010.png)

## 11. Menambahkan Content Artikel

Saya menambahkan dua artikel pada bagian main content. Setiap artikel memiliki judul, gambar, dan paragraf.

**Kode HTML:**

```html
<hr class="divider" />

<article class="entry">
  <h2>First featurette heading.</h2>
  <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" />
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo
    fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc,
    nec pretium nunc pretium ac.
  </p>
</article>

<hr class="divider" />

<article class="entry">
  <h2>First featurette heading.</h2>
  <img
    src="https://dummyimage.com/150/7b8a70/fff.png"
    alt=""
    class="right-img"
  />
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo
    fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc,
    nec pretium nunc pretium ac.
  </p>
</article>
```

**Kode CSS:**

```css
.divider {
  border: 0;
  border-top: 1px solid #eeeeee;
  margin: 40px 0;
}

.entry {
  margin: 15px 0;
}

.entry h2 {
  margin-bottom: 20px;
}

.entry p {
  line-height: 25px;
}

.entry img {
  float: left;
  border-radius: 5px;
  margin-right: 15px;
}

.entry .right-img {
  float: right;
}
```

**Screenshot codingan:**
![Codingan Langkah 11](images/codingan%2011.png)

**Screenshot codingan:**
![Codingan Langkah 11.2](images/codingan%2011.2.png)

**Screenshot hasil browser:**
![Hasil-browser 11](images/hasil-browser%2011.png)

## 12. Membuat Halaman About

Pada tugas tambahan, saya membuat halaman About yang berisi deskripsi dan portofolio.

**File:** `about.html`

Kode lengkap halaman About disertakan pada file terpisah di folder `lab4_layout`.

**Screenshot codingan:**
![Codingan Langkah 12](images/codingan%2012.png)

**Screenshot hasil browser:**
![Hasil-browser 12](images/hasil-browser%2012.png)

## 13. Membuat Halaman Kontak

Saya membuat halaman Kontak yang berisi formulir nama, email, pesan, dan tombol kirim.

**File:** `kontak.html`

Kode lengkap halaman Kontak disertakan pada file terpisah di folder `lab4_layout`.

**Screenshot codingan:**
![Codingan Langkah 13](images/codingan%2013.png)

**Screenshot hasil browser:**
![Hasil-browser 13](images/hasil-browser%2013.png)

## Kesimpulan

Dari praktikum ini, saya mempelajari cara membuat elemen Div, menggunakan properti float dan clear, serta mengatur layout halaman web menggunakan HTML dan CSS. Saya juga mempelajari pembuatan navigasi, hero panel, sidebar, widget, footer, main content, artikel, dan halaman About serta Kontak.
