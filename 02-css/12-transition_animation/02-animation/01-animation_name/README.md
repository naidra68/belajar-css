# Animation Name

Property ini berfungsi untuk menghubungkan keyframe dengan CSS selector. Ketika saya melihat setelah definisi keyframes ada sebuah tulisan seperti `lebar` atau `warna`.Penulisan itu yang nantinya akan ditulis didalam property `animation-name`.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1">Box 1</div>
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
    float: left;
    margin: 2em;
    line-height: 50px;
    text-align: center;
    color: white;
}
.box1 {
    background-color: red;
}
.box1:hover {
    background-color: blue;
    animation-name: lebar;
}

@keyframes lebar {
    0% {
        width: 250px;
    }
    100% {
        width: 400px;
    }
}
```

Jika dijalankan, tidak terlihat apa-apa karena saya belum menambahkan property durasi pada animation. Sama seperti `transition`, saya harus mendefinisikan durasi agar dapat dijalankan.