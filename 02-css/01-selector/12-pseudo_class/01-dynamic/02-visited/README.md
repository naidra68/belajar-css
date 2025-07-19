# :visited Selector

:visited Selector digunakan untuk mencari sebuah link yang telah dikunjungi. Biasanya ini akan terlihat ketika user telah click link pada tag `<a>`.

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
:link {
    color: red;
}

:visited {
    color: green;
}
```

Jika dijalankan, link yang belum pernah dibuka akan berwarna merah. Setelah link di click, menuju lokasi link tersebut dan apabila kembali ke index lagi, maka link tersebut akan berubah style sesuai code css yang dibuat.
