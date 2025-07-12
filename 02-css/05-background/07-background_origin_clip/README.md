# Background Origin and Background Clip

Dua Property ini dipakai untuk menentukan dari mana gambar atau warna pada background dimulai. Entah itu dari border, dari padding, atau hanya untuk konten saja.

Perbedaan dari dua property ini? Sebelum ke code-nya, saya harus paham mengenai perbedaan dua property `background-origin` dan `background-clip`.

Sederhana-nya, `background-origin` dipakai untuk mengatur gambar background, sedangkan `background-clip` dipakai untuk mengatur warna background.

berikut contoh penerapan-nya

```html
<!-- background-clip -->
<div class="box satu">border-box</div>
<div class="box dua">padding-box</div>
<div class="box tiga">content-box</div>
<br style="clear: both;">
<!-- background-origin -->
<div class="box1 satu">border-box</div>
<div class="box1 dua">padding-box</div>
<div class="box1 tiga">content-box</div>
```

```css
.box {
    width: 100px;
    height: 100px;
    border: 6px dashed red;
    float: left;
    margin: 10px;
    padding: 0.5em;
    background-color: yellow;
    font-size: 12px;
    text-align: center;
}
.box1 {
    width: 100px;
    height: 100px;
    border: 6px dashed lime;
    float: left;
    margin: 10px;
    padding: 0.5em;
    background-image: url('../img/bluebarry100x100.png');
    font-size: 12px;
    text-align: center;
    color: white;
}

.satu {background-clip: border-box;}
.dua {background-clip: padding-box;}
.tiga {background-clip: content-box;}

.empat {background-origin: border-box;}
.lima {background-origin: padding-box;}
.enam {background-origin: content-box;}
```

Jika dijalankan, terlihat bahwa setiap isi dari property ini akan menentukan dimana gambar dan warna background akan ditempatkan.