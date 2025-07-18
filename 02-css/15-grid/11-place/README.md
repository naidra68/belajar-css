# Place Items

Property ini merupakan penulisan singkat shorthand notation dari dua property yakni `justify-items` dan `align-items`. Nilai pertama yang diisi adalah untuk `justify-items` dan nilai kedua yang diisi adalah untuk `align-items`.

> `place-items: justify-items align-items`

Jika terdapat satu nilai pada property `place-items`, maka nilai tersebut akan dipakai oleh dua property sekaligus.

> **CSS Wajib**

```css
.container {
    height: 300px;
    background-color: aqua;
    border: 2px solid salmon;
    margin: 1rem;
    text-align: center;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}
.box {
    background-color: yellow;
}
.box:nth-child(even) {
    background-color: yellowgreen;
}
```

berikut contoh penerapan-nya

```html
<div class="container place1">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<div class="container place2">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.place1 {place-items: start end;}
.place2 {place-items: center center;}
```