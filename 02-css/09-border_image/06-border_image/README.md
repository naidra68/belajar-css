# Border Image (Shorthand Notation)

Penulisan ini akan menyingkat semua property yang telah saya pelajari sebelumnya. Format penulisan dari `border-image` adalah sebagai berikut.

> border-image: source slice / width / outset repeat;

contoh penulisan

> border-image: url('../img/border`.png' 33 fill / 30px / 30px round);

berikut contoh penerapan-nya

```html
<div class="box box1"></div>
<div class="box box2"></div>
<div class="box box3"></div>
```

```css
.box {
    width: 200px;
    height: 200px;
    line-height: 200px;
    text-align: center;
    color: white;
    font-size: 1.5em;
    background-color: dimgray;
    margin: 3em;
    float: left;
    border: 33px solid transparent;
}
.box1 {border-image: url('../img/border1.png') 33 fill / 30px / 30px round;}
.box2 {border-image: url('../img/border2.png') 20 / 20px / 30px round;}
.box3 {border-image: url('../img/border3.png') 30% / 30px / 0px round;}
```

Jika dijalankan, terlihat bahwa saya membuat beberapa `border-image` dengan penulisan shorthand notation dan gambar border yang berbeda-beda.

# Border Image Gradient

Untuk membuat border image dengan efek gradient, maka bisa menggunakan fungsi dari gradient itu sendiri.

berikut contoh penerapan-nya

```html
<div class="box box4"></div>
```

```css
.box4 {border-image: repeating-radial-gradient(circle, green, lime 10%) 10% / 20px / 20px round;}
```

Ketika dijalankan, maka gambar border-nya akan menggunakan warna gradient. Efek ini dapat dipakai jika dirasa tidak mempunyai gambar untuk dipakai pada `border-image`.