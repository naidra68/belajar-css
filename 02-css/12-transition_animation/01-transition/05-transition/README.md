# Transition

Selain menggunakan property transition satu-persatu, saya bisa langsung gunakan penulisan shorthand notation untuk menyederhanakan. Format penulisan-nya adalah sebagai berikut:

> transition: property duration timing-function delay;

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
.box2 {transition: width 1.5s linear 100ms;}
.box3 {transition: background-color 0.5s ease-in-out 1000ms;}
.box4 {transition: none 2s ease-out 250ms;}

.box1:hover,.box2:hover,
.box3:hover,.box4:hover {
    width: 400px;
    background-color: maroon;
}
```

Jika dijalankan, terlihat bahwa setiap element memiliki property transition masing-masing, dengan penulisan shorthand notation ini lebih ringkas, asal mengerti urutan isi penulisan-nya.