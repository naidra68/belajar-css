# Transition Duration

Property ini berfungsi untuk menentukan durasi efek transisi. Nilai yang bisa diisi adalah angka dalam satuan s (second) atau ms (millisecond).

Dengan menggabungkan `transition-property` dan `transition-duration`, maka efek transisi akan terlihat lebih jelas dan halus. Saya akan mencoba menggunakan-nya dengan code sebelum-nya

```html
<div class="container">
    <div class="box box1">Box 1</div>
    <div class="box box2">Box 2</div>
    <div class="box box3">Box 3</div>
    <div class="box box4">Box 4</div>
</div>
```

```css
.box {
    width: 200px;
    height: 50px;
    float: left;
    margin: 2em;
    line-height: 50px;
    text-align: center;
    color: white;
}
.box1 {
    background-color: red;
    transition-property: background-color;
    transition: 1s;
}
.box1:hover {
    background-color: blue;
}
.box2 {
    background-color: green;
    transition-property: background-color;
    transition: 500ms;
}
.box2:hover {
    background-color: lime;
}
.box3 {
    background-color: orange;
    transition-property: background-color;
    transition: 500ms;
}
.box3:hover {
    height: 200px;
    background-color: yellow;
}
.box4 {
    color: white;
    background-color: blue;
    transition-property: all;
    transition: 500ms;
}
.box4:hover {
    transform: scale();
    color: black;
    background-color: cyan;
}
```

Jika dijalankan, terlihat bahwa semua element akan menampilkan transisi bergantian warna ataupun ukuran secara halus. Efek ini biasanya dipakai untuk transisi tombol link agar enak dilihat.

<hr>

## navbar sederhana

Sekarang, saya akan mencoba membuat sebuah navbar sederhana menggunakan pengetahuan css sebelumnya dan penambahan efek transisi agar lebih halus pergantian warna-nya.

berikut contoh penerapan-nya

```html
<div class="container">
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Project</a></li>
        <li><a href="#">About</a></li>
    </ul>
</div>
```

```css
ul {
    background-color: red;
    float: left;
    width: 100%;
    padding: 1em;
}
ul li {
    list-style: none;
    padding: 0;
    margin: 0;
    float: left;
}
ul li a {
    color: white;
    text-decoration: none;
    background-color: red;
    padding: 1em;
    transition-property: all;
    transition-duration: 250ms;
}
ul li a:hover {
    background-color: maroon;
}
```

