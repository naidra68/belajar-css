# Fungsi Calc()

Fungsi ini digunakan untuk melakukan perhitungan nilai dari isi property, perhitungan tersebut ditulis sebagai argumen, argumen yang dimaksud itu adalah simbol `()`.

Operasi pada fungsi `calc()` ini mendukung `+`,`-`,`*`,`/`. Selain operasi, saya dapat menggabungkan berbagai nilai satuan.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box1 h-100"></div>
    <div class="box2 h-100"></div>
    <div class="box3 h-100"></div>
    <div class="box4 h-100"></div>
</div>
```

```css
.container {
    width: 90%;
    height: 400px;
    margin: 1rem auto;
    background-color: red;
    padding: 0.5rem;
}

.h-100 {height: 100px;}

.box1 {
    width: calc(10px + 100px);
    background-color: aqua;
}
.box2 {
    width: calc(100% - 30px);
    background-color: lime;
}
.box3 {
    width: calc(2em * 5);
    background-color: magenta;
}
```

