# Color

Warna merupakan aspek terpenting dalam membuat web modern saat ini. Maka dari itu, CSS menghadirkan property color untuk keperluan ini.

Property color digunakan untuk mengubah warna font pada document HTML. Selain color, terdapat pula background color yang digunakan untuk mengubah warna latar belakang font.

contoh penggunaan

```html
<h1>Belajar CSS</h1>
<p>Paragraf pertama</p>
```

```css
h1, p {
    color: white;
    background-color: red;
}
```

## Satuan Color CSS

CSS memiliki setidaknya 4 notasi penulisan warna, diantara-nya :

- keyword
- #RRGGBB / #RGB
- rgb(rr, gg, bb) / rgba(rr, gg, bb, aa)
- hsl(hh, ss, ll) / hsla(hh, ss, ll, aa)

### Keyword

sejak tadi, ketika saya mengisi property color selalu menggunakan tulisan warna dalam bahasa inggris. Inilah yang disebut sebagai keyword.

Saat ini ada ratusan lebih keyword yang bisa ditulis di CSS untuk mendefinisikan warna. Pada teks editor VS Code yang menggunakan fitur emmet, maka bisa dilihat bahwa terdapat banyak keyword color yang bisa digunakan.

berikut contoh penerapan-nya

```html
<p class="magenta">Warna Magenta</p>
<p class="cyan">Warna Cyan</p>
<p class="tomato">Warna Tomato</p>
<p class="darkblue">Warna Darkblue</p>
<p class="firebrick">Warna Firebrick</p>
<p class="chocolate">Warna Chocolate</p>
```

```css
.magenta {color: magenta;}
.cyan {color:cyan;}
.tomato {color:tomato;}
.darkblue {color:darkblue;}
.firebrick {color:firebrick;}
.chocolate {color:chocolate;}
```


### #RRGGBB / #RGB

**RGB** adalah singkatan dari Red Green Blue (merah hijau biru). Dalam desain media visual seperti televisi atau komputer, model warna inilah yang umumnya dipakai. Seluruh warna lain dihasilkan dari perpaduan ketiga warna dasar RGB.

Format #RRGGBB adalah cara penulisan warna RGB dimana RR
mewakili warna merah (red), GG mewakili warna hijau (green), dan BB mewakili warna biru (blue). Masing masing warna ini memiliki 256 tingkat kepekatan yang diwakili oleh angka 0 hingga 255.

berikut contoh penerapan-nya

```html
<p class="satu">#FFFFFF = Putih</p>
<p class="dua">#FF0000 = Merah</p>
<p class="tiga">#00FF00 = Hijau</p>
<p class="empat">#FFFF00 = Kuning</p>
<p class="lima">#0000FF = Biru</p>
```

```css
.satu{color: #FFFFFF;}
.dua{color: #FF0000;}
.tiga{color: #00FF00;}
.empat{color: #FFFF00;}
.lima{color: #0000FF;}
```

Tulisan bisa disingkat menjadi 3 kata, jika terdapat kode warna yang berulang seperti `#112233` bisa ditulis `#123`. Kode warna tersebut memberikan hasil yang sama.

Apabila kode warna tidak berulang, maka tidak bisa menggunakan penyingkatan seperti itu.


### rgb(rr, gg, bb) / rgba(rr, gg, bb, aa)

Format warna rgb(rr, gg, bb) dan rgba(rr, gg, bb, aa) sebenarnya hampir sama dengan format #RRGGBB, cuma kali ini saya tidak harus menggunakan angka heksadesimal.

berikut contoh penerapan-nya

```html
<p class="rgb1">rgb(255,255,255) = Putih</p>
<p class="rgb2">rgb(255,0,0) = Merah</p>
<p class="rgb3">rgb(0, 255, 0) = Hijau</p>
<p class="rgb4">rgb(255, 255, 0) = Kuning</p>
<p class="rgb5">rgb(0, 0, 255) - Biru</p>
```

```css
.rgb1 {color: rgb(255, 255, 255);}
.rgb2 {color: rgb(255, 0, 0);}
.rgb3 {color: rgb(0, 255, 0);}
.rgb4 {color: rgb(255, 255, 0);}
.rgb5 {color: rgb(0, 0, 255);}
```

Saat dijalankan, hasilnya sama seperti menggunakan `#RRGGBB`. 

Selain `rgb()`, ada `rgba()` untuk membuat warna dengan alpha channel. Alpha channel merupakan teknik untuk memberikan efek blur pada warna tersebut, bisa dikatakan sebagai transparansi.

berikut contoh penerapan-nya

```html
<p class="rgba1">rgba(255,0,0,1) = Merah (1)</p>
<p class="rgba2">rgba(255,0,0,0.8) = Merah (0.8)</p>
<p class="rgba3">rgba(255,0,0,0.6) = Merah (0.6)</p>
<p class="rgba4">rgba(255,0,0,0.4) = Merah (0.4)</p>
<p class="rgba5">rgba(255,0,0,0.2) - Merah (0.2)</p>
```

```css
.rgba1 {color: rgba(255,0,0,1);}
.rgba2 {color: rgba(255,0,0,0.8);}
.rgba3 {color: rgba(255,0,0,0.6);}
.rgba4 {color: rgba(255,0,0,0.4);}
.rgba5 {color: rgba(255,0,0,0.2);}
```


### hsl(hh, ss, ll) / hsla(hh, ss, ll, aa)

Format penulisan warna ini terbaru diluncurkan pada CSS3. Bisa dibilang ini dibuat agar pemilihan warna lebih fleksible daripada `rgb()` maupun `rgba()` dan lebih mudah digunakan.

**HSL** merupakan singkatan dari Hue, Saturation dan Lightness (atau kadang disebut juga dengan Luminance). HSL menggunakan konsep 'mencari warna' menggunakan color wheel.

```html
<p class="hsl1">hsl(360,0%,100%) = Putih</p>
<p class="hsl2">hsl(0,100%,50%) = Merah</p>
<p class="hsl3">hsl(0, 255, 0) = Hijau</p>
<p class="hsl4">hsl(67, 100%, 50%) = Kuning</p>
<p class="hsl5">hsl(0, 0, 255) - Biru</p>
```

```css
.hsl1 {color: hsl(360,0%,100%);}
.hsl2 {color: hsl(0,100%,50%);}
.hsl3 {color: hsl(120,100%,25%);}
.hsl4 {color: hsl(67, 100%, 50%);}
.hsl5 {color: hsl(240,100%,50%);}
```

`hsla()` sama seperti `rgba()` dimana ada alpha channel untuk mengatur transparansi.

berikut contoh penerapan-nya

```html
<p class="hsla1">hsla(0,100%,50%,1) = Merah (1)</p>
<p class="hsla2">hsla(0,100%,50%,0.8) = Merah (0.8)</p>
<p class="hsla3">hsla(0,100%,50%,0.6) = Merah (0.6)</p>
<p class="hsla4">hsla(0,100%,50%,0.4) = Merah (0.4)</p>
<p class="hsla5">hsla(0,100%,50%,0.2) - Merah (0.2)</p>
```

```css
.hsla1 {color: hsla(0,100%,50%,1);}
.hsla2 {color: hsla(0,100%,50%,0.8);}
.hsla3 {color: hsla(0,100%,50%,0.6);}
.hsla4 {color: hsla(0,100%,50%,0.4);}
.hsla5 {color: hsla(0,100%,50%,0.2);}
```