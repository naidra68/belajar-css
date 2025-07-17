# Grid Column and Row

Property ini merupakan penulisan singkat dari property `grid-column-start, grid-column-end` dan `grid-row-start, grid-row-end`.

Untuk nilai yang diisi pada property ini terdapat dua nilai yaitu awal dan akhir, pembeda untuk nilai awal dan akhir menggunakan slash `/`.

Sekarang saya akan mencoba membuat layout seperti sebelum-nya namun dengan property singkat ini agar lebih ringkas.


> **CSS Wajib**

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

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box header"> Header </div>
    <div class="box main"> Main </div>
    <div class="box sidebar"> Sidebar </div>
    <div class="box footer"> Footer </div>
</div>
```

```css
.header, .footer {grid-column: 1 / 4;}
.main {
    grid-column: 1 / 3;
    grid-row: 2 / 4;
}
.sidebar {grid-row: 2 / 4;}
```

Jika dijalankan, hasilnya sama seperti contoh sebelumnya. Dengan menggunakan property singkat ini akan membuat kodingan lebih rapi.