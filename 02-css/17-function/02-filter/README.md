# Filter

Filter ini adalah property bukanlah fungsi, namun saya taruh di sini karena isi dari filter semua-nya adalah fungsi. Property ini berfungsi untuk memberikan efek pada gambar agar terlihat menarik.

Nilai yang dapat diisi didalam propert ini berupa fungsi semua, berikut ini daftar fungsi yang dapat digunakan :

- `blur()`
- `brightness()`
- `drop-shadow()`
- `grayscale()`
- `hue-rotate()`
- `contrast()`
- `opacity()`
- `sepia()`
- `saturate()`
- `invert`

berikut contoh penerapan-nya

```html
<img class="blur" src="image.jpg">
<img class="brightness" src="image.jpg">
<img class="contrast" src="image.jpg">
<img class="grayscale" src="image.jpg">
<img class="invert" src="image.jpg">
<img class="opacity" src="image.jpg">
<img class="sepia" src="image.jpg">
<img class="saturate" src="image.jpg">
<img class="hue-rotate" src="image.jpg">
<img class="drop-shadow" src="image.jpg">
<img class="multiple" src="image.jpg">
```

```css
img {
    padding: 0.5rem;
}
.blur {filter: blur(3px);}
.brightness {filter: brightness(150%);}
.contrast {filter: contrast(350%);}
.grayscale {filter: grayscale(85%);}
.invert {filter: invert(100%);}
.opacity {filter: opacity(50%);}
.saturate {filter: saturate(500%);}
.hue-rotate {filter: hue-rotate(90deg);}
.drop-shadow {filter: drop-shadow(2px 2px 10px);}
.multiple {filter: drop-shadow(3px 3px red) sepia(100%) drop-shadow(-3px -3px blue);}
```

