# :link Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

:link Selector digunakan untuk mencari seluruh link di dalam HTML. Fungsi ini mirip dengan element selector `a` untuk mencari tag `<a>`. Namun perlu diperhatikan bahwa tidak semua tag `<a>` adalah sebuah link.

berikut contoh penerapan-nya.

```html
<ul>
    <li><a href="https://github.com/naidra68/belajar-html">Belajar HTML</a></li>
    <li><a href="https://github.com/naidra68/belajar-css">Belajar CSS</a></li>
    <li><a href="https://github.com/naidra68/belajar-javascript">Belajar Javascript</a></li>
    <li><a href="https://github.com/naidra68/belajar-php">Belajar PHP</a></li>
    <li><a href="https://github.com/naidra68/belajar-mysql">Belajar MYSQL</a></li>
    <li><a id="belajarBootstrap">Belajar Bootstrap</a></li>
</ul>
```

```css
:link {
    color: red;
}
```

Jika dijalankan, tulisan Belajar Bootstrap tidak akan di style karena meskipun menggunakan tag `<a>` namun tag tersebut tidak memiliki attribute `href` yang menjadikan `:link` tidak bisa mengidentifikasi kalau tag tersebut sebuah link.
