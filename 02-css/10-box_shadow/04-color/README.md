# Box Shadow Color

Nilai kelima dari property `box-shadow` adalah color. Yap, memberikan warna pada `box-shadow`. Satuan warna mulai dari keyword, RGB hingga format HSL dapat dipakai pada property ini.

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
    background-color: green;
    float: left;
    margin: 1.5em;
}
.box1 {box-shadow: 10px 10px 10px 10px red;}
.box2 {box-shadow: 10px 10px 10px 10px #0000FF;}
.box3 {box-shadow: 10px 10px 10px 10px rgba(255,88,75,0.8);}
.box4 {box-shadow: 10px 10px 10px 10px hsl(50,100%,50%);}
```

Ketika dijalankan, terlihat bahwa saya membuat warna-nya mulai dari keyword hingga hsl. Warna ini biasanya digunakan agar warna dari `box-shadow` tidak monoton.