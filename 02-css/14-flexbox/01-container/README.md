# Flex Container

Hal pertama yang harus dilakukan agar dapat menggunakan flexbox adalah menambahkan property flex didalam element parent-nya. Biasanya parent element yang diberi property flex disebut sebagai **Flex Container**. Property flex yang dimaksud adalah property `display: flex` atau `display: inline-flex`.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container flex">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container inline-flex">
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
}
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.flex {
    display: flex;
}
.inline-flex {
    display: inline-flex;
}
```

Jika dijalankan, terlihat bahwa element yang memiliki property `display: flex` akan menampilkan element box berjejer disamping sebelah kiri, hal ini sama seperti menggunakan `float: left`.

Element yang memiliki property `display: inline-flex` akan menampilkan element box berjejer disamping sebelah kiri dan juga parent element-nya menyesuaikan element box.

Simple-nya begini :

1. `flex` : block level element
2. `inline-flex` : inline level element

## Jenis-jenis Flexbox Property

Langkah selanjutnya setelah membuat parent element menjadi flex container adalah menambahkan beberapa property flexbox lain untuk mengontrol child element-nya. Property flexbox ini dipecah menjadi 1 kelompok yaitu : `flex container` dan `flex item`.

1. Flex Container :
    - flex-direction
    - flex-wrap
    - flex-flow
    - justify-content
    - align-items
    - align-content
2. Flex Item :
    - order
    - flex-grow
    - flex-shrink
    - flex-basis
    - flex

Pemahaman mengenai perbedaan antara **flex container** dan **flex item** harus dipahami agar tidak terbalik ketika menggunakan property flexbox. Semua property diatas akan saya coba satu-persatu.

Sebelum itu, agar tidak terjadi kebingungan antara maksud dari container dan item. Selanjutnya, saya ubah istilah container sebagai parent element dan item sebagai child element.