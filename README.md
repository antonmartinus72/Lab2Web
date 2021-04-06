# PRAKTIKUM PEMROGRAMAN WEB 2
Perintah dalam praktikum ini adalah mempraktikan penulisan ulang kode html beserta css yang sudah ada pada modul yang sudah ada. Penulisan yang sudah lengkap akan mendapatkan hasil seperti ini :

![enter image description here](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/1_ss.jpg)
![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/1_code.jpg)

Selanjutnya kita akan menambahkan dan memodifikasi kode html dan css di atas.

## 1. Backround Gambar
Kita akan mengubah kode css sehingga membentuk tampilabn seperti ini :
![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/2_ss.jpg)

Perubahan di atas terdapat pada warna layout yang berubah dan memiliki transparansi serta terdapat background gambar yang di tambahkan pada css dengan menggunakan selector tag `<body>`.

**1. Layout transparan :**
![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/3_code.jpg)
Untuk format warna `background-color` yang di pakai adalah format **rgba** yang mendukung pewarnaan transparan.

**2. Background gambar :**
![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/2_code.jpg)
Background diatas di buat dengan menggunakan `background-size : cover` yang membuat background memenuhi halaman. 

**3. Hover**
Class "**btn-primary**" pada html juga ditambahkan **Pseudo-Class** yang di tulis pada file css, sehingga tombol tersebut dapat berubah warna saat kursor menyentuh tombol tersebut.

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/4_ss.jpg)

Dapat terlihat warna pada tombol dengan text "Informasi selengkapnya." berubah warna saat kursor menyentuh tombol tersebut.

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/4_css.jpg)

**4. Box Hyperlink**
Selanjutnya adalah menambahkan 3 box hyperlink baru yang jika kita klik akan membawa kita ke halaman lain.

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/5_ss.jpg)

Struktur html yang digunakan :

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/5_code.jpg)

Struktur css yang digunakan :
![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/5_css.jpg)

Disini terdapat selector **container** yang berfungsi sebagai pengatur wilayah yang akan di isi kode lainnya. Untuk masing-masing box menggunakan selectornya sendiri untuk membuat warna background yang berbeda.
Untuk pembentuk dari bentuk kotaknya sendiri menggunakan tag `<a>` sebagai selector.  Ukuran dari kotaknya menggunakan `padding` yang membuat kotak dapat di klik dan berfungsi sebagai hyperlink. `Border` juga di tambahkan untuk membuat garis pada sisi kotak. 

**5. Animasi**

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/6_ss.gif)

Animasi di atas di terapkan di box hyperlink yang sudah dibuat dengan pada bagian **hover**. Terlihat saat kursor menyentuh kotak warna akan berubah ke berbagai warna yang sudah ditentukan.

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/6_css.jpg)

Pada setiap box, sudah di tambahkan `animation-name` yang di gunakan pada `@keyframes`. Animasi berjalan selama 4 detik yang di definisikan pada deklarasi `animation-duration: 4s;` dan akan terus diputar secara berulang tanpa henti pada deklarasi `animation-iteration-count: infinite;`.
Pada `@keyframes` terdapat persentase yang di gunakan untuk menjalankan setiap frame animasi dan di isi dengan warna.

**6. Gambar**
Selanjutnya adalah menambahkan gambar.

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/7_ss.jpg)

Gambar di atas dibuat dengan html yang cukup sederhana :

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/7_code.jpg)

Gambar panda diatas menggunakan selector **container** yang berisi properti `margin` untuk memisahkan gambar dengan objek di atasnya.

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/7_css.jpg)

Untuk selector **.img_container img** menggunakan deklarasi `margin: auto;` yang membuat gambar berada di tengah halaman dengan ukuran menutupi 90% halaman pada properti `width`. Gambar juga diberikan border yang membuat sudut gambar terlihal tumpul pada deklasrasi `border-radius: 5px;`.

**7. Footer**

**Struktur html :**

Pada footer terdapat dua bagian footer dengan id **footer-left** dan **footer-right** yang di isi dengan tag `<span>` dan tag list `<ul>` & `<li>` untuk membuat tampilan daftar.

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/8_code.jpg)

**Tampilan halaman :**

Pada bagian bawah halaman terdapat footer sebagai bagian akhir halaman dengan gradasi warna hitam transparan yang berisi hyperlink. Gradasi warna ini menggunakan property `background-image` yang mendukung gradiasi warna.

![img](https://github.com/antonmartinus72/Lab2Web/raw/main/assets/8_ss.jpg)

Bagian **footer-left** dan **footer-right** ini menggunakan deklarasi `float: left;` untuk membuat kedua bagian menjadi bersebelahan. Bagian ini di isi dengan hyperlink yang disusun secara list. 
Untuk tampilan text pada hyperlink menggunakan selector terpisah yaitu **footer a**. Font dan ukuran font untuk hyperlink juga diganti dengan menggunakan properti `font-family` dan `font-size`. Untuk garis hyperlink dihilangkan dengan menggunakan deklarasi `text-decoration: none;`.

## Menjawab Pertanyaan

**1.** Pertanyaan nomor 1 sudah terjawab pada experimen css di atas.

**2.** Perbedaan selector type `h1 {...}` dan `#intro h1 {...}` terdapat pada kedalaman selector yang mewakili tag html. Selector `h1 {...}` adalah tipe "**Type**". Selector ini mengubah langsung  html dengan menggunakan tag html itu sendiri sebagai selector. 

    <body>
		<div id="intro">
			<h1>...</h1>
		</div>
    </body>

Sedangkan selector `#intro h1 {...}` adalah tipe **"Descendant"** yang ditunjukan pada bagian yang lebih spesifik, yang mengubah tag `<h1>` pada tag html yang memiliki parent tag dengan atribut `id="intro"`.

**3.** Inline css memiliki prioritas pertama yang berarti deklarasi pada internal dan external css akan di timpa. Sedangkan internal css memiliki prioritas di atas extertenal css. 

**Contoh :**
Terdapat 3 properti pada inline css, internal css dan external css yang mengubah tag `<div>` yang mempunyai atribut `class` dengan value `box`  pada file html beriku

**Inline :**
Deklarasi css di dalam atribut `style` dalam tag `<div>`di bawah ini akan menjadikan tag html yang dimaksud mempunyai background berwarna merah yang akan menimpa deklarasi internal dan external css.
Inline css tidak memerlukan atribut seperti `id` atau `class` karena css langsung di terapkan pada bagian yang di maksud.

    `<div class="box" style="background-color: red;">...</div>`
    
**Internal :**
Background pada tag `<div>` akan berubah warna menjadi hijau **hanya jika** tag `<div>` dengan class `.box` diatas tidak memiliki atribut style yang memiliki value css dengan properti `background-color`. Internal html biasanya di susun di dalam tag `<head>` pada file html.

    <style>
		.box {
			background-color: green;
		}
	</style>

**External :**
Background pada tag `<div>` akan berubah warna menjadi biru **hanya jika** inline css dan internal tidak memiliki properti  `background-color` pada tag html yang sama atau class dengan selector yang sama dengan internal css.

    .box {
		background-color: blue;
	}

**4.** Atribut `id` dan `class` pada html yang diterapkan secara bersamaan dapat di gunakan secara bersamaan dengan cara mengkombinasikan kedunya. Namun atribut id dalam css mendapat perioritas pertama. Yaitu apabila keduanya memiliki selector dan properti yang sama dengan value yang berbeda maka value pada selector yang menggunakan id yang akan ditampilkan pada layar.

**Contoh :**
Terdapat baris html seperti berikut :

    <p id="paragraf-1" class="text-paragraf"> TEST ID DAN CLASS</p>

dengan css sebagai berikut :

    #paragraf-1 {
      background-color: red;
    }
    
    .text-paragraf {
      background-color: black;
      color: white;
    }

Warna background yang akan ditampilkan tetap akan berwarna merah walaupun selector dengan tipe **"id"** diletakan di atas kode yang memiliki selector dengan  tipe **"class"**. Meskipun begitu warna text yang ditampilkan akan berwarna putih pada selector dengan tipe **"class"**.