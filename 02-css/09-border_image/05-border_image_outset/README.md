# Border Image Outset

Property ini dipakai untuk memindahkan gambar border keluar daari element, yakni berada di posisi garis outset. Property `border-image-outset` butuh nilai dalam satuan length untuk berfungsi menggeser border keluar.

berikut contoh penerapan-nya

```html
<div class="box box1"></div>
```

```css
.box {
    width: 200px;
    height: 200px;
    line-height: 200px;
    text-align: center;
    color: white;
    font-size: 1.5em;
    background-color: dimgray;
    margin: 3em;
    float: left;
    border: 33px solid transparent;
    border-image-source: url('../img/border1.png');
    border-image-slice: 33;
}
.box1 {
    border-image-outset: 33px;
}
```

Jika dijalankan, terlihat bahwa gambar akan keluar element. Efek ini dapat digunakan jika sebuah gambar border ingin dikeluarkan pada element.