# :not Selector

Pseudo selector :not() cukup unik, berfungsi untuk mencari element HTML selain yang ditulis. Selector ini dikenal juga sebagai negation pseudo-class selector.

contoh penerapan-nya

```html
<p>Bukan Halo</p>
<p>Bukan Halo</p>
<p class="halo">Halo</p>
<p>Bukan Halo</p>
<p class="halo">Halo</p>
<p class="halo">Halo</p>
<p>Bukan Halo</p>
<p class="halo">Halo</p>
<p class="halo">Halo</p>
<p class="halo">Halo</p>
```

```css
p:not(.halo) {
    color: red;
}
```

Jika dijalankan, semua element paragraf yang tidak memiliki `class="halo"` akan di style. Seperti fungsi dari :not.

Fungsi ini sangat super power jika sudah memasuki web kompleks. Karena terkadang, saya ingin mengecualikan satu element agar tidak terkena style, maka saya bisa menggunakan `:not` ini.