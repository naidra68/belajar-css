# Transition Delay

Property ini berfungsi untuk membuat jead waktu sebelum efek transisi berlangsung. Nilai yang diisi adalah second dan millisecond.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1">Box 1</div>
    <div class="box box2">Box 2</div>
    <div class="box box3">Box 3</div>
    <div class="box box4">Box 4</div>
</div>
```

```css
.container {
    background-color: dimgray;
    width: 80%;
    height: 400px;
    margin: 1em auto;
    padding: 2em;
}

.box {
    width: 200px;
    height: 50px;
    line-height: 50px;
    text-align: center;
    color: white;
    margin: 1em;
    transition-duration: 1s;
    background-color: red;
}
.box1 {transition-delay: 1s;}
.box2 {transition-delay: 0.5s;}
.box3 {transition-delay: 100ms;}
.box4 {transition-delay: 2000ms;}

.box1:hover,.box2:hover,
.box3:hover,.box4:hover {
    width: 400px;
    background-color: maroon;
}
```

Jika dijalankan, terlihat bahwa setiap element akan menunggu terlebih dahulu sebelum di transisi. Waktu tunggu sesuai yang telah di definisikan.