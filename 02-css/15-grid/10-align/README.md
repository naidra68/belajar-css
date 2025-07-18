# Align Items

Property ini berfungsi untuk mengatur posisi semua grid item pada sumbu y. NIlai yang dapat diisi pada property ini adalah `stretch (default)`, `start`, `center`, dan `end`.

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
<h1>Stretch</h1>
<div class="container stretch">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<h1>Start</h1>
<div class="container start">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<h1>Center</h1>
<div class="container center">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<h1>End</h1>
<div class="container end">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.stretch {align-items: stretch;}
.start {align-items: start;}
.center {align-items: center;}
.end {align-items: end;}
```

Terlihat bahwa lebar setiap grid item akan mengecil sesuai lebar konten jika terdapat property `align-items`. Ini hanya berlaku jika grid item tidak di set lebar atau tinggi-nya.