# Linear Gradient

Pembuatan efek gradient paling sederhana adalah menggunakan `linear-gradient`. Gradiasi warna akan terjadi pad sebuah garis lurus.

berikut contoh penerapan-nya

```html
<!-- Linear Gradient 2 Warna -->
<div class="linear-gradient">
    <div class="box box1">
        <span>Red</span>
    </div>
    <div class="box box2">
        <span>Green</span>
    </div>
    <div class="box box3">
        <span>Blue</span>
    </div>
</div>
```

```css
.linear-gradient {
    width: 80%;
    height: 160px;
    text-align: center;
    margin: 1em auto;
    background-color: dimgray;
    padding: 1em;
}
.box {
    width: 160px;
    height: 160px;
    line-height: 160px;
    float: left;
}
.box > span {
    color: white;
    background-color: black;
    padding: 0.5em;
}
.box1 {background-image: linear-gradient(red, white);}
.box2 {background-image: linear-gradient(green, white);}
.box3 {background-image: linear-gradient(blue, white);}
```

Ketika dijalankan, terlihat bahwa efek gradiasi dimulai dari atas dengan warna merah lalu kebawah akan menjadi warna putih.

## Linear Stop

Warna gradient seperti contoh diatas biasanya disebut sebagai **color stop**, perintah untuk isi `linear-gradient` setidaknya harus ada 2 warna yakni warna awal dan warna akhir.

Ketika saya ingin membuat warna lebih dari 2 warna seperti 3 warna, 4 warna dan seterusnya pada `liner-gradient`, maka cukup tambahkan color stop ke dalam `linear-gradint` color stop ini dipisah dengan tanda koma.

berikut contoh penerapan-nya

```html
<!-- Linear Gradient 2 Warna -->
<div class="linear-gradient">
    <div class="box box4">
        <span>Red</span>
    </div>
    <div class="box box5">
        <span>Green</span>
    </div>
    <div class="box box6">
        <span>Blue</span>
    </div>
</div>
```

```css
.box4 {background-image: linear-gradient(red, green, blue);}
.box5 {background-image: linear-gradient(cyan, magenta, yellow,black);}
.box6 {background-image: linear-gradient(red, orange, yellow,lime ,limegreen, cyan, blue, purple, magenta);}
```

## Linear Length

Ketika diperhatikan, semua efek warna akan disebar secara merata. Untuk mengatur ukuran efek warna ini bisa gunakan perintah satuan length setelah memasukkan perintah warna.

berikut contoh penerapan-nya

```html
<!-- Linear Gradient Length -->
<div class="linear-gradient">
    <div class="box box7">
        <span>Box 1</span>
    </div>
    <div class="box box8">
        <span>Box 2</span>
    </div>
    <div class="box box9">
        <span>Box 3</span>
    </div>
</div>
```

```css
.box7 {
    background-image: linear-gradient(red 25%, blue 50%, red 100%);
}
.box8 {
    background-image: linear-gradient(cyan 25%, yellow 50%, magenta 75%, black 100%);
}
.box9 {
    background-image: linear-gradient(red 10%,orange 20%, yellow 30%,
                                    lime 40%, green 50%, blue 60%,
                                    cyan 70%, pink 80%, magenta 90%,
                                    purple 100%);
}
```

Ketika dijalanakan, terlihat bahwa saya membuat semua warna dengan bantuan ukuran gradient dimasing-masing warna secara berbeda.

## Linear Direction

Sejauh ini, warna dari gradient dimulai dari atas dan bawah. Untuk mengganti aturan ini, biasanya menggunakan perintah direction diawal nilai sebelum mendefinisikan warna gradient. Isi dari direction ini bisa gunakan keyword arah ataupun menggunakan sudut.

Saya akan coba terlebih dahulu menggunakan keyword arah seperti `to left`, `to right`, `to bottom`, `to top`.

berikut contoh penerapan-nya

```html
    <!-- Linear Gradient Direction Keyword -->
<div class="linear-gradient1">
    <div class="box box10">
        <span>Box 1</span>
    </div>
    <div class="box box11">
        <span>Box 2</span>
    </div>
    <div class="box box12">
        <span>Box 3</span>
    </div>
    <div class="box box13">
        <span>Box 4</span>
    </div>
    <div class="box box14">
        <span>Box 5</span>
    </div>
    <div class="box box15">
        <span>Box 6</span>
    </div>
    <div class="box box16">
        <span>Box 7</span>
    </div>
    <div class="box box17">
        <span>Box 8</span>
    </div>
</div>
```

```css
.linear-gradient1 {
    width: 80%;
    height: 480px;
    text-align: center;
    margin: 1em auto;
    background-color: dimgray;
    padding: 1em;
}

.box10 {background-image: linear-gradient(to left, white, red);}
.box11 {background-image: linear-gradient(to right, red, green, blue);}
.box12 {background-image: linear-gradient(to top, red, white);}
.box13 {background-image: linear-gradient(to bottom, blue, red);}
.box14 {background-image: linear-gradient(to top left, green, white);}
.box15 {background-image: linear-gradient(to top right, blue, white);}
.box16 {background-image: linear-gradient(to bottom left, green, white, blue);}
.box17 {background-image: linear-gradient(to bottom right, red, white, yellow);}
```

Jika dijalankan, terlihat bahwa saya membuat beberapa gradient warna menggunakan semua keyword yang ada. Selanjutnya, saya akan mencoba-nya menggunakan sudut.

berikut contoh penerapan-nya

```html
    <!-- Linear Gradient Direction Sudut -->
<div class="linear-gradient1">
    <div class="box box18">
        <span>Box 1</span>
    </div>
    <div class="box box19">
        <span>Box 2</span>
    </div>
    <div class="box box20">
        <span>Box 3</span>
    </div>
    <div class="box box21">
        <span>Box 4</span>
    </div>
    <div class="box box22">
        <span>Box 5</span>
    </div>
    <div class="box box23">
        <span>Box 6</span>
    </div>
</div>
```

```css
.box18 {background-image: linear-gradient(45deg, red, white, blue);}
.box19 {background-image: linear-gradient(90deg, red, white, blue);}
.box20 {background-image: linear-gradient(135deg, red, white, blue);}
.box21 {background-image: linear-gradient(-45deg, red, white, blue);}
.box22 {background-image: linear-gradient(-90deg, red, white, blue);}
.box23 {background-image: linear-gradient(-135deg, red, white, blue);}
```

## Repeat Linear

Repaeat Linear Gradient berfungsi untuk menghasilkan efek lanjutan dari linear gradient. Khusus untuk repeat linear gradient, ukuran nilai warna linear gradient harus kurang dari 100% karena nilai yang mnentukan berapa kali efek gradient akan di ulang.

berikut contoh penerapan-nya

```html
<!-- Repeating Linear Gradient -->
<div class="linear-gradient1">
    <div class="box box24">Box 1</div>
    <div class="box box25">Box 2</div>
    <div class="box box26">Box 3</div>
    <div class="box box27">Box 4</div>
    <div class="box box28">Box 5</div>
</div>
```

```css
.box24 {background-image: repeating-linear-gradient(red, white 25%);}
.box25 {background-image: repeating-linear-gradient(to bottom right, red, white, red 4%);}
.box26 {background-image: repeating-linear-gradient(to left, red, white 20%);}
.box27 {background-image: repeating-linear-gradient(to top right, red, white, red 1%);}
.box28 {background-image: repeating-linear-gradient(to right, red,orange,yellow,lime,limegreen,cyan,blue,pink,magenta,purple 10%);}
```

Jika dijalankan, terlihat bahwa liniear gradient akan diulang-ulang sampai memenuhi element-nya.