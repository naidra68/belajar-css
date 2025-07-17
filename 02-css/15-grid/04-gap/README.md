# Row-Gap, Column-Gap and Gap

Ketiga property ini digunakan untuk membuat spasi di antar baris dan kolom grid. Nilai yang dapat diisi adalah satuan length seperti `px`, `em`, `rem`, dan lain-lain.

Sesuai nama-nya, `row-gap` dipakai untuk spasi antar baris, `column-gap` dipakai untuk spasi antar kolom, dan `gap` dipakai untuk spasi antar baris dan kolom atau bisa dibilang penulisan shorthand notation dari `row-gap` dan `column-gap`.


> CSS Wajib
```css
.container {
    height: 150px;
    background-color: aqua;
    border: 2px solid salmon;
    margin: 1rem;
    text-align: center;
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
}
.box {
    background-color: yellow;
}
.box:nth-child(even) {
    background-color: yellowgreen;
}
```

## Row-Gap

berikut contoh penerapan-nya

```html
<h1>Row Gap</h1>
<div class="container row-gap">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.row-gap {row-gap: 20px;}
```
## Column-Gap

berikut contoh penerapan-nya

```html
<h1>Column Gap</h1>
<div class="container column-gap">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.column-gap {column-gap: 1.5em;}
```

## Gap

berikut contoh penerapan-nya

```html
<h1>Gap</h1>
<div class="container gap1">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<div class="container gap2">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.gap1 {gap: 1.5rem;}
.gap2 {gap: 1rem 0.5rem;}
```

