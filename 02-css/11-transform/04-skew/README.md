# Transform Skew

Efek `skew` adalah mengubah sudut elment pada sumbu vertikal, horizontal ataupun kedua-nya. Efek yang dihasilkan seperti element tersebut ditarik ke arah tertentu.

sama seperti `scale`, untuk membuat `skew` terdapat 2 nilai yang dapat digunakan yaitu `skewX` dan `skewY`. Untuk penulisan shorthand notation bisa gunakan `skew`.

berikut contoh penerapan-nya

```html
<div class="box box1"></div>
<div class="box box2"></div>
<div class="box box3"></div>
<div class="box box4"></div>
```

```css
.box {
    width: 200px;
    height: 80px;
    background-color: green;
    float: left;
    margin: 1.5em;
}
.box1 {transform: skew(30deg, 15deg);}
.box2 {transform: skewX(15deg);}
.box3 {transform: skewY(15deg);}
.box4 {transform: skewX(-60deg) skewY(15deg);}
```

Jika dijalankan, terlihat bahwa element tersebut seperti merenggang dari ukuran asli-nya. Menggunakan `skew` dapat membuat element berbentuk menarik seperti itu.