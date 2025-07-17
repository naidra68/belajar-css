# Flex Direction

Property `flex-direction` digunakan untuk mengatur urutan dan posisi element yang terdapat di dalam **flex container**. Nilai yang dapat diisi adalah `row` (nilai default), `row-reverse`, `column`, dan `column-reverse`.

berikut contoh penerapan-nya

```html
<div class="container row">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container row-reverse">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container column">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container column-reverse">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
```

```css
.container {
    height: 150px;
    border: 2px solid #FF734F;
    background-color: #09A8C8;
    margin: 1em;
    display: flex;
}
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.row {
    flex-direction: row;
}
.row-reverse {
    flex-direction: row-reverse;
}
.column {
    flex-direction: column;
}
.column-reverse {
    flex-direction: column-reverse;
}
```

Jika dijalankan, terlihat bahwa saya memasukkan flex container kedalam parent element yakni class `.container`. Dengan menambahkannya ke parent element, maka saya bisa mengontrol child element-nya.

Property flex-direction ini dipakai untuk menentukan main axis (sumbu utama) dari flexbox. Nilai `row` akan mengarah pada sumbu X (horizontal) dan Nilai `column` akan mengarah pada sumbu Y (vertical).

Untuk nilai `row-reverse` sama seperti `row` dan nilai `column-reverse` sama seperti `column`, cuma dibalik saja urutan child element-nya. Arah main axis ini akan berperngaruh terhadap property flexbox lain-nya.