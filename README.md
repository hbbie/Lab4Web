# Lab4Web
Tugas Pertemuan 5 Pemrograman Web

Nama : Dhani Naufal Habibie

Kelas : T.I.24.A4

NIM : 312410300

# Langkah-langkah Praktikum
Persiapan membuat dokumen HTML dengan nama file lab4_box.html seperti berikut.
1. Membuat Box Element
Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut.
2. CSS Float Property
Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut.

# Membuat Box Element Sederhana

kode program : 

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
<section>
<div class="div1">Div 1</div>
<div class="div2">Div 2</div>
<div class="div3">Div 3</div>
<div class="div4">Div 4</div>
</section>

<style>
div {
float:left;
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
.div4 {
background-color: blue;
clear: both;
float: none;
}
</style>

```

Penjelasan :


<!DOCTYPE html> → Menandakan bahwa dokumen ini menggunakan HTML5.


<html lang="en"> → Menentukan bahasa utama halaman yaitu bahasa Inggris.


<head> → Berisi metadata seperti charset (UTF-8), viewport (untuk tampilan responsif), dan judul halaman (“Box Element”).


<body> → Berisi konten utama halaman.


<header> → Bagian kepala halaman, berisi judul <h1>Box Element</h1>.

iv { float:left; padding:10px; }
➜ Semua elemen <div> akan mengapung ke kiri dan memiliki jarak dalam (padding) sebesar 10 piksel.
➜ Ini menyebabkan div1, div2, dan div3 sejajar secara horizontal.

.div1, .div2, .div3 → Masing-masing diberi warna latar berbeda:

div1 → merah

div2 → kuning

div3 → hijau

.div4:

background-color: blue; → Latar belakang biru

clear: both; → Menghentikan efek float dari elemen sebelumnya

float: none; → Membuat elemen ini kembali ke posisi normal (bukan float)
➜ Hasilnya, Div 4 akan muncul di bawah tiga kotak pertama.

📊 Kesimpulan Tampilan

Ketika dijalankan di browser:

“Box Element” tampil di bagian atas sebagai judul.

Di bawahnya, tiga kotak berwarna merah, kuning, dan hijau akan sejajar secara horizontal.

Kotak keempat (biru) akan berada di bawah ketiganya, menempati baris baru.


<img width="1919" height="1077" alt="Screenshot 2025-10-16 132241" src="https://github.com/user-attachments/assets/2fd3cab7-c6f7-47db-9976-c8ebdb82672b" />


3. Mengatur Clearfix Element
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk mengaturnya.
Tambahkan element div lainnya seteleah div3 seperti berikut.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
    <style>
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

        .div4 {
            background-color: blue;
            clear: left;
            float: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>

    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
    </section>
</body>
</html>
```

Hasilnya :

<img width="1919" height="1079" alt="Screenshot 2025-10-16 132634" src="https://github.com/user-attachments/assets/88a91853-1941-46c9-8b3f-e6576370e0b0" />
# Membuat Layout Sederhana
Kita akan membuat layout web sederhana seperti gambar berikut. Buat folder baru dengan nama lab4_layout, kemudian buatlah file baru didalamnya dengan nama
home.html, dan file css dengan nama style.css.
```
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
    </div>

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

Hasilnya :

<img width="1919" height="1079" alt="Screenshot 2025-10-16 133337" src="https://github.com/user-attachments/assets/974aeba3-386c-4e2e-aed4-a709f295e361" />


Kemudian tambahkan kode CSS untuk membuat layoutnya.
```
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

* {
    margin: 0;
    padding: 0;
}

body {
    line-height: 1;
    font-size: 100%;
    font-family: 'Open Sans', sans-serif;
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

Hasilnya : 

<img width="1909" height="1079" alt="Screenshot 2025-10-16 134101" src="https://github.com/user-attachments/assets/2c5e8c02-e3c0-4aae-9157-ea7a89c051de" />


4. Membuat Navigasi
Kemudian selanjutnya mengatur navigasi.
```
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

* {
    margin: 0;
    padding: 0;
}

body {
    line-height: 1;
    font-size: 100%;
    font-family: 'Open Sans', sans-serif;
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

Hasilnya :
<img width="1919" height="1079" alt="Screenshot 2025-10-16 134141" src="https://github.com/user-attachments/assets/daf95098-2e18-4c97-9d7f-12413ec94a66" />



5. Membuat Hero Panel.
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.
versi html
```
    <section id="hero">
        <h1>Hello World!</h1>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.
            Proin in leo fringilla, vestibulum mi porta, faucibus felis.
            Integer pharetra est nunc, nec pretium nunc pretium ac.
        </p>
        <a href="home.html">Learn more &raquo;</a>
    </section>

    <footer>
        <p>&copy; 2021 - Universitas Pelita Bangsa</p>
    </footer>
```
versi css

```
#hero {
    background-color: #e4e4e5;
    padding: 20px;
}

#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
    color: #333;
}

#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
    color: #555;
}
```

Hasilnya :

<img width="1919" height="1079" alt="Screenshot 2025-10-16 134639" src="https://github.com/user-attachments/assets/637fda78-cb7a-4d51-8a91-c1d8118ef2b3" />

6. Mengatur Layout Main dan Sidebar
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.
7. Membuat Sidebar Widget
Kemudian selanjutnya menambahkan element lain dalam sidebar.
untuk html nya
```
<aside class="sidebar">
            <div class="widget">
                <h3 class="widget-title">Widget Header</h3>
                <ul>
                    <li><a href="#">Widget Link</a></li>
                    <li><a href="#">Widget Link</a></li>
                    <li><a href="#">Widget Link</a></li>
                    <li><a href="#">Widget Link</a></li>
                    <li><a href="#">Widget Link</a></li>
                </ul>
            </div>
            <div class="widget">
                <h3 class="widget-title">Widget Text</h3>
                <p>
                    Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. 
                    Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, 
                    nec pretium nunc pretium ac.
                </p>
            </div>
        </aside>
```
untuk css
```
#wrapper {
    margin: 0;
}

#main {
    float: right;
    width: 640px;
    padding: 20px;
}

#sidebar {
    float: right;
    width: 260px;
    padding: 20px;
}

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

footer {
    clear: both;
    background-color: #d1d1d1;
    padding: 20px;
    color: #eee;
}
```
Hasilnya :

![gambar](https://github.com/Abcdeflahhh/Lab4WEBPW/blob/7f00390caadaacab9a48f38224746b559af4e8a6/image/2025-10-16%2017_21_41-Layout%20Sederhana%20-%20Prak4PW%20-%20Aflah%20-%20Visual%20Studio%20Code.png47.png)

8. Mengatur Footer
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.
Menambahkan Elemen lainnya pada Main Content

untuk html
```
<article class="entry">
                <h2>First featurette heading.</h2>
                <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, 
                    iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
                    vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.
                </p>
            </article>

            <hr class="divider" />

            <article class="entry">
                <h2>Second featurette heading.</h2>
                <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, 
                    iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
                    vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.
                </p>
            </article>
        </section>
```

untuk css
```
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
  color: #333;
}

.entry p {
  line-height: 25px;
}

.entry img {
  float: left;
  border-radius: 5px;
  margin-right: 15px;
}
```

Hasilnya : 

![gambar](https://github.com/Abcdeflahhh/Lab4WEBPW/blob/bc7eeb09c71923933fff94d0850ec67f37ed9ac5/image/2025-10-16%2017_23_26-Layout%20Sederhana%20-%20Personal%20-%20Microsoft%E2%80%8B%20Edge.png48.png)

9. Menambahkan Elemen lainnya pada Main Content dan Artikel

Kode Program (html) :
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>

    <style>
        /* Import Google Font */
        @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700;800&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:wght@300;700&display=swap');

        /* Reset CSS */
        * {
            margin: 0;
            padding: 0;
        }

        body {
            line-height: 1.5;
            font-size: 100%;
            font-family: 'Open Sans', sans-serif;
            color: #5a5a5a;
            background-color: #f9f9f9;
        }

        /* Container */
        #container {
            width: 980px;
            margin: 20px auto;
            box-shadow: 0 0 1em #cccccc;
            background: #fff;
        }

        /* Header */
        header {
            padding: 20px;
            background: #fafafa;
        }

        header h1 {
            color: #b5b5b5;
        }

        /* Navigasi */
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

        /* Hero Panel */
        #hero {
            background-color: #e4e4e5;
            padding: 50px 20px;
            margin-bottom: 20px;
            text-align: center;
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

        .btn {
            background-color: #1f5faa;
            color: #fff;
            padding: 10px 20px;
            border-radius: 4px;
            text-decoration: none;
        }

        .btn:hover {
            background-color: #2b83ea;
        }

        /* Wrapper */
        #wrapper {
            display: flex;
            padding: 20px;
        }

        /* Main Content */
        #main {
            flex: 3;
            background: #ffffff;
            margin-right: 10px;
            padding: 20px;
        }

        /* Sidebar */
        #sidebar {
            flex: 1;
            background: #f3f3f3;
            padding: 20px;
        }

        /* Widget */
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

        /* Box */
        .row {
            margin: 0 -10px;
            display: flex;
        }

        .box {
            width: 33.33%;
            box-sizing: border-box;
            padding: 0 10px;
            text-align: center;
        }

        .box img {
            border-radius: 50%;
            border: 0;
            vertical-align: middle;
        }

        .box h3 {
            margin: 15px 0;
        }

        .box p {
            font-size: 14px;
            margin-bottom: 15px;
        }

        /* Divider */
        .divider {
            border: 0;
            border-top: 1px solid #eeeeee;
            margin: 40px 0;
        }

        /* Entry / Artikel */
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
            margin-left: 15px;
        }

        /* Footer */
        footer {
            clear: both;
            background-color: #1d1d1d;
            padding: 20px;
            color: #eee;
            text-align: center;
        }
    </style>
</head>

<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>

    <nav>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="artikel.html">Artikel</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="contact.html">Kontak</a></li>
  </ul>
    </nav>


        <section id="hero">
            <h1>Hello World!</h1>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit,
                iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.
            </p>
            <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
        </section>

        <section id="wrapper">
            <section id="main">
                <div class="row">
                    <div class="box">
                        <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>

                    <div class="box">
                        <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>

                    <div class="box">
                        <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                </div>

                <hr class="divider" />

                <article class="entry">
                    <h2>First featurette heading</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
                        elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
                        pretium ac.</p>
                </article>

                <hr class="divider" />

                <article class="entry">
                    <h2>Second featurette heading</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
                        elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
                        pretium ac.</p>
                </article>
            </section>

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
                        Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra
                        est nunc, nec pretium nunc pretium ac.
                    </p>
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
Kode Css :
```css
/* Import Google Font */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700;800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:wght@300;700&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Body */
body {
    line-height: 1.5;
    font-size: 100%;
    font-family: 'Open Sans', sans-serif;
    color: #5a5a5a;
    background-color: #f9f9f9;
}

/* Container utama */
#container {
    width: 980px;
    margin: 20px auto;
    box-shadow: 0 0 1em #cccccc;
    background: #fff;
}

/* Header */
header {
    padding: 20px;
    background: #fafafa;
}

header h1 {
    color: #1f5faa;
    font-weight: 700;
}

/* Navigasi */
nav {
    display: block;
    background-color: #1f5faa;
}

nav ul {
    list-style: none;
}

nav ul li {
    display: inline-block;
}

nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
    transition: 0.3s;
}

nav a.active,
nav a:hover {
    background-color: #2b83ea;
}

/* Hero Section */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
    text-align: center;
}

#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
    color: #333;
}

#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
    color: #555;
}

/* Tombol */
.btn {
    background-color: #1f5faa;
    color: #fff;
    padding: 10px 20px;
    border-radius: 4px;
    text-decoration: none;
    font-weight: 600;
    transition: 0.3s;
}

.btn:hover {
    background-color: #2b83ea;
}

/* Wrapper utama */
#wrapper {
    display: flex;
    flex-wrap: wrap;
    padding: 20px;
}

/* Main content */
#main {
    flex: 3;
    background: #ffffff;
    margin-right: 10px;
    padding: 20px;
}

/* Sidebar */
#sidebar {
    flex: 1;
    background: #f3f3f3;
    padding: 20px;
}

/* Widget box */
.widget-box {
    border: 1px solid #eee;
    margin-bottom: 20px;
    border-radius: 5px;
    overflow: hidden;
}

.widget-box .title {
    padding: 10px 16px;
    background-color: #428bca;
    color: #fff;
    font-weight: bold;
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
    transition: 0.3s;
}

.widget-box li:hover a {
    background-color: #eee;
}

.widget-box p {
    padding: 15px;
    line-height: 25px;
}

/* Box Layout */
.row {
    margin: 0 -10px;
    display: flex;
    flex-wrap: wrap;
}

.box {
    width: 33.33%;
    box-sizing: border-box;
    padding: 0 10px;
    text-align: center;
}

.box img {
    border-radius: 50%;
    border: 0;
    vertical-align: middle;
}

.box h3 {
    margin: 15px 0;
    color: #1f5faa;
}

.box p {
    font-size: 14px;
    margin-bottom: 15px;
}

/* Divider */
.divider {
    border: 0;
    border-top: 1px solid #eeeeee;
    margin: 40px 0;
}

/* Artikel */
.entry {
    margin: 15px 0;
}

.entry h2 {
    margin-bottom: 20px;
    color: #1f5faa;
}

.entry p {
    line-height: 25px;
    text-align: justify;
}

.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}

.entry .right-img {
    float: right;
    margin-left: 15px;
}

/* Formulir Kontak */
form {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-top: 15px;
}

input, textarea {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-family: inherit;
    font-size: 14px;
}

textarea {
    resize: none;
    height: 120px;
}

button {
    background-color: #1f5faa;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-weight: 600;
    transition: 0.3s;
}

button:hover {
    background-color: #2b83ea;
}

/* Footer */
footer {
    clear: both;
    background-color: #1d1d1d;
    padding: 20px;
    color: #eee;
    text-align: center;
    font-size: 14px;
    margin-top: 20px;
}

/* Responsif */
@media (max-width: 768px) {
    #container {
        width: 95%;
    }

    #wrapper {
        flex-direction: column;
    }

    #main, #sidebar {
        width: 100%;
        margin-right: 0;
    }

    .box {
        width: 100%;
        margin-bottom: 20px;
    }

    nav ul li {
        display: block;
        text-align: center;
    }

    nav a {
        padding: 12px;
        display: block;
    }
}

```

Hasilnya :

<img width="1919" height="1079" alt="Screenshot 2025-10-16 142125" src="https://github.com/user-attachments/assets/e8660450-5fb3-46f2-8807-358a05cb9b59" />


SELESAI.

SOAL & PERTANYAAN

![gambar](https://github.com/Abcdeflahhh/Lab4WEBPW/blob/cb2a65e7f3608ea990aec0b988de425af850400f/image/Screenshot%20from%202025-10-15%2019-22-47.png)

JAWABAN :

1
Buatlah File dalam  about.html dalam folder
<img width="158" height="33" alt="image" src="https://github.com/user-attachments/assets/26a3c4cf-a929-4dad-ae7c-d97428de0e91" />

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About - Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<div id="container">
    <header>
        <h1>Tentang Kami</h1>
    </header>

    <nav>
        <ul>
            <li><a href="index.html">Home</a></li>
            <li><a href="artikel.html">Artikel</a></li>
            <li><a href="about.html" class="active">About</a></li>
            <li><a href="contact.html">Kontak</a></li>
        </ul>
    </nav>

    <section id="hero">
        <h1>Selamat Datang di Halaman About</h1>
        <p>Kami adalah tim kreatif yang berfokus pada pengembangan web modern, desain menarik, dan solusi digital inovatif.</p>
    </section>

    <section id="wrapper">
        <section id="main">
            <article class="entry">
                <h2>Deskripsi Perusahaan</h2>
                <p>
                    Kami berdiri sejak tahun 2020 dengan tujuan membantu UMKM dan bisnis lokal bertransformasi ke dunia digital.
                    Tim kami terdiri dari desainer, pengembang, dan digital strategist berpengalaman.
                </p>
            </article>

            <hr class="divider" />

            <article class="entry">
                <h2>Portfolio Kami</h2>
                <div class="row">
                    <div class="box">
                        <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="">
                        <h3>Website Toko Online</h3>
                        <p>Proyek e-commerce dengan fitur katalog, cart, dan sistem pembayaran otomatis.</p>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="">
                        <h3>Aplikasi Mobile</h3>
                        <p>Desain aplikasi mobile interaktif untuk layanan pesan antar makanan.</p>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/db7d25/fff.png" alt="">
                        <h3>Sistem Informasi</h3>
                        <p>Pengembangan sistem manajemen data internal berbasis web untuk perusahaan.</p>
                    </div>
                </div>
            </article>
        </section>

        <aside id="sidebar">
            <div class="widget-box">
                <h3 class="title">Info Singkat</h3>
                <p>Kami berbasis di Bekasi, Jawa Barat. Melayani klien dari seluruh Indonesia.</p>
            </div>
            <div class="widget-box">
                <h3 class="title">Sosial Media</h3>
                <ul>
                    <li><a href="#">Instagram</a></li>
                    <li><a href="#">LinkedIn</a></li>
                    <li><a href="#">Facebook</a></li>
                    <li><a href="#">YouTube</a></li>
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
<img width="1919" height="1072" alt="image" src="https://github.com/user-attachments/assets/8449e4e4-8ddb-4014-b64e-c36c12000698" />


2. Buatlah File dalam  contact.html dalam folder
<img width="244" height="186" alt="image" src="https://github.com/user-attachments/assets/14f454ae-b9bc-4e59-81a2-51455b16a68b" />

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kontak Kami - Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
    <style>
        form {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        input, textarea {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-family: inherit;
        }

        textarea {
            resize: none;
            height: 120px;
        }

        button {
            background-color: #1f5faa;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #2b83ea;
        }
    </style>
</head>
<body>
<div id="container">
    <header>
        <h1>Kontak Kami</h1>
    </header>

    <nav>
        <ul>
            <li><a href="index.html">Home</a></li>
            <li><a href="artikel.html">Artikel</a></li>
            <li><a href="about.html">About</a></li>
            <li><a href="contact.html" class="active">Kontak</a></li>
        </ul>
    </nav>

    <section id="hero">
        <h1>Hubungi Kami</h1>
        <p>Kami siap membantu Anda! Silakan kirim pesan melalui form berikut untuk pertanyaan atau kerja sama.</p>
    </section>

    <section id="wrapper">
        <section id="main">
            <article class="entry">
                <h2>Formulir Kontak</h2>
                <form action="#" method="post">
                    <label for="nama">Nama:</label>
                    <input type="text" id="nama" name="nama" placeholder="Masukkan nama Anda" required>

                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" placeholder="Masukkan email Anda" required>

                    <label for="pesan">Pesan:</label>
                    <textarea id="pesan" name="pesan" placeholder="Tulis pesan Anda..." required></textarea>

                    <button type="submit">Kirim Pesan</button>
                </form>
            </article>
        </section>

        <aside id="sidebar">
            <div class="widget-box">
                <h3 class="title">Alamat Kami</h3>
                <p>
                    Jl. Raya Cikarang No. 123<br>
                    Bekasi, Jawa Barat 17530<br>
                    Email: info@layoutsimple.id<br>
                    Telp: (021) 9876543
                </p>
            </div>

            <div class="widget-box">
                <h3 class="title">Jam Operasional</h3>
                <ul>
                    <li>Senin - Jumat: 08.00 - 17.00</li>
                    <li>Sabtu: 09.00 - 15.00</li>
                    <li>Minggu: Tutup</li>
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
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b4acdff3-7ea2-4820-a885-bcbc0fac2b2a" />




