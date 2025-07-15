# Animation Iteration Count

Property ini berfungsi untuk mengulang animasi beberapa kali. Tidak seperti transisi yang hanya berjalan sekali. Nilai yang bisa diisi adalah angka yang menentukan berapa kali animasi terjadi.

Selain menggunakan angka, jika saya ingin animasi tidak berhenti-henti atau berjalan terus, dapat menggunakan keyword `infinite`.

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
    animation-timing-function: ease;
    animation-delay: 1s;
    animation-iteration-count: 5;
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
    animation-timing-function: ease-in-out;
    animation-delay: 2s;
    animation-iteration-count: infinite;
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

Jika dijalankan, terlihat bahwa element pertama akan mengulang sebanyak 5x sedangkan element kedua akan mengulang animasi-nya sebanyak tidak terhingga atau selama-nya.