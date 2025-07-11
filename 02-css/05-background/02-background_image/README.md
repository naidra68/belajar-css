# Background Image

Jika background dengan berbagai pilihan warna masih kurang menarik, saatnya gunakan gambar. Property background-image berfungsi untuk memasukkan gambar ke dalam background sebuah element HTML.

berikut contoh penerapan-nya

```css
body {
    background-image: url('wallpaper.png');
}
```

Jika dijalankan, `<body>` akan menampilkan gambarnya selayar full karena saya definisikan pada parent element. Bagaimana jika saya gunakan element lain seperti div?

Jawabannya bisa, saya akan menggunakan beberapa gambar untuk membuat sebuah list-list gambar beserta keterangan ditengah-nya.

berikut contoh penerapan-nya

```html
<div class="box satu"><span>Jeruk</span></div>
<div class="box dua"><span>Strawberry</span></div>
<div class="box tiga"><span>Kiwi</span></div>
<div class="box empat"><span>Blueberry</span></div>
```

```css
span {
    background-color: white;
    padding: 0.5em;
    border-radius: 5px;
}
.satu {background-image: url('../img/jeruk.jpg');}
.dua {background-image: url('../img/strawberry.png');}
.tiga {background-image: url('../img/kiwi.png');}
.empat {background-image: url('../img/bluebeerry.png');}
```

Jika dijalankan, saya membuat tampilan beberapa gambar buah dengan keterangan dari gambar tersebut.

# Background Image CSS3

Property ini telah diperbarui pada CSS3, salah satu fitur-nya adalah daoat membuat banyak gambar sekaligus. Teknik ini dikenal dengan **multiple background**. Setiap input dipisah dengan tanda koma `,`.

berikut contoh penerapan-nya

```html
<div class="box multiple"></div>
```

```css
.multiple {
    background-image: url('../img/kiwi100x100.png'),
                      url('../img/jeruk.jpg');
}
```

Jika dijalankan, terlihat hanya tampil gambar pertama yang didefinisikan, namun sebenar-nya gambar tersebut ketumpuk, jadi gambar yang tidak terlihat ada dibelakang gambar pertama.

Ketika dilihat secara seksama, gambar kiwi akan tampil secara berulang kali dan memenuhi lebar element dan menutupi gambar kedua. Untuk menghilangkan efek tersebut ada property background lain.
