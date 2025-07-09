# Text Decoration

Property yang cukup banyak digunakan adalah `text-decoration`. Property ini berfungsi untuk dekorasi teks seperti membuat garis bawah,garis atas, dan garis tercoret.

Terdapat 2 pemhasan mengenai `text-decoration` ini, `text-decoration` memiliki property tambahan pada CSS3.

## Text Decoration (CSS2)

berikut ini beberapa isi dari text-decoration.
- underline
- overline
- line-trought
- none

berikut contoh penerapan-nya

```html
<p class="underline">Underline</p>
<p class="overline">Overline</p>
<p class="line-trought">Line Trought</p>
<p class="none">None</p>
<p class="all">All Value</p>
```

```css
.underline {text-decoration: underline;}
.overline {text-decoration: overline;}
.line-trought {text-decoration: line-through;}
.none {text-decoration: none;}
.all {text-decoration: underline overline line-through;}
```

Apabila digabung dengan property `color`, maka `text-decoration` akan menyesuaikan `color` nya.

Dengan pemahaman property `color`,`background-color`,`text-decoration`, pseudo class selector `:hover`, dan berbagai macam selector. Maka, saya bisa membuat sebuah navigasi bar sederhana.

berikut contoh penerapan-nya.

```html
<ul>
    <li><a href="#">HOME</a></li>
    <li><a href="#">ABOUT</a></li>
    <li><a href="#">PROJECT</a></li>
    <li><a href="#">CONTACT</a></li>
</ul>
```

```css
/* Membuat navbar sederhana */

ul li a {
    text-decoration: none;
    color: white;
    background-color: black;
}
ul li a:hover {
    color: red;
    background-color: yellow;
}
```

Jika dijalankan, memang terlihat jelek sekali 😂. Namun dengan ini saya bisa melihat betapa kompleks-nya CSS jika digabungkan dan dapat menghasilkan tampilan seperti itu.


## Text Decoration (CSS3)

Terdapat 3 property baru untuk `text-decoration` pada CSS3.

- text-decoration-line
- text-decoration-style
- text-decoration-color

`text-decoration-line` sama seperti `text-decoration`, nilai-nya pun sama persis.

`text-decoration-style` berfungsi untuk mengatur jenis garis, dan bisa diisi dengan solid, double, dotted, dashed atau wavy.

`text-decoration color` berfungsi untuk mengatur warna garis, nilainya bisa berupa kode warna yang kita pelajari pada property color, yakni keyword, warna RGB/RGBA maupun HSL/HSLA.

berikut contoh penerapan-nya

```html
<p class="satu">Paragraf Pertama</p>
<p class="dua">Paragraf Kedua</p>
<p class="tiga">Paragraf Ketiga</p>
```

```css
.satu {
    text-decoration-line: underline;
    text-decoration-style: solid;
    text-decoration-color: green;
}
.dua {
    text-decoration-line: overline;
    text-decoration-style: dashed;
    text-decoration-color: red;
}
.tiga {
    text-decoration-line: line-through;
    text-decoration-style: wavy;
    text-decoration-color: hsla(240, 100%, 50%, 0.9);
}
```

Selain penulisan satu-persatu property-nya, saya bisa meringkas penulisan menjadi satu property menggunakan `text-decoration`.

```css
.satu {
    text-decoration: underline solid green;
}
.dua {
    text-decoration: overline dashed red;
}
.tiga {
    text-decoration: line-through wavy hsla(240, 100%, 50%, 0.9);
}
```

Jika dijalankan, kode css diatas dianggap valid dan benar. Cara penulisan seperti ini biasa-nya disebut sebagai **Shorthand Notation**.