# Grid Template Columns

Property ini digunakan untuk menentukan jumlah dan lebar kolom grid. Setelah grid ada di parent element, maka semua item akan berderet sesuai jumlah kolom yang telah didefinisikan.

Apabila jumlah grid item melebihi jumlah kolom, maka akan pindah membentuk baris baru. Hal ini seperti efek wrap pada Flexbox.

berikut contoh penerapan-nya

```html
<h1>Template 3 Column</h1>
<div class="container temp_3">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<h1>Template 3 Column</h1>
<div class="container temp_3">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
</div>
```

```css
.container {
    height: 150px;
    background-color: aqua;
    border: 2px solid salmon;
    margin: 1rem;
    text-align: center;
    display: grid;
}
.temp_3 {grid-template-columns: 100px 200px 100px;}
.box {
    padding: 0.3rem;
    background-color: yellow;
}
.box:nth-child(even) {
    background-color: yellowgreen;
}
```

Jika dijalankan, terlihat bahwa semua grid item akan menyesuaikan grid-template-nya dengan aturan `100px, 200px, 100px`. Apabila ada element melebihi dari aturan template tersebut akan pindah ke baris baru. Inilah mengapa box 7 pada parent element kedua akan membuat baris baru.

Jika aturan diganti menjadi `100px, 200px, 100px, 200px`, maka nantinya box 4 tidak akan membuat baris baru, namun berjejer seperti box 1 s/d 3.

```html
<h1>Template 4 Column</h1>
<div class="container temp_4">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.temp_4 {grid-template-columns: 100px 200px 100px 200px;}
```

Jika dijalankan, terlihat seperti yang telah dijelaskan diatas.

## Auto and fr

Selain nilai length, dapat juga diisi oleh nilai khusus untuk lebar kolom grid yaitu, **auto** dan **fr**.

Jika menggunakan nilai auto diakhir penulisan template column, maka kolom grid akan memenuhi sisa ruang yang tersisa jika ada.

berikut contoh penerapan-nya

```html
<h1>Template auto</h1>
<div class="container temp_auto">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.temp_auto {grid-template-columns: 100px 200px 100px auto;}
```

Yang paling menarik dan sering dipakai untuk grid adalah fr (singkatan dari fraction). Nilai fr dipakai untuk membagi lebar grid container dengan skala tertentu.

berikut contoh penerapan-nya

```html
<h1>Template fr</h1>
<div class="container temp_fr">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.temp_fr {grid-template-columns: 1fr 2fr 1fr;}
```

Jika dijalankan, terlihat bahwa grid template akan membagi seluruh item menjadi rata dengan perbandingan 1 : 2 : 1. Saat lebar parent element diperbesar atau diperkecil, maka skala perbandingan ini tetap dipertahankan.

## Fungsi Repeat

Fungsi ini memudahkan penulisan kolom dengan nilai yang berulang. Sebagai contoh, jika memiliki 5 box dengan template perbandingan sama besar. Alih-alih menulis seperti berikut :

> `grid-template-columns: 1fr 1fr 1fr 1fr 1fr`

Saya bisa gunakan fungsi `repeat()`, agar tidak menulis code berulang. Penulisan menggunakan fungsi `repeat()` sebagai berikut :

> `grid-template-columns: repeat(5, 1fr)`

Atau, saya bisa mengulang beberapa kolom sekaligus. Misalnya sebagai berikut :

> `grid-template-columns: repeat(3, 200px 1fr)`

berikut contoh penerapan-nya

```html
<h1>Template fr repeat()</h1>
<div class="container temp_fr_repeat">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<div class="container temp_fr_repeat1">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
</div>
```

```css
.temp_fr_repeat {grid-template-columns: repeat(5, 1fr);}
.temp_fr_repeat1 {grid-template-columns: repeat(3, 200px 1fr);}
```

## Fungsi MinMax

Untuk mengatur lebar kolom yang lebih fleksible, CSS menyediakan fungsi minmax(). Fungsi ini membutuhkan dua buah nilai input yang berguna untuk menentukan lebar kolom minimum dan maksimum.

> `grid-template-columns: minmax(200px,300px) minmax(200px,300px) minmax(200px,300px);`

Jika grid container diperkecil, maka lebar kolom tidak bisa menjadi kecil lagi dari nilai minimum tersebut dan tidak akan bisa menjadi besar lagi dari nilai maksimum tersebut.

berikut contoh penerapan-nya

```html
<h1>Fungsi MinMax</h1>
<div class="container temp_minmax">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.temp_minmax {grid-template-columns: minmax(200px, 300px) minmax(200px, 300px) minmax(200px, 300px);}
```

## auto-fill and auto-fit

Fungsi `repeat()` memiliki keyword khusus untuk emmbuat jumlah kolom dinamis, yakni **auto-fill** dan **auto-fit**. Apabila nilai pertama pada fungsi `repeat()` diisi dengan salah satu nilai tersebut, maka jumlah kolom ditentukan dari seberapa banyak yang bisa ditampung oleh grid container.

Agar lebih dinamis lagi, gabungkan fungsi `repeat()` dengan fungsi `minmax()`. Karena dengan ini, maka seluruh child element akan menyesuaikan lebar-nya.

berikut contoh penerapan-nya

```html
<h1>Auto Fill and Auto Fit</h1>
<div class="container temp_fill">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
<div class="container temp_fit">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
</div>
```

```css
.temp_fill {grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));}
.temp_fit {grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));}
```