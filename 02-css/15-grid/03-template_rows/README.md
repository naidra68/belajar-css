# Grid Template Rows

Property ini digunakan untuk menentukan jumlah dan lebar baris grid. Penulisan nilai property ini sama seperti `grid-template-column`. Perpaduan antara **template-column** dan **template-rows** akan membuat sebuah sistem grid yang terdiri dari kolom dan baris.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
    <div class="box">Box 10</div>
</div>
```

```css
.container {
    background-color: aqua;
    border: 2px solid salmon;
    margin: 1rem;
    text-align: center;
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    grid-template-rows: 50px 80px;
}
.box {
    padding: 0.3rem;
    background-color: yellow;
}
.box:nth-child(even) {
    background-color: yellowgreen;
}
```

Jika dijalankan, terlihat bahwa semua child element memiliki aturan kolom `1fr 2fr 1fr` dan baris `50px 80px`. Jika digambarkan, struktur grid ini bisa menampung `3 x 2 = 6 item`. Contoh paling bagus ada pada parent element pertama, dimana baris pertama sesuai 50px dan baris kedua sesuai 80px.

Jika terdapat baris baru seperti parent element kedua maka akan tampil default dan tidak di set. Biasanya property ini jarang digunakan ketika menggunakan grid karena baris harus fleksible tergantung isi element-nya. Namun, mengatur baris juga tidak ada salahnya.