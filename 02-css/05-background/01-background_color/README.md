# Background Color

Property background-color dipakai untuk mengubah warna latar belakang dari element HTML. Nilai default property ini adalah transparent Berbagai nilai warna dapat digunakan untuk property ini seperti, `keyword`, `#RGB`, `rgb()`, `rgba()`, `hsl()`, dan `hsla()`.

berikut contoh penerapan-nya

```html
<div class="satu">Kotak Pertama</div>
<div class="dua">Kotak Kedua</div>
<div class="tiga">Kotak Ketiga</div>
<div class="empat">Kotak Keempat</div>
<div class="lima">Kotak Kelima</div>
<div class="enam">Kotak Keenam</div>
```

```css
div {
    width: 280px;
    height: 80px;
    line-height: 80px;
    float: left;
    margin: 10px;
    text-align: center;
    font-size: 20px;
    border: 2px solid black;
}
.satu {background-color: pink;}
.dua {background-color: #ff00ff;}
.tiga {background-color: hsl(180, 100%, 50%);}
.empat {background-color: rgb(255, 255, 0);}
.lima {background-color: rgba(255, 152, 18, 0.589);}
.enam {background-color: hsla(170, 50%, 45%, 1)}
```