# :target Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Selector :target sangat spesifik karena baru akan aktif ketika mengakses sebuah "anchor link", yakni internal link pada sebuah halaman.

berikut contoh penerapan-nya.

```html
<a id="halPertama">Halaman Pertama</a>
<ul>
    <li><a href="https://github.com/naidra68/belajar-html">Belajar HTML</a></li>
    <li><a href="https://github.com/naidra68/belajar-css">Belajar CSS</a></li>
    <li><a href="https://github.com/naidra68/belajar-javascript">Belajar Javascript</a></li>
    <li><a href="https://github.com/naidra68/belajar-php">Belajar PHP</a></li>
    <li><a href="https://github.com/naidra68/belajar-mysql">Belajar MYSQL</a></li>
</ul>
<a href="#halPertama">Kembali ke link Halaman Pertama</a>
```

```css
:target {
    color: magenta;
}
```

Jika dijalankan, maka tidak terjadi apapun. Namun, ketika klik link **Kembali ke link Halaman Pertama** maka link **Halaman Pertama** akan di style.