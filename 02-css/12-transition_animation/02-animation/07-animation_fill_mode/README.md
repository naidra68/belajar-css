# Animation Fill Mode

Property ini berfungsi untuk menentukan bagaimana style element dan sesudah animasi ditampilkan. Nilai yang dapat di isi adalah `none`, `forward`, `backward`, `both`.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1">Forward</div>
    <div class="box box2">Backward</div>
    <div class="box box3">Both</div>
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
    animation-name: warna_forward;
    animation-duration: 5s;
    animation-delay: 1s;
    animation-fill-mode: forwards;
}

@keyframes warna_forward {
    0% {background-color: red;}
    25% {background-color: green;}
    50% {background-color: blue;}
    75% {background-color: cyan;}
    100% {background-color: magenta;}
}

.box2 {
    background-color: black;
}
.box2:hover {
    background-color: gray;
    animation-name: warna_backward;
    animation-duration: 5s;
    animation-delay: 1s;
    animation-fill-mode: backwards;
}

@keyframes warna_backward {
    0% {background-color: red;}
    25% {background-color: green;}
    50% {background-color: blue;}
    75% {background-color: cyan;}
    100% {background-color: magenta;}
}
.box3 {
    background-color: black;
}
.box3:hover:hover {
    background-color: gray;
    animation-name: warna_both;
    animation-duration: 5s;
    animation-delay: 1s;
    animation-fill-mode: both;
}

@keyframes warna_both {
    0% {background-color: red;}
    25% {background-color: green;}
    50% {background-color: blue;}
    75% {background-color: cyan;}
    100% {background-color: magenta;}
}
```

Jika dijalankan, terlihat bahwa terdapat berbedaan antara `forward`,`backward`, dan `both`. Dimana masing-masing nilai ini memiliki tujuan yang berbeda.

**Forward** akan menampilkan warna background awal dari `:hover`, lalu akan masuk ke warna background keyframes dan berhenti di warna terakhir pada keyframe.

**Backward** akan menampilkan warna background keyframes langsung, lalu akan berhenti di warna `:hover`. Intinya ini kebalikan dari Forward.

**Both** akan menampilkan terlebih dahulu warna background keyframes, lalu tetap memertahankan warna background keyframe terakhir dan tidak balik ke warna background `:hover`.

Penjelasan diatas terkesan rumit dan susah untuk dipahami, namun coba lihat hasilnya dan pahami sesuai konteks-nya.