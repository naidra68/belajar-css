# Box Shadow Blur Radius

Setelah penulisan offset-x dan offset-y, maka nilai selanjutnya adalah nilai untuk mengatur blur-radius dari sebuah `box-shadow`. Nilainya bisa diisi dengan seluruh satuan width positif.

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
    height: 200px;
    background-color: green;
    float: left;
    margin: 1.5em;
}
.box1 {box-shadow: 10px 10px 3px;}
.box2 {box-shadow: 20px 20px 10px;}
.box3 {box-shadow: 10px 10px 15px;}
.box4 {box-shadow: 20px 20px 20px;}
```

Jika dijalankan, terlihat bahwa semakin banyak nilai yang disi **blur-radius**, maka semakin buram juga box-shadow-nya.