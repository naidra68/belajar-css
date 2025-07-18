# Grid Template Areas and Grid Area

Property ini mempermudah cara untuk menggabungkan baris dan kolom grid. Alih-alih menggunakan nomor urut baris / kolom, saya bisa menggunakan property ini untuk mempermudah penggabungan.

Property yang dapat digunakan ada 2 yakni `grid-template-areas` dan `grid-area`. Sakti-nya menggunakan property ini, saya bisa seperti menggambar pola grid layout tanpa harus mengitung urutan baris atau kolom-nya.

> `CSS Wajib`

```css
.container {
    height: 300px;
    background-color: aqua;
    border: 2px solid salmon;
    margin: 1rem;
    text-align: center;
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    grid-template-rows: repeat(4, 50px);
    gap: 0.2rem;
}
.box {
    background-color: yellow;
}
.box:nth-child(even) {
    background-color: yellowgreen;
}
```

Agar property ini dapat digunakan, saya akan membuat nama grid area untuk setiap item seperti header, main, sidebar, dan footer.

```css
.header {grid-area: header;}
.main {grid-area: main;}
.sidebar {grid-area: sidebar;}
.footer {grid-area: footer;}
```

Setelah me-label setiap element dengan `grid-area`. Maka, saya bisa gunakan `grid-template-areas` dibagian class container untuk merangkai pola gambar grid-nya.

Namun, saya tidak akan tambahkan pada class container, melainkan membuat class baru agar lebih mudah dilihat saja.

berikut contoh penerapan-nya

```html
<div class="container grid-template-areas">
    <div class="box header"> Header </div>
    <div class="box main"> Main </div>
    <div class="box sidebar"> Sidebar </div>
    <div class="box footer"> Footer </div>
</div>
```

```css
.grid-template-areas {
    grid-template-areas:
    " header header header "
    " main main sidebar "
    " main main sidebar "
    " footer footer footer ";
}
```

Pahami sejenak isi dari property tersebut, code ini jika dijalankan, terlihat bahwa hasilnya sama seperti contoh-contoh sebelumnya.

Dengan menggunakan property ini, tidak perlu lagi menghitung seperti itu, yang penting paham mengenai template areas. Selanjutnya, bagaimana jika salah satu template diatas dikosongin seperti `" footer footer footer "` menjadi ` " footer foooter" `.

Hal seperti itu bisa dilakukan, namun dengan menambahkan karakter titik pada isi dari template area-nya.

berikut contoh penerapan-nya

```html
<div class="container grid-template-areas1">
    <div class="box header"> Header </div>
    <div class="box main"> Main </div>
    <div class="box sidebar"> Sidebar </div>
    <div class="box footer"> Footer </div>
</div>
```

```css
.grid-template-areas1 {
    grid-template-areas:
    " ... header ... "
    " main main sidebar "
    " main main ... "
    " ... footer footer ";
}
```
