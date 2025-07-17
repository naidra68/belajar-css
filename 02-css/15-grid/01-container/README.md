# Grid Container

Untuk menggunakan grid, maka element ahurs berada di dalam grid container, seperti hal-nya dengan flexbox. Cara menambahkan suatu element masuk kedalam grid container adalah dengan cara meanmbahkan property `display: grid` atau `display: inline-grid`.

berikut contoh penerapan-nya

```html
<h1>Normal</h1>
<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
</div>
<h1>Grid</h1>
<div class="container grid">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
</div>
<h1>Inline Grid</h1>
<div class="container inline-grid">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
</div>
```

```css
.container {
    height: 150px;
    background-color: aqua;
    border: 2px solid salmon;
    margin: 1rem;
}
.box {
    padding: 0.3rem;
    margin: 0.3rem;
    background-color: yellow;
}
.box:nth-child(even) {
    background-color: yellowgreen;
}
.grid {display: grid;}
.inline-grid {display: inline-grid;}
```

Jika dijalankan, terlihat bahwa parent element yang tidak memiliki **grid container** akan terdapat space kosong. Ketika parent element diberi **grid container**, maka child element akan terlihat stretch dan memenuhi parent element.

Hal ini bisa terjadi karena child element tidak di set lebar ataupun tinggi element. Selain itu, jika menggunakan `inline-grid `maka terlihat bahwa akan menjadi inline-level element.

## Jenis-jenis Grid Property

Sama seperti flexbox, setelah membuat grid container, maka selanjutnya harus menambahkan property grid lain. Property ini dibagi menjadi 2 kelompok yaitu : **grid container** dan g**rid item**.

**Grid Container**
- `grid-template-columns`
- `grid-template-rows`
- `grid-template-areas`
- `grid-column-gap / column-gap`
- `grid-row-gap / row-gap`
- `grid-gap / gap`
- `justify-items`
- `align-items`
- `place-items`

**Grid Item**
- `grid-column-start`
- `grid-column-end`
- `grid-row-start`
- `grid-row-end`
- `grid-column`
- `grid-row`
- `grid-area`
- `justify-self`
- `align-self`
- `place-self`

Sangat banyak sekali yaaaaaa. Saya akan mencoba-nya satu persatu.