# Background Blend Mode

Property ini berfungsi untuk mendapatkan gabungan dari gambar background dan warna background. Nilai yang dapat di isi pada property ini adalah keyword dengan 16 jenis keyword.

- normal
- multiply
- overlay
- screen
- darken
- lighten
- color-dodge
- color-burn
- hard-light
- soft-light
- difference
- exclusion
- hue
- saturation
- color
- luminosity

berikut contoh penerapan-nya

```html
<div class="satu"><p>Normal</p></div>
<div class="dua"><p>Multiply</p></div>
<div class="tiga"><p>Overlay</p><</div>
<div class="empat"><p>Screen</p><</div>
<div class="lima"><p>Darken</p><</div>
<div class="enam"><p>Lighten</p><</div>
<div class="tujuh"><p>Color-Dodge</p><</div>
<div class="delapan"><p>Color-Burn</p><</div>
<div class="sembilan"><p>Hard-Light</p><</div>
<div class="sepuluh"><p>Soft-Light</p><</div>
<div class="sebelas"><p>Difference</p><</div>
<div class="duabelas"><p>Exclusion</p><</div>
<div class="tigabelas"><p>Hue</p><</div>
<div class="empatbelas"><p>Saturation</p><</div>
<div class="limabelas"><p>Color</p><</div>
<div class="enambelas"><p>Luminosity</p><</div>
```

```css
div {
    width: 200px;
    height: 200px;
    border: 3px solid black;
    float: left;
    margin: 0.5em;
    background-image: url('../img/wallpaper.png');
    background-repeat: no-repeat;
    background-color: green;
    background-size: cover;
}
p {
    line-height: 200px;
    text-align: center;
    color: white;
}

.satu {background-blend-mode: normal;}
.dua {background-blend-mode: multiply;}
.tiga {background-blend-mode: overlay;}
.empat {background-blend-mode: screen;}
.lima {background-blend-mode: darken;}
.enam {background-blend-mode: lighten;}
.tujuh {background-blend-mode: color-dodge;}
.delapan {background-blend-mode: color-burn;}
.sembilan {background-blend-mode: hard-light;}
.sepuluh {background-blend-mode: soft-light;}
.sebelas {background-blend-mode: difference;}
.duabelas {background-blend-mode: exclusion;}
.tigabelas {background-blend-mode: hue;}
.empatbelas {background-blend-mode: saturation;}
.limabelas {background-blend-mode: color;}
.enambelas {background-blend-mode: luminosity;}
```

Ketika dijalankan, akan terlihat perbedaan beberapa gambar jika di isi oleh property `background-blend-mode`.