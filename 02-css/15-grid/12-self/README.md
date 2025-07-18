# Justify Self, Align Self, Place Self

Ketiga property adalah variasi dari property `justify-items`, `align-items`, dan `place-items` yang ditempatkan ke dalam grid item. Jadi, `justify-self`, `align-self`, dan `place-self` digunakan untuk memberikan style grid items secara individu.

Nilai ayng dapat diisi oleh ketiga property tersebut sama seperti 3 property sebelumnya, yakni `stretch`, `start`, `center`, dan `end`.

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
<div class="container">
    <div class="box justify-self-1">Box 1</div>
    <div class="box justify-self-2">Box 2</div>
    <div class="box justify-self-3">Box 3</div>
    <div class="box align-self-1">Box 4</div>
    <div class="box align-self-2">Box 5</div>
    <div class="box align-self-3">Box 6</div>
    <div class="box place-self-1">Box 7</div>
    <div class="box place-self-2">Box 8</div>
    <div class="box place-self-3">Box 9</div>
</div>
```

```css
.justify-self-1 {justify-self: start;}
.justify-self-2 {justify-self: center;}
.justify-self-3 {justify-self: end;}

.align-self-1 {align-self: start;}
.align-self-2 {align-self: center;}
.align-self-3 {align-self: end;}

.place-self-1 {place-self: start end;}
.place-self-2 {place-self: center end;}
.place-self-3 {place-self: center center;}
```
