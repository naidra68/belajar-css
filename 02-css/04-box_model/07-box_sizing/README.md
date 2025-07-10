# Box Sizing

Memahami konsep box model dapat memberikan kesimpulan bahwa dimensi total dari sebuah element dihitung dari width / height + padding + border + margin.

Untuk mengubah aturan dari perhitungan dari total box model ini dapat menggunakan sebuah property `box-sizing`. Property ini berfungsi untuk mengatur dimensi element.

Nilai dari property ini adalah `content-box` dan `border-box`.

Untuk `content-box` merupakan default dari web browser jika property `box-sizing` tidak di definisikan.

Untuk `border-box` merupakan nilai yang menggabungkan width height dengan padding, border, dan padding.

Kembali lagi ke konsep Box-Model, saat saya memberikan content dengan `width`, `height`, `border`, `padding`, `margin`. Maka semua itu akan diakumulasikan yang menjadikan `width` dan `height` bertambah.

Menggunakan nilai `border-box` akan membuat semua property `border`, `padding`, dan `margin` akan disamakan dengan width height.

berikut contoh penerapan-nya

```html
<div class="satu">Content Box</div>
<div class="dua"> Border Box</div>
```

```css
* {
    margin: 0;
    padding: 0;
}   

div {
    width: 200px;
    height: 100px;
    background-color: aqua;
    border: 5px solid black;
    padding: 20px;
    margin: 20px;
    text-align: center;

}
.satu{
    box-sizing: content-box;
}
.dua{
    box-sizing: border-box;
}
```

Jika dijalankan, maka terlihat bahwa `border-box` tetap mempertahankan nilai dari `width` dan `height`. Property ini hadir untuk mempermudah perhitungan element box model. Keunggulan inilah yang sering dipakai framework css seperti **Bootstrap**.

Terkadang, saat menemukan project orang lain. Saya perlu memastikan mengenai style yang dipakai, apalagi dengan `box-sizing` nya menggunakan `content-box` atau `border-box`. Agar nantinya dapat menyesuaikan perilaku mereka berdua. 