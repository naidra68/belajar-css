# :not Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

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

Fungsi ini sangat super power jika sudah memasuki web kompleks. Karena terkadang, saya ingin mengecualikan satu element agar tidak terkena style, maka saya bisa menggunakan :not ini.