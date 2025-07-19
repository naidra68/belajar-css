# :link Selector

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

Jika dijalankan, tulisan Belajar Bootstrap tidak akan di style karena meskipun menggunakan tag `<a>` namun tag tersebut tidak memiliki attribute `href` yang menjadikan `:link` tidak bisa mengidentifikasi kalau tag tersebut adalah sebuah link.
