# Grid Row Start and End

Property ini digunakan untuk menggabungkan baris grid. Sama seperti property Grid Column Start and End. Hanya saja ini khusus untuk baris grid.

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
.header, .footer {
    grid-column-start: 1;
    grid-column-end: 4;
}
.main {
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 2;
    grid-row-end: 4;
}
.sidebar {
    grid-row-start: 2;
    grid-row-end: 4;
}
```

Jika dijalankan, terlihat bahwa element main akan mengambil baris ke 2 sampai ke 4 dan sidebar juga mengambil baris ke 2 sampai ke 4.