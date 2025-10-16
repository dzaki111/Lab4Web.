
# Lab4Web
#### Nama   = Dzaki Arif Rahman
#### Kelas  = TI.24.A4 
#### NIM    = 312410312 
#### Matkul = Pemrograman Web 1  

# Praktikum 4 – CSS Layout

---

## Pertanyaan Praktikum

<img width="771" height="331" alt="image" src="https://github.com/user-attachments/assets/c6b539e3-e89d-4359-ae7a-7374491073b0" />


---

## Jawaban dan Penjelasan  


Pada praktikum kali ini, **saya mempelajari tentang CSS Layout**, yaitu cara mengatur tata letak elemen-elemen pada halaman web agar tampil lebih rapi, seimbang, dan menarik.
Tujuan dari praktikum ini adalah agar saya memahami bagaimana struktur halaman web dibentuk — mulai dari bagian header, navigasi, konten utama, sidebar, hingga footer — serta bagaimana semua bagian tersebut diatur menggunakan CSS.

Beberapa hal penting yang saya pelajari dalam praktikum ini antara lain:

1. **Box Element**
   Pada bagian ini saya belajar bahwa semua elemen HTML sebenarnya memiliki bentuk kotak (box). Dengan memahami konsep *box model*, saya dapat mengatur ukuran, jarak (margin dan padding), serta warna dari setiap elemen agar tampilannya sesuai kebutuhan.

2. **Float Property**
   Di sini saya mempelajari bagaimana cara membuat elemen “mengambang” ke sisi kiri atau kanan halaman menggunakan properti `float`. Teknik ini biasanya digunakan untuk membuat layout kolom, seperti menempatkan konten utama dan sidebar berdampingan.

3. **Clearfix**
   Saya juga mempelajari cara menggunakan `clear` untuk mengatasi masalah tata letak yang terjadi akibat penggunaan `float`. Dengan properti ini, elemen berikutnya tidak akan bertabrakan dengan elemen yang difloat sebelumnya.

4. **HTML5 Semantic Elements**
   Selain itu, saya dikenalkan dengan berbagai elemen semantik dalam HTML5 seperti `<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, dan `<footer>`. Elemen-elemen ini memberikan makna yang lebih jelas terhadap struktur halaman web sehingga lebih mudah dipahami oleh pengguna maupun mesin pencari seperti Google.

5. **Layout Web Sederhana**
   Pada bagian terakhir, saya menggabungkan semua konsep yang telah dipelajari untuk membuat sebuah layout web sederhana. Layout ini terdiri dari beberapa bagian utama seperti header, navigasi, hero section, konten utama, sidebar, dan footer.
   Dari latihan ini, saya belajar bagaimana membangun tampilan web yang tertata rapi dan terlihat profesional meskipun menggunakan teknik dasar CSS.



---

## LATIHAN 1 – Membuat Box Element  

### Step 1: Membuat Struktur HTML Dasar  

Kita buat file baru bernama `web.html` seperti ini:

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


---

### Penjelasan

Pada contoh di atas, saya membuat tiga elemen `<div>` di dalam tag `<section>` dan menggunakan CSS untuk mengatur tampilannya. Berikut penjelasan detailnya:

1. **Float: left**
   Saya menggunakan properti `float: left` pada elemen `<div>` agar setiap box “mengapung” ke kiri dari container induknya. Secara default, `<div>` adalah elemen blok yang menempati seluruh lebar baris dan tampil secara vertikal, satu di atas yang lain. Dengan `float: left`, perilaku ini berubah: setiap `<div>` akan mencoba menempati ruang horizontal yang tersedia di sisi kiri container, sehingga beberapa `<div>` dapat tampil sejajar dalam satu baris jika ruang cukup.

2. **Padding**
   Saya menambahkan padding di dalam box agar ada jarak antara tepi `<div>` dan isi teksnya. Hal ini membuat konten tidak menempel langsung pada batas box, sehingga tampilan menjadi lebih rapi dan lebih nyaman dibaca.

3. **Warna (Background)**
   Saya memberi warna latar pada setiap `<div>` dengan beberapa tujuan:

   * Membantu saya membedakan satu box dengan box lainnya.
   * Membuat tampilan lebih menarik dan jelas bagi pengguna.
   * Memudahkan saya melihat efek `float` secara langsung karena setiap box terlihat terpisah.

4. **Kelebihan dan Kekurangan Float**

   * **Kelebihan**: Float mudah digunakan untuk membuat elemen tampil berdampingan.
   * **Kekurangan**: Elemen setelah `<div>` yang difloat dapat “menempel” pada floating box jika saya tidak menggunakan `clear`, sehingga layout bisa menjadi berantakan. Untuk layout yang lebih kompleks, saya biasanya menggunakan metode modern seperti `display: flex` atau `display: grid`, yang lebih fleksibel dan mudah dikelola.

---

### Kesimpulan

Dengan menggunakan `float: left`, saya dapat menampilkan beberapa `<div>` secara horizontal di dalam container. Warna dan padding membantu saya membedakan setiap box dan membuat tampilannya lebih rapi. Meskipun float efektif untuk membuat layout sederhana, untuk layout yang lebih kompleks saya lebih menyarankan menggunakan Flexbox atau Grid agar lebih stabil, fleksibel, dan mudah diatur.

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


---

### Penjelasan

Pada latihan ini, saya menambahkan elemen `<div class="div4">` setelah tiga `<div>` sebelumnya yang menggunakan `float: left`.

1. **Masalah float**
   Saat saya menggunakan `float`, elemen yang difloat “mengapung” ke kiri, dan elemen lain bisa menempel atau sejajar di sampingnya. Hal ini sering menimbulkan masalah ketika saya ingin menempatkan elemen baru **di bawah** elemen yang difloat. Tanpa penanganan khusus, elemen baru bisa muncul **sejajar dengan box sebelumnya**, bukan di bawahnya.

2. **Properti clear**
   Saya menggunakan properti `clear` untuk mengatasi masalah ini. Dalam contoh ini:

   ```css
   clear: left;
   ```

   Artinya, elemen `.div4` akan **menghentikan floating dari elemen sebelah kiri** dan otomatis turun ke posisi di bawah semua elemen yang difloat ke kiri.

3. **Float none**
   Saya juga menambahkan `float: none;` pada `.div4` untuk memastikan elemen ini tidak ikut mengapung ke kiri atau kanan, sehingga sepenuhnya menempati posisi normal dalam aliran dokumen.

4. **Warna (Background)**
   Saya memberi warna biru pada `.div4` untuk membedakannya dari tiga box sebelumnya (merah, kuning, hijau). Dengan begitu, efek `clear` terlihat jelas: box biru muncul di baris baru dan tidak sejajar dengan box yang difloat.

5. **Visualisasi efek**
   Dengan kombinasi `clear: left` dan `float: none`, saya melihat `.div4` muncul **di bawah** ketiga box yang difloat, menjaga tata letak tetap rapi dan mudah dibaca.

---

### Kesimpulan

Properti `clear` sangat berguna ketika saya menggunakan elemen yang difloat dan ingin menempatkan elemen baru **di baris terpisah**. Dalam latihan ini, `clear: left` membuat “Div 4” turun di bawah ketiga box sebelumnya. Penggunaan `float: none` memastikan elemen tidak ikut mengapung, sehingga layout tetap bersih dan terstruktur. Teknik ini penting bagi saya untuk menghindari masalah layout saat membuat halaman dengan elemen yang berdampingan menggunakan float.

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
### Screenshot hasil dan codingannya

<img width="1486" height="899" alt="image" src="https://github.com/user-attachments/assets/98de6338-6e1a-42e9-8f73-8cddac31b1f3" />


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

<img width="1726" height="936" alt="image" src="https://github.com/user-attachments/assets/30c2d0c3-b414-4e99-a31f-467bf162a51a" />


---

### Penjelasan

Pada latihan ini, saya membuat layout web sederhana menggunakan HTML dan CSS. Struktur halaman terdiri dari beberapa bagian utama: header, navigasi, hero section, main content, sidebar, dan footer. Mari saya jelaskan satu per satu:

1. **Container**
   Saya menggunakan elemen `#container` untuk membungkus seluruh konten halaman. Dengan `width: 980px` dan `margin: 0 auto`, container ini berada di tengah halaman secara horizontal. `box-shadow` saya tambahkan untuk memberikan efek bayangan lembut di sekeliling container agar tampilan lebih estetik.

2. **Header**
   Bagian header berisi judul halaman (`h1`). Saya menambahkan padding agar teks tidak menempel pada tepi container. Warna font saya atur agar lebih lembut dan kontras dengan background.

3. **Navigasi (Nav Bar)**
   Navigasi saya buat menggunakan elemen `<nav>` dengan link (`<a>`) yang disusun horizontal menggunakan `display: inline-block`. Background biru gelap membuat menu terlihat jelas, sementara efek hover dan class `.active` memberi saya umpan balik visual ketika link aktif atau disentuh.

4. **Hero Section**
   Hero section adalah area menonjol di bagian atas halaman yang berisi pesan utama atau ajakan tindakan (call-to-action). Padding besar saya gunakan agar konten terlihat lega, dan background abu-abu muda membedakan hero section dari bagian lain.

5. **Layout Dua Kolom**
   Bagian utama (`#main`) dan sidebar (`#sidebar`) saya susun menggunakan **float layout**:

   * `#main` saya float ke kiri dengan lebar 640px.
   * `#sidebar` juga saya float ke kiri dengan lebar 260px.
     Saya menambahkan padding agar isi konten tidak menempel pada tepi box.
     Dengan float ini, kedua kolom tampil berdampingan secara horizontal.

6. **Widget Sidebar**
   Sidebar saya isi dengan widget yang memiliki border dan margin antar widget. Judul widget saya beri warna biru dengan font putih agar menonjol. Link di dalam widget saya beri efek hover agar lebih interaktif.

7. **Footer**
   Footer saya beri `clear: both` untuk memastikan tampilannya berada **di bawah** semua elemen yang difloat. Warna gelap dan teks putih membuat footer mudah dibaca dan membedakan dari konten utama.

---

### Kesimpulan

Layout web sederhana ini saya buat memanfaatkan konsep **float layout** untuk menyusun konten utama dan sidebar secara berdampingan. Penggunaan container, padding, margin, dan warna membuat halaman terlihat rapi dan estetis. Hero section menonjolkan informasi penting, navigasi memudahkan akses antar halaman, dan footer saya letakkan di posisi yang tepat menggunakan `clear: both`.

Dengan pemahaman ini, saya dapat membuat layout web multi-kolom yang responsif dan mudah dibaca, meskipun float kini banyak digantikan oleh metode modern seperti **Flexbox** atau **CSS Grid** untuk pengaturan layout yang lebih fleksibel dan efisien.

---

## TUGAS PRAKTIKUM

### 1. Layout **About**

Halaman ini berisi deskripsi diri dan daftar portfolio.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>About - Dzaki Arif Rahman</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="container">
    <header>
      <h1>Dzaki Arif Rahman</h1>
    </header>

    <nav>
      <a href="home.html">Home</a>
      <a href="artikel.html">Artikel</a>
      <a href="about.html" class="active">About</a>
      <a href="kontak.html">Kontak</a>
    </nav>

    <section id="wrapper">
      <section id="main">
        <h2>Tentang Saya</h2>
        <p>Halo! Saya <b>Dzaki Arif Rahman</b>, mahasiswa Universitas Pelita Bangsa, jurusan Teknik Informatika.  
        Saat ini saya sedang mempelajari dasar-dasar <b>Pemrograman Web</b> termasuk HTML, CSS, dan JavaScript.  
        Tujuan saya adalah menjadi seorang Web Developer profesional yang bisa membangun website interaktif dan fungsional.</p>

        <h3>Portfolio</h3>
        <ul>
          <li> Project 1 – Desain Web Pribadi</li>
          <li> Project 2 – Sistem Inventori Barang</li>
          <li> Project 3 – Landing Page UMKM</li>
        </ul>

        <h3>Keahlian</h3>
        <p>Saya memiliki minat dalam bidang:</p>
        <ul>
          <li>lagi belajar (HTML, CSS)</li>
          <li>Desain UI/UX</li>
          <li>Pengembangan Aplikasi Web Dasar</li>
        </ul>
      </section>

      <aside id="sidebar">
        <div class="widget-box">
          <h3 class="title">Tentang Saya</h3>
          <p>Saya mahasiswa yang bersemangat dalam dunia teknologi dan ingin terus berkembang dalam bidang web development.</p>
        </div>

        <div class="widget-box">
          <h3 class="title">Media Sosial</h3>
          <ul>
            <li><a href="#">Instagram</a></li>
            <li><a href="#">LinkedIn</a></li>
            <li><a href="#">GitHub</a></li>
          </ul>
        </div>
      </aside>
    </section>

    <footer>
      <p>&copy; 2025 - Dzaki Arif Rahman | Universitas Pelita Bangsa</p>
    </footer>
  </div>
</body>
</html>
````

### Screenshot hasil dan codingannya

<img width="1725" height="934" alt="image" src="https://github.com/user-attachments/assets/b2dfb8df-e319-47c8-97a2-3f99bf061811" />


---

### 2. Layout **Contact**

Halaman ini berisi form sederhana.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contact - Dzaki Arif Rahman</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="container">
    <header>
      <h1>Contact Dzaki Arif Rahman</h1>
    </header>

    <nav>
      <a href="home.html">Home</a>
      <a href="artikel.html">Artikel</a>
      <a href="about.html">About</a>
      <a href="kontak.html" class="active">Kontak</a>
    </nav>

    <section id="wrapper">
      <section id="main">
        <h2>Hubungi Saya</h2>
        <p>Silakan isi form di bawah ini untuk mengirim pesan atau pertanyaan:</p>

        <form action="proses.php" method="post">
          <p>
            <label for="nama">Nama</label><br>
            <input type="text" id="nama" name="nama" placeholder="Masukkan nama lengkap" required>
          </p>
          <p>
            <label for="email">Email</label><br>
            <input type="email" id="email" name="email" placeholder="Masukkan alamat email" required>
          </p>
          <p>
            <label for="pesan">Pesan</label><br>
            <textarea id="pesan" name="pesan" rows="5" placeholder="Tulis pesan Anda di sini..."></textarea>
          </p>
          <p>
            <button type="submit">Kirim Pesan</button>
          </p>
        </form>
      </section>

      <aside id="sidebar">
        <div class="widget-box">
          <h3 class="title">Informasi Kontak</h3>
          <ul>
            <li>Email: <a href="mailto:dzaki@example.com">dzaki@example.com</a></li>
            <li>Instagram: <a href="#">@dzakiarif_</a></li>
            <li>Alamat: Bekasi, Jawa Barat</li>
          </ul>
        </div>
      </aside>
    </section>

    <footer>
      <p>&copy; 2025 - Dzaki Arif Rahman | Universitas Pelita Bangsa</p>
    </footer>
  </div>
</body>
</html>

```

### Screenshot hasil dan codingannya

<img width="1730" height="957" alt="image" src="https://github.com/user-attachments/assets/2b91484f-4e95-4bb6-b23c-affa11f4a2d5" />


---

## Penjelasan Layout About

Halaman **About** menampilkan deskripsi diri saya dan daftar portfolio, dengan sidebar tambahan untuk informasi dan link media sosial. 

1. **Struktur HTML**

   * Saya menggunakan `#container` untuk membungkus semua konten halaman. Dengan cara ini, halaman tetap terpusat dan lebih mudah saya atur stylingnya, seperti lebar maksimal dan bayangan (`box-shadow`).
   * Header (`<header>`) berisi judul halaman (`h1`). Dengan menempatkan header di atas, saya bisa memastikan pengguna langsung mengetahui halaman yang sedang mereka buka.
   * Navigasi (`<nav>`) berisi link antar halaman. Link yang aktif (`class="active"`) saya beri styling khusus agar saya dan pengguna tahu posisi kita di website.
   * Section `#main` saya gunakan untuk memuat konten utama, termasuk deskripsi diri, daftar portfolio, dan keahlian.
   * Sidebar (`#sidebar`) menampilkan widget tambahan, seperti bio singkat dan media sosial saya. Sidebar ini membantu memperkaya informasi tanpa mengganggu konten utama.

2. **Penggunaan Float Layout**

   * Saya menggunakan `float: left` pada `#main` dan `#sidebar` agar keduanya tampil berdampingan secara horizontal.
   * Dengan float, konten utama tetap di kiri dan sidebar di kanan, membuat halaman terlihat seimbang.
   * Padding dan margin saya gunakan agar teks tidak menempel pada tepi box, sehingga lebih nyaman dibaca.
   * Saya menyadari kelebihan float adalah mudah membuat layout dua kolom, tapi jika tidak menggunakan `clear` pada footer, footer bisa menempel di samping kolom sehingga posisinya jadi tidak rapi.

3. **Widget Sidebar**

   * Saya membungkus widget dengan `div.widget-box` yang memiliki border dan margin bawah. Border membantu saya memisahkan tiap widget secara visual.
   * Judul widget (`.title`) saya beri background biru dan font putih, supaya menonjol dan mudah dikenali.
   * Daftar link dalam widget saya atur tanpa bullet (`list-style: none`) dan diberi efek hover agar interaktif.
   * Saya menggunakan sidebar untuk melengkapi informasi tanpa mengganggu fokus pada konten utama.

4. **Visualisasi Layout**

   * Layout dua kolom membuat halaman About mudah dibaca, karena konten utama lebih lebar di kiri dan sidebar di kanan tetap terlihat tapi tidak dominan.
   * Saya menggunakan warna, padding, dan margin agar area konten dan sidebar jelas terbagi sehingga tampilan rapi dan profesional.

---

## Penjelasan Layout Contact

Halaman **Contact** menampilkan form agar pengguna bisa mengirim pesan kepada saya:

1. **Struktur Form**

   * Saya menggunakan `method="POST"` agar data dikirim dengan aman ke `proses.php`.
   * Input teks untuk nama (`<input type="text">`) dan email (`<input type="email">`) memastikan saya bisa menerima data utama pengguna.
   * Textarea untuk pesan memungkinkan pengguna menulis pesan panjang.
   * Tombol submit (`<button>`) mengirimkan semua data.
   * Saya menggunakan label untuk setiap elemen form agar pengguna tahu data apa yang harus diisi, sekaligus membantu aksesibilitas.

2. **Sidebar**

   * Sidebar menampilkan informasi kontak saya, seperti email, Instagram, dan alamat.
   * Format widget sama dengan halaman About agar konsistensi desain tetap terjaga.
   * Sidebar tetap menggunakan float, sehingga form berada di kiri dan sidebar di kanan.

3. **Float dan Footer**

   * Saya menggunakan float pada `#main` dan `#sidebar` sehingga dua kolom tetap sejajar.
   * Footer saya beri `clear: both` agar selalu muncul di bawah kedua kolom, tidak menempel pada elemen yang difloat.
   * Dengan begitu, layout tetap rapi meskipun konten atau sidebar bertambah panjang.

---

## Kesimpulan

Dari praktikum ini, saya belajar beberapa hal penting:

* Saya dapat membuat **layout web sederhana** dengan HTML dan CSS, termasuk penggunaan semantic elements seperti `header`, `nav`, `section`, `aside`, dan `footer`.
* Saya memahami konsep **box model**, padding, margin, dan border, yang mempengaruhi jarak dan penampilan elemen.
* Saya belajar bahwa **float layout** berguna untuk membuat dua kolom (konten utama dan sidebar), tapi perlu `clear` pada elemen berikutnya agar footer tetap di posisi yang benar.
* Widget di sidebar membantu saya melengkapi informasi halaman tanpa mengganggu fokus utama.
* Pengetahuan ini menjadi dasar sebelum saya mempelajari layout modern seperti **Flexbox** atau **CSS Grid**, yang lebih fleksibel dan responsif.

Dengan penjelasan ini, saya bisa memahami **alasan di balik setiap elemen dan properti CSS** yang saya gunakan, sehingga bukan hanya menyalin kode, tetapi juga mengerti cara membuat layout web yang rapi dan profesional.



