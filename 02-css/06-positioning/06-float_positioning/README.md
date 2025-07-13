# Float Positioning

Sebelum era **Flexbox** dan **Grid**. Untuk membuat layout sebuah website biasanya menggunakan teknik float positioning. Dimana setiap posisi layout akan diatur menggunakan property `float`.

Biasanya website yang masih menggunakan `float` untuk layouting web nya adalah web lama atau web tua. Namun ada juga developers atau programmer yang menggunakan `float` karena biasanya sudah terlalu nyaman.

```html
<div class="container">
    <div class="box box1">Box 1</div>
    <div class="box box2">Box 2</div>
    <div class="box box3">Box 3</div>
</div>
<div class="container">
    <div class="box box4">Box 4</div>
    <div class="box box5">Box 5</div>
    <div class="box box6">Box 6</div>
</div>
<div class="container">
    <div class="box box7">Box 7</div>
    <div class="box box8">Box 8</div>
    <div class="box box9">Box 9</div>
</div>
```

```css
.container {
    width: 80%;
    background-color: dimgray;
    margin: 1em auto;
}
.box {
    height: 200px;
    line-height: 200px;
    text-align: center;
    color: white;
    float: left;
    font-size: 1.5em;
}
.box1 {
    width: 25%;
    background-color: red;
}
.box2 {
    width: 50%;
    background-color: green;
}
.box3 {
    width: 25%;
    background-color: blue;
}
.box4 {
    width: 25%;
    background-color: cyan;
}
.box5 {
    width: 25%;
    background-color: yellow;
}
.box6 {
    width: 50%;
    background-color: magenta;
}
.box7 {
    width: 25%;
    background-color: purple;
    float: right;
}
.box8 {
    width: 50%;
    background-color: orangered;
    float: right;
}
.box9 {
    width: 25%;
    background-color: saddlebrown;
}
```

Ketika dijalankan, terlihat bahwa saya membuat layout web sederhana untuk mengatur antar element.