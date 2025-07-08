# :hover Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Dari kebanyakan pseudo class, yang paling menarik dan sangat sering digunakan adalah :hover. Fungsi dari pseudo class ini adalah akan aktif ketika cursor mouse mensorot sebuah element.

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
a:hover {
    color: red;
}
```

Jika dijalankan, link ketika disorot oleh mouse akan berubah style-nya. Pseudo class ini sering digunakan sebagai user interaktif murni CSS yang menarik karena user dapat melihat perbedaan style antara link disorot ataupun tidak.

Saya menggunakan element spesific untuk identifikasi element mana yang akan di hover. Saya menambahkan element selector `a` sebelum `:hover`. Ini berfungsi jika kode css dan struktur html sudah kompleks.