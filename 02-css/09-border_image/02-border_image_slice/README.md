# Border Image Slice

Property ini berfungsi untuk memotong gambar agar dapat disatukan menjadi `border`. Property `border-image-slice` akan membagi gambar menjadi 9 bagian. Bagian inilah yang nantinya akan dipakai sebagai border disetiap sudut sisi element.

berikut contoh penerapan-nya

```html
<div class="box box1"></div>
<div class="box box2"></div>
<div class="box box3"></div>
<div class="box box4"></div>
```

```css
.box {
    width: 200px;
    height: 200px;
    background-color: dimgray;
    margin: 1em;
    float: left;
    border: 33px solid transparent;
}
.box1 {
    border-image-source: url('../img/border1.png');
    border-image-slice: 33 33 33 33;
}
.box2 {
    border-image-source: url('../img/border1.png');
    border-image-slice: 16 33 16 33;
}
.box3 {
    border-image-source: url('../img/border2.png');
    border-image-slice: 15%;
}
.box4 {
    border-image-source: url('../img/border1.png');
    border-image-slice: 33 fill;
}
```

Ketika dijalankan, terlihat saya membuat pemotongan gambarnya berbeda-beda setiap box. Pada box1 saya memotong-nya sama sisi dari atas,bawah,kiri, dan kanan.

Untuk box2, maka pemotongan untuk sisi atas dan bawah adalah 16, sedangkan sisi kiri dan kanan adalah 33. Untuk box3 saya menggunakan percent untuk memotong-nya dan box4 saya gunakan fill untuk menampilkan potongan terakhir berada ditengah-tengah hasil potongan.

Jika dipahami, memang sedikit rumit. Pemahaman mengenai ini lebih mudah jika divisualisasikan menggunakan gambar.

