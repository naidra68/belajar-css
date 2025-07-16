# Media Query : Width dan Height

Aturan yang sering dipakai untuk media query adalah mengatur lebar element (`width`) dan tinggi element (`height`).

Width dan Height pada aturan media query ini adalah merujuk ke lebar dan tinggi jendela web browser (`viewport`).

## 1. Media Query : Width

Dengan media query width, developer bisa membuat kode CSS yang dapat dijalankan pada lebar tertentu saja.

berikut contoh penerapan-nya

```html
<div class="box box1"></div>
```

```css
.box {
    width: 800px;
    height: 100px;
    line-height: 100px;
    text-align: center;
    font-size: 1.2em;
    margin: 2em auto;
}
.box1 {
    background-color: green;
}
@media (width: 500px) {
    .box1 {
        background-color: red;
    }
}
```

Jika dijalankan, terlihat bahwa saat developer mencoba mengecilkan jendela web browser hingga ke `width:600px` maka warna dari element `box1` menjadi berwarna merah.

Namun, dengan ini jadi susah diatur lebar-nya karena jika developer menambah dan mengurangi 1px pun antara 601px dan 599px maka dia akan berubah menjadi warna hijau.

Maka dari itu, untuk mengatasi masalah ini, css menambahkan prefix ke dalam media query dengan max dan min untuk mengatur lebar. 

berikut contoh penerapan-nya.

```html
<div class="box box2">Max-Width 600px</div>
```

```css
.box2 {
    background-color: green;
}

@media (max-width: 600px) {
    .box2 {
        background-color: blue;
    }
}
```

Jika dijalankan, terlihat bahwa saat developer mengecilkan jendela web browser hingga 600px, maka tampil warna biru dan ketika diperbesar sedikit menjadi 601px maka dia akan tampil biru. Apabila diperkecil sampai 0px pun tampil warna biru.

Sekarang saya akan mencoba menggunakan nilai minimum dan maximum untuk mengatur lebar layar-nya, karena css tidak terbatas dengan 1 isi media query saja, namun dapat di chaining menjadi aturan yang lebih spesifik.

berikut contoh penerapan-nya

```html
<div class="box box3">Min-Width 400px dan Max-Width 600px</div>
```

```css
.box3 {
    background-color: green;
}

@media (min-width: 400px) and (max-width: 600px) {
    .box3 {
        background-color: magenta;
    }
}
```

Jika dijalankan, terlihat bahwa setiap jendela web browser dikecilkan sampai 600px maka element akan menjadi warna magenta sampai dengan 400px, ketika dikecilkan lagi setelah melewati 400px, maka element akan menjadi warna hijau lagi.

Sebelum mengatur tinggi element, saya akan mencoba melakukan responsive element dengan mengatur lebar element sesuai ukuran layar.

berikut contoh penerapan-nya

```html
<div class="box box4">Element ini akan berubah-ubah ukuran.</div>
```

```css
.box4 {
    background-color: red;
}

@media (min-width: 600px) and (max-width: 800px) {
    .box4 {
        width: 550px;
    }
}
@media (min-width: 400px) and (max-width: 600px) {
    .box4 {
        width: 300px;
    }
}
```

Jika dijalankan, terlihat bahwa lebar element akan berubah-ubah sesuai set dari min dan max width-nya. Silahkan dicoba perkecil dan perbesar jendela web browser.

## 1. Media Query : Height

Breakpoint merupakan titik dimana layout atau tampilan website akan berubah mengikuti apa yang ditulis di dalam media query. Semua contoh yang telah dibuat merupakan istilah breakpoint. Batasan breakpoint juga bisa menggunakan nilai height viewport.

berikut contoh penerapan-nya

```html
<div class="box box5">Berubah-ubah warna sesuai tinggi viewport</div>
```

```css
.box5 {
    background-color: green;
}

@media (max-height: 200px) {
    .box5 {
        background-color: gray;
    }
}
@media (min-height: 201px) and (max-height: 400px) {
    .box5 {
        background-color: blue;
    }
}
```

Jika dijalankan, terlihat bahwa warna element akan berubah sesuai breakpoint dari tinggi element. Apabila element melebihi tinggi 400px maka dia akan menjadi warna hijau, ketika tinggi antar 201px dan 400px maka dia akan menjadi warna biru, terakhir jika tinggi maksimal 200px maka akan menjadi warna abu-abu.

<hr>

Dengan memahami media query untuk mengatur lebar dan tinggi element agar responsive seperti ini cukup untuk membuat layout responsive. Terlihat cukup menarik, bukan?