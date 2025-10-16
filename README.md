
# Lab4Web
#### Nama   = Dzaki Arif Rahman
#### Kelas  = TI.24.A4 
#### NIM    = 312410312 
#### Matkul = Pemrograman Web 1  

# Praktikum 4 – CSS Layout

---

## Pertanyaan Praktikum

<img width="900" height="400" alt="Screenshot Pertanyaan Praktikum 4" src="https://github.com/user-attachments/assets/xxxxxxxxx" />

---

## Jawaban dan Penjelasan  

Pada praktikum kali ini, kita akan belajar tentang **CSS Layout**, yaitu cara mengatur tata letak elemen-elemen pada halaman web.  
Beberapa hal yang dipelajari di praktikum ini antara lain:
1. **Box Element** – memahami struktur dasar elemen dalam bentuk kotak (box model).  
2. **Float Property** – membuat elemen “mengambang” di sisi kiri/kanan.  
3. **Clearfix** – mengatur elemen agar tidak bertabrakan dengan elemen yang difloat.  
4. **HTML5 Semantic Elements** – mengenal tag semantik seperti `<header>`, `<nav>`, `<section>`, `<aside>`, `<footer>`.  
5. **Layout Web Sederhana** – menggabungkan semua konsep di atas menjadi satu halaman web.  

---

## LATIHAN 1 – Membuat Box Element  

### Step 1: Membuat Struktur HTML Dasar  

Kita buat file baru bernama `lab4_box.html` seperti ini:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Element</title>
</head>
<body>
  <header>
    <h1>Box Element</h1>
  </header>
</body>
</html>
````

---

### Step 2: Menambahkan Elemen Box

Tambahkan tiga elemen `<div>` ke dalam tag `<section>` untuk membuat 3 box.

```html
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
</section>
```

---

### Step 3: Menambahkan CSS Float

Tambahkan kode CSS di bagian `<head>` untuk memberi warna dan mengatur posisi.

```html
<style>
  div {
    float: left;
    padding: 10px;
  }
  .div1 { background: red; }
  .div2 { background: yellow; }
  .div3 { background: green; }
</style>
```

### Screenshot hasil dan codingannya

<img width="1640" height="1030" alt="image" src="https://github.com/user-attachments/assets/d1f0019c-651e-4e9b-b868-404a4f5168e0" />


### Penjelasan

* Setiap elemen `<div>` akan ditampilkan berdampingan secara horizontal karena menggunakan `float: left`.
* Warna dan padding membuat setiap box terlihat jelas dan terpisah.

---

## LATIHAN 2 – Mengatur Clearfix Element

### Step 1: Tambahkan Elemen Baru

Tambahkan satu elemen lagi di bawah tiga box tadi.

```html
<div class="div4">Div 4</div>
```

### Step 2: Tambahkan CSS Clearfix

Tambahkan properti `clear` untuk mengatur posisi elemen berikutnya agar tidak sejajar dengan elemen yang difloat.

```css
.div4 {
  background-color: blue;
  clear: left;
  float: none;
}
```

### Screenshot hasil dan codingannya

<img width="1614" height="918" alt="image" src="https://github.com/user-attachments/assets/bd457df0-bbdd-474e-bdc8-ac6d6773ad54" />


### Penjelasan

* Properti `clear: left;` membuat “Div 4” turun ke bawah.
* Tanpa `clear`, elemen keempat akan tetap sejajar dengan elemen sebelumnya.

---

## LATIHAN 3 – Membuat Layout Web Sederhana

### Step 1: Buat Struktur HTML

Buat file baru `home.html` di folder `lab4_layout`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Layout Sederhana</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="container">
    <header>
      <h1>Dzaki Arif Rahman</h1>
    </header>

    <nav>
      <a href="home.html" class="active">Home</a>
      <a href="artikel.html">Artikel</a>
      <a href="about.html">About</a>
      <a href="kontak.html">Kontak</a>
    </nav>

    <section id="hero">
      <h1>Hello World!</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
      <a href="#" class="btn btn-large">Learn more &raquo;</a>
    </section>

    <section id="wrapper">
      <section id="main">
        <h2>Welcome to My Website ZAKI</h2>
        <p>Contoh konten utama ditampilkan di sini...</p>
      </section>

      <aside id="sidebar">
        <div class="widget-box">
          <h3 class="title">Widget Header</h3>
          <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
          </ul>
        </div>
      </aside>
    </section>

    <footer>
      <p>&copy; 2025 - Universitas Pelita Bangsa</p>
    </footer>
  </div>
</body>
</html>

```

---

### Step 2: Tambahkan CSS Layout

Buat file `style.css` di folder yang sama.

```css
* { margin: 0; padding: 0; }
body {
  font-family: 'Open Sans', sans-serif;
  color: #5a5a5a;
}

#container {
  width: 980px;
  margin: 0 auto;
  box-shadow: 0 0 1em #ccc;
}

/* Header */
header { padding: 20px; }
header h1 { color: #b5b5b5; }

/* Navigasi */
nav { background: #1f5faa; }
nav a {
  color: white;
  padding: 15px 30px;
  display: inline-block;
  text-decoration: none;
  font-weight: bold;
}
nav a.active, nav a:hover {
  background: #2b83ea;
}

/* Hero Section */
#hero {
  background: #e4e4e5;
  padding: 50px 20px;
  margin-bottom: 20px;
}

/* Layout dua kolom */
#wrapper { margin: 0; }
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

/* Widget Sidebar */
.widget-box {
  border: 1px solid #eee;
  margin-bottom: 20px;
}
.widget-box .title {
  background: #428bca;
  color: #fff;
  padding: 10px 16px;
}
.widget-box ul { list-style: none; }
.widget-box li a {
  display: block;
  padding: 10px 16px;
  color: #333;
  text-decoration: none;
}
.widget-box li:hover a {
  background: #eee;
}

/* Footer */
footer {
  clear: both;
  background: #1d1d1d;
  color: #eee;
  padding: 20px;
  text-align: center;
}
```

### Screenshot hasil dan codingannya

<img width="1725" height="928" alt="image" src="https://github.com/user-attachments/assets/d8a20aef-756a-46bc-8878-8d20e026b7e8" />


### Penjelasan

* Layout terdiri dari **header, navigasi, hero panel, main content, sidebar, dan footer**.
* Elemen-elemen disusun menggunakan konsep **float layout**.
* Sidebar berada di kanan dan konten utama di kiri.

---

## TUGAS PRAKTIKUM

### 1. Layout **About**

Halaman ini berisi deskripsi diri dan daftar portfolio.

```html
<section id="main">
  <h2>Tentang Saya</h2>
  <p>Saya adalah mahasiswa Universitas Pelita Bangsa yang sedang mempelajari Pemrograman Web.</p>

  <h3>Portfolio</h3>
  <ul>
    <li>Project 1 – Desain Web Pribadi</li>
    <li>Project 2 – Sistem Inventori Barang</li>
    <li>Project 3 – Landing Page UMKM</li>
  </ul>
</section>
```

---

### 2. Layout **Contact**

Halaman ini berisi form sederhana.

```html
<section id="main">
  <h2>Kontak Kami</h2>
  <form action="proses.php" method="post">
    <p>
      <label for="nama">Nama</label><br>
      <input type="text" id="nama" name="nama" required>
    </p>
    <p>
      <label for="email">Email</label><br>
      <input type="email" id="email" name="email" required>
    </p>
    <p>
      <label for="pesan">Pesan</label><br>
      <textarea id="pesan" name="pesan" rows="4"></textarea>
    </p>
    <p>
      <button type="submit">Kirim</button>
    </p>
  </form>
</section>
```

### Screenshot hasil dan codingannya

<img width="900" height="450" alt="contact page" src="https://github.com/user-attachments/assets/xxxxxxxxx" />

### Penjelasan

* Form berfungsi untuk menerima data pengguna.
* Input teks untuk nama, email, dan pesan.
* Data akan dikirim ke `proses.php` dengan metode `POST`.

---

## 💡 Kesimpulan

Dari praktikum ini, kita telah mempelajari cara membuat **layout web sederhana** menggunakan kombinasi HTML dan CSS.
Konsep **box model**, **float**, **clear**, dan **HTML5 semantic elements** sangat penting dalam mengatur struktur tampilan web agar lebih rapi dan mudah dipahami.

Selain itu, penggunaan **float layout** membantu membuat tampilan dua kolom (main dan sidebar) dengan struktur yang profesional.
Pengetahuan ini menjadi dasar sebelum mempelajari layout modern seperti **Flexbox** dan **CSS Grid**.

---


Kalau kamu mau, aku bisa tambahkan **gambar-gambar hasil coding** langsung dari file PDF atau buat placeholder screenshot biar README-mu kelihatan profesional di GitHub. Mau sekalian aku tambahkan bagian itu juga?
```
