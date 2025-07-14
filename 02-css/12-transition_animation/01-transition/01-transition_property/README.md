# Transition Property

Property ini berfungsi untuk membuat apa saja property yang mendaoat efek transisi. Nilai yang digunakan adalah all, none atau nama property dipisah dengan koma.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1">Box 1</div>
</div>
```

```css
.box {
    width: 200px;
    height: 50px;
    float: left;
    margin: 2em;
    line-height: 50px;
    text-align: center;
    color: white;
}
.box1 {
    background-color: red;
    transition-property: background-color;
}
.box1:hover {
    background-color: blue;
}
```

Jika dijalankan, maka efek transisi akan berlaku pada property `background-color` saja. Ketika dicoba, terlihat tidak ada efek sama sekali, karena saya belum menambahkan durasi pada transisi-nya.

Penambahan durasi dapat menggunakan property `transition` lain-nya setelah saya mendefinisikan `transition-property`. Apabila ingin tidak hanya perubahan pada `background-color` saja maka bisa menggunakan `all` untuk memilih semua property.