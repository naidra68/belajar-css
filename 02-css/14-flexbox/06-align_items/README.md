# Align Items

Property ini digunakan untuk emngatur posisi child element pada cross axis, ini adalah sumbu yang berseberangan dengan sumbu utama yaitu main axis.

Begini penjelasan simple-nya.

Kalau parent element menggunakan direction row (sumbu x | horizontal) dan align-items ditambahkan disitu, maka child element akan diatur posisi-nya menjadi column (sumbu y | vertical).

Kalau parent element menggunakan direction column (sumbu y | vertical) dan align items ditambahkan disitu, maka child element akan diatur posisi-nya menjadi row (sumbu x | horizontal).

Property ini memiliki 5 nilai yang dapat diisi diantara-nya :

1. `stretch` : default jika `align-items` tidak didefinisikan.
2. `flex-start` : child element berada dibagian awal (sisi atas).
3. `center` : child element berada dibagian tengah (sisi tengah).
4. `flex-end` : child element berada dibagian akhir (sisi bawah).
5. `baseline` : child element berdasarkan font size.

berikut contoh penerapan-nya

```html
<h1>Row</h1>
<div class="container row stretch">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container row start">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container row center">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container row end">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container row baseline">
    <div class="box f18">Box 1</div>
    <div class="box f22">Box 2</div>
    <div class="box f26">Box 3</div>
</div>
<hr>
<h1>Column</h1>
<div class="container column stretch">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container column start">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container column center">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container column end">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container column baseline">
    <div class="box f18">Box 1</div>
    <div class="box f22">Box 2</div>
    <div class="box f26">Box 3</div>
</div>
```

```css
.container {
    height: 200px;
    border: 2px solid #FF734F;
    background-color: #09A8C8;
    margin: 1em;
    display: flex;
}
.row {flex-direction: row;}
.column {flex-direction: column;}

.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.stretch {align-items: stretch;}
.start {align-items: flex-start;}
.center {align-items: center;}
.end {align-items: flex-end;}
.baseline {align-items: baseline;}

.f18 {height: 30px; line-height: 30px; font-size: 18px;}
.f22 {height: 40px; line-height: 40px; font-size: 22px;}
.f26 {height: 50px; line-height: 50px; font-size: 26px;}
```

Saya akan memahami sejenak mengenai kode diatas. Setelah saya lihat hasilnya, terlihat bahwa posisinya akan berubah jika menggunakan align-items.

Setelah melihat perbedaan antara `justify-content` dan `align-items`. Saya menemukan kesimpulan bahwa `flex-direction` sangat penting untuk mengetahui bagaimana 2 property ini akan dijalankan.