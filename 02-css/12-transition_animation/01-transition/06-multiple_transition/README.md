# Multiple Transition

CSS mendukung pemisahan setiap isi dari property transition agar berjalan pada waktu yang berbeda-beda.

Sebagai contoh, jika ingin membuat ttransisi background berjalan 1 detik, transisi width 5 detik, dan transisi color 10 detik. Maka penulisan-nya dipisahkan dengan tanda koma `,`.

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
.box1 {transition: all 1s ease-out 250ms;}
.box2 {transition: width 1s, background-color 10s;}
.box3 {transition: width 1s, background-color 5s, color 10s;}
.box4 {transition: width 100ms 1s, backgroun-color 1s 3s, color 100ms 5s;}

.box1:hover,.box2:hover,
.box3:hover,.box4:hover {
    width: 400px;
    background-color: maroon;
    color: black;
}
```

Jika dijalankan, terlihat bahwa setiap box element akan menghasilkan transisi yang berbeda dan unik karena saya membuatnya seperti memiliki transisi banyak pada satu box element.