# :visited Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

:link Selector digunakan untuk mencari sebuah link yang telah dikunjungi. Biasanya ini akan terlihat ketika user telah click link pada tag `<a>`.

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

Jika dijalankan, link yang belum pernah dibuka akan berwarna merah. Setelah link di click, menuju lokasi link tersebut dan kembali ke index maka link tersebut akan berubah style sesuai code css yang dibuat. Silahkan mencoba.
