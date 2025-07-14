# Transform Scale

Nilai dari Scale berfungsi untuk memperbesar atau memperkecil ukuran sebuah element. Nilai dari scla berupa angka tanpa satuan. Angka yang di isi berupa pecahan baik positif maupun negatif.

Efek `scale` terdiri dari 2 dimensi, yakni `scaleX` untuk sumbu X (Lebar Element) dan `scaleY` untuk sumbu Y (Tinggi Element).

Selain itu, ada penulisan shortand notation dengan menulis `scale` dengan isian berupa `scaleX` dan `scaleY`.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1">Box 1</div>
    <div class="box box2">Box 2</div>
</div>
<div class="container">
    <div class="box box3">Box 1</div>
    <div class="box box4">Box 2</div>
</div>
```

```css
.container {
    width: 80%;
    height: 200px;
    background-color: dimgray;
    margin: 1em auto;
    padding: 1em;
}
.box {
    width: 100px;
    height: 100px;
    background-color: green;
    float: left;
    margin: 2em;
    line-height: 100px;
    text-align: center;
    color: white;
}
.box1 {transform: scaleX(1.5);}
.box2 {transform: scaleY(1.5);}
.box3 {transform: scale(1.5);}
.box4 {transform: scale(2,1);}
```

Jika dijalankan, terlihat bahwa saya mencoba seluruh nilai dari `scale` mulai dari lebar dan tinggi element serta penulisan shorthand notation.

<hr>

Ketika menggunakan `scale`, saya bisa menggabungkan-nya dengan pseudo element selector `:hover` untuk menampilkan efek yang menarik ketika user mensorot element tersebut.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box5">Box 1</div>
</div>
```

```css
.box5:hover {
    transform: scale(1.5);
}
```

Jika dijalankan dan element disorot maka efek scale akan ada. Cukup menarik menggunakan scale ini untuk web interaktif kepada pengguna.