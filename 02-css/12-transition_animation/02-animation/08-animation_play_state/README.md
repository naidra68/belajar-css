# Animation Play State

Property ini berfungsi untuk mengontrol jalan-nya animasi, biasanya untuk mengontrol jalan animasi menggunakan javascript. Namun, saat ini dengan CSS hal tersebut dapat dilakukan.

Property `animation-play-state` dapat diisi dengan keyword `running` atau `paused`. Sesuai nama-nya, jika memakai `running` maka dia akan berjalan dan jika memakai `paused` dia akan berhenti.


berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1">Click Me</div>
</div>
```

```css
.container {
    background-color: dimgray;
    width: 80%;
    height: 400px;
    margin: 1em auto;
    position: relative;
}

.box {
    width: 100px;
    height: 100px;
    line-height: 100px;
    text-align: center;
    color: white;
    background-color: red;
    position: absolute;
}
.box1 {
    animation-name: move;
    animation-duration: 10s;
    animation-iteration-count: infinite;
}
.box1:hover {
    animation-play-state: paused;
    background-color: black;
}

@keyframes move {
    0% {top: 0; left: 0;}
    25% {top: 0; left: 445px;}
    50% {top: 300px; left: 445px;}
    75% {top: 300px; left: 0;}
    100% {top: 0; left: 0;}
}
```

Jika dijalankan, terlihat bahwa Box akan memiliki animasi pindah secara terus-menerus tanpa henti, ketika saya sorot box tersebut, maka dia akan berhenti karena saya pakai `animation-play-state: paused;` untuk stop pergerakan-nya. Apabila saya tidak sorot box-nya maka dia akan lanjut lagi.

Efek ini sangat bagus digunakan ketika ingin membuat sebuah animasi dari element yang nantinya akan berhenti ketika user ingin pencet element tersebut atau hanya sekedar mensorot-nya.