# Z-Index

Property ini berfungsi untuk mengatur pertumpukan sebuah element. Ketika saya ingin agar sebuah element ditumpuk secara teratur sesuai keinginan saya, maka menggunakan property ini adalah solusi yang tepat.

Property `z-index` harus disandingkan dengan property `position: relative` sebagai acuan posisi parent element-nya agar pengaturan-nya tidak merujuk ke jendela web browser dan property `position: absolute` sebagai pengatur posisi child element-nya.

```html
<div class="container">
    <div class="box box1"></div>
    <div class="box box2"></div>
    <div class="box box3"></div>
</div>
```

```css
.container {
    width: 80%;
    height: 500px;
    background-color: dimgray;
    margin: 1em auto;
    position: relative;
}
.box {
    width: 100px;
    height: 100px;
    position: absolute;
}
.box1 {
    top: 30px;
    left: 30px;
    /* z-index: 3; */
    background-color: cyan;
}
.box2 {
    top: 80px;
    left: 80px;
    /* z-index: 2; */
    background-color: yellow;
}
.box3 {
    top: 130px;
    left: 130px;
    /* z-index: 1; */
    background-color: magenta;
}
```

Jika dijalankan, terlihat bahwa element box 2 akan menimpa element box 1 dan element box 3 akan menimpa element box 2. Pada code tersebut saya comment terlebih dahulu `z-index` agar tidak ada efek-nya.

Apabila `z-index` saya aktifkan, terlihat bahwa element box 1 yang menimpa elment box 2 bukan sebaliknya. Ini terjadi karena saya definisikan box 1 isi dari `z-index` lebih besar daripada box 2.

berikut code css dengan z-index

```css
.box1 {
    top: 30px;
    left: 30px;
    z-index: 3;
    background-color: cyan;
}
.box2 {
    top: 80px;
    left: 80px;
    z-index: 2;
    background-color: yellow;
}
.box3 {
    top: 130px;
    left: 130px;
    z-index: 1;
    background-color: magenta;
}
```

Property ini bisanya digunakan untuk membuat element seperti tumpukan card. Dengan `z-index` maka element tersebut bisa dibuat.

