# Text Shadow

Membuat teks dengan ada bayang-bayang itu cukup menarik. CSS3 membuat hal ini bisa dilakukan, dengan property `text-shadow` dapat membuat teks mendapatkan bayang-bayang seperti pada aplikasi pengelola gambar.

Aturan isi dari property ini terdapat 4 pilihan.

- offset-x
- offset-y
- blur-radius
- color

`offset-x` merupakan nilai pertama yang harus ditulis, ini berfungsi untuk mengatur seberapa jauh bayangan yang dihasilkan pada sumbu x (horizontal).

`offset-y` nilai kedua berfungsi untuk mengatur pada sumbu y (vertical).

`blur-radius` nilai ketiga berfungsi untuk mengatur blur pada bayang-bayang.

`color` nilai ke empat adalah untuk mengatur warna dari bayang-bayang.

berikut contoh penerapan-nya

```html
<!-- Offset x dan y -->
<p class="satu">Paragraf Pertama</p>
<p class="dua">Paragraf Kedua</p>
<p class="tiga">Paragraf Ketiga</p>

<!-- blur -->
<p class="empat">Paragraf Keempat</p>
<p class="lima">Paragraf Kelima</p>
<p class="enam">Paragraf Keenam</p>

<!-- color -->
<p class="tujuh">Paragraf Ketujuh</p>
<p class="delapan">Paragraf Kedelapan</p>
<p class="sembilan">Paragraf Sembilan</p>
```

```css
.satu {text-shadow: 15px 0px;}
.dua {text-shadow: -20px 0px;}
.tiga {text-shadow: 15px 15px;}

.empat {text-shadow: 10px 15px 2px;}
.lima {text-shadow: -10px 5px 10px;}
.enam {text-shadow: 20px 15px 5px;}

.tujuh {text-shadow: 10px 15px 5px red;}
.delapan {text-shadow: 10px 0px 5px green;}
.sembilan {text-shadow: 35px 15px 5px blue;}
```

Efek ini cukup menarik di coba dan di kreasikan. Selain 1 efek, ternyata saya bisa membuat 2 efek atau 3 efek sekaligus dalam satu property. Untuk membedakan antar efek pertama dan seterusnya, diakhir code tambahkan koma `,`.

berikut contoh penerapan-nya

```html
<p class="pertama">Paragraf Pertama Extra</p>
<p class="kedua">Paragraf Kedua Extra</p>
<p class="ketiga">Paragraf Ketiga Extra</p>
<p class="keempat">Paragraf Keempat Extra</p>
```

```css
.pertama {
    text-shadow: 4px 3px 0px red,
                 9px 8px 0px rgba(0, 0, 0, 0.15);
}
.kedua {
    text-shadow: -10px 10px 0px #ff00ff,
                 -20px 20px 0px #00ff00;
}
.ketiga {
    text-shadow: 1px 1px 2px black,
                 0 0 1em blue,
                 0 0 0.2em blue;
}
.keempat {
    text-shadow: 0px 3px 0px #b2a98f,
                 0px 14px 10px rgba(0, 0, 0, 0.15),
                 0px 24px 2px rgba(0, 0, 0, 0.1),
                 0px 34px 30px rgba(0, 0, 0, 0.1);
}
```