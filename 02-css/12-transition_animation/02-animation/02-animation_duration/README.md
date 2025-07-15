# Animation Duration

Property ini berfungsi untuk menentukan durasi sebuah animasi. Satuan second dan millisecond untuk mengisi durasi animation.

Dengan menggabungkan `@keyframes`,`animation-name`,`animation-duration`. Maka sebuah animasi akan tampil pada element CSS.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1">Box 1</div>
    <div class="box box2">Box 2</div>
</div>
```

```css
.container {
    background-color: dimgray;
    width: 80%;
    height: 400px;
    margin: 1em auto;
}

.box {
    width: 200px;
    height: 50px;
    margin: 2em;
    line-height: 50px;
    text-align: center;
    color: white;
}
.box1 {
    background-color: black;
}
.box1:hover {
    background-color: gray;
    animation-name: lebar;
    animation-duration: 1s;
}

@keyframes lebar {
    0% {width: 250px;}
    50% {width: 100px;}
    100% {width: 400px;}
}

.box2 {
    background-color: black;
}
.box2:hover {
    background-color: gray;
    animation-name: warna;
    animation-duration: 5s;
}

@keyframes warna {
    10% {background-color: red;}
    20% {background-color: green;}
    30% {background-color: blue;}
    40% {background-color: cyan;}
    50% {background-color: magenta;}
    60% {background-color: yellow;}
    70% {background-color: black;}
    80% {background-color: purple;}
    90% {background-color: tomato;}
    100% {background-color: lime;}
}
```

Jika dijalankan, terlihat bahwa element pertama saya buat animation nya dengan menambah lebar element secara acak dan element kedua saay buat animation nya mengubah warna secara bertahap selama 5 detik.