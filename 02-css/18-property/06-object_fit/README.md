# Object Fit

Property ini digunakan untuk mengatur bagaimana ketika sebuah gambar dipaksa mengecil. Nilai yang bisa di isi adalah `fill`, `contain`, `cover`, `none`, dan `scale-down`.

berikut contoh penerapan-nya

```html
<img src="photo02.jpg">
<img class="crop fill" src="photo02.jpg">
<img class="crop contain" src="photo02.jpg">
<img class="crop cover" src="photo02.jpg">
<img class="crop none" src="photo02.jpg">
<img class="crop scale-down" src="photo02.jpg">
```

```css
img {
    margin-left: 10px;
    border: 2px solid;
    padding: 0.2rem;
    background-color: yellow;
}
.crop {
    width: 100px;
    height: 200px;
}
.fill {object-fit: fill;}
.contain {object-fit: contain;}
.cover {object-fit: cover;}
.none {object-fit: none;}
.scale-down {object-fit: scale-down;}
```