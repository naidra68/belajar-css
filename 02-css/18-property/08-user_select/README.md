# User Select

Property ini berfungsi untuk mengatur cara user men-seleksi konten yang ada di dalam sebuah element. Nilai yang bisa diisi antara lain: `auto` (default), `text`, `all` dan `none`. 

berikut contoh penerapan-nya

```html
<p class="auto">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Enim, rerum corporis. Quo fugiat modi, dolores minus incidunt numquam ex alias, iste, id expedita mollitia. Ipsum soluta nesciunt ex? Magnam, rem?</p>
<p class="text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Enim, rerum corporis. Quo fugiat modi, dolores minus incidunt numquam ex alias, iste, id expedita mollitia. Ipsum soluta nesciunt ex? Magnam, rem?</p>
<p class="all">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Enim, rerum corporis. Quo fugiat modi, dolores minus incidunt numquam ex alias, iste, id expedita mollitia. Ipsum soluta nesciunt ex? Magnam, rem?</p>
<p class="none">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Enim, rerum corporis. Quo fugiat modi, dolores minus incidunt numquam ex alias, iste, id expedita mollitia. Ipsum soluta nesciunt ex? Magnam, rem?</p>
```

```css
p {
    border: 2px solid;
    padding: 0.5rem;
}
.auto {user-select: auto;}
.all {user-select: all;}
.text {user-select: text;}
.none {user-select: none;}
```