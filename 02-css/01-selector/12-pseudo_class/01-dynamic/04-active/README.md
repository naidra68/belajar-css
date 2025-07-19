# :active Selector

:active selector akan aktif persekian detik, yakni ketika men-klik tombol mouse dan tahan jangan sampai melepaskan untuk melihat efeknya.

berikut contoh penerapan-nya.

```html
<ul>
    <li><a href="https://github.com/naidra68/belajar-html">Belajar HTML</a></li>
    <li><a href="https://github.com/naidra68/belajar-css">Belajar CSS</a></li>
    <li><a href="https://github.com/naidra68/belajar-javascript">Belajar Javascript</a></li>
    <li><a href="https://github.com/naidra68/belajar-php">Belajar PHP</a></li>
    <li><a href="https://github.com/naidra68/belajar-mysql">Belajar MYSQL</a></li>
</ul>
```

```css
a:active {
    color: red;
}
```

Jika dijalankan, maka akan diperlihatkan perubahan style secara cepat sepersekian detik jika tidak menahan tombol-nya. Namun, ketika klik dan tahan maka akan melihat efeknya secara terus-menerus.