# Flex Grow

Property ini berfungsi untuk menentukan skala pembesaran pada **child element (flex item)**. Property ini akan berfungsi apabila parent element memiliki lebar atau tinggi. Nilai yang dapat diisi oleh property ini adalah angka tanpa satuan seperti 1,2,3, dst.

Satu hal yang menarik dari `flex-grow` ini apabila **child element (flex item)** memiliki lebar element masing-masing 200px dan di salah satu element tersebut menggunakan property `flex-grow`. Maka, jika ada sisa ruang pada **parent element (flex container)** akan di isi oleh child element yang memiliki `flex-grow` tadi.

berikut contoh penerapan-nya

```html
<h1>Row</h1>
<div class="container h-100 row">
    <div class="box w-200">Box 1</div>
    <div class="box w-200">Box 2</div>
    <div class="box w-200 fg-1">Box 3</div>
</div>
<div class="container h-100 row">
    <div class="box w-200">Box 1</div>
    <div class="box w-200 fg-1">Box 2</div>
    <div class="box w-200 fg-2">Box 3</div>
</div>
<h1>Column</h1>
<div class="container h-600 column">
    <div class="box h-100">Box 1</div>
    <div class="box h-100">Box 2</div>
    <div class="box h-100 fg-1">Box 3</div>
</div>
<div class="container h-600 column">
    <div class="box h-100">Box 1</div>
    <div class="box h-100 fg-1">Box 2</div>
    <div class="box h-100 fg-2">Box 3</div>
</div>
```

```css
.container {
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

.row {flex-direction: row;}
.column {flex-direction: column;}

.w-200 {width: 200px;}
.h-100 {height: 100px;}
.h-600 {height: 600px;}

.fg-1 {flex-grow: 1;}
.fg-2 {flex-grow: 2;}
```

Jika dijalankan, terlihat bahwa element yang memiliki `flex-grow` akan mengambil sisa ruang yang ada di parent element, jika ingin melihat perbedaan-nya. Silahkan hilangkan `flex-grow` dan lihat hasil-nya.