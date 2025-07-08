# ::before dan ::after Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Pseudo element selector `::before` dan `::after` dikenal juga sebagai selector generated content. Karena dari kedua selector ini saya bisa menyisipkan konten baru ke dalam struktur HTML. apakah itu berupa teks, gambar, atau bahkan sebuah artikel yang terdiri dari beberapa paragraf.

1. `::before` = digunakan untuk menambah konten sebelum element HTML.
2. `::after` = digunakan untuk menambah konten setelah element HTML.

Agar dapat bekerja, `::before` dan `::after` memiliki tambahan property `content` yang di inisialisasi diawal.

berikut contoh penerapan-nya.

```html
<ul>
    <li><a href="https://github.com/naidra68/belajar-html">HTML</a></li>
    <li><a href="https://github.com/naidra68/belajar-css">CSS</a></li>
    <li><a href="https://github.com/naidra68/belajar-javascript">Javascript</a></li>
    <li><a href="https://github.com/naidra68/belajar-php">PHP</a></li>
    <li><a href="https://github.com/naidra68/belajar-mysql">MYSQL</a></li>
</ul>
```

```css
a::before {
    content: 'Belajar ';
}
a::after {
    content: ' [pemula]';
}
```

Jika dijalankan, akan ada penambahan kalimat diawal dan diakhir. 


Contoh lain penggunaan 2 pseudo element ini. Saya akan membuat sebuah tulisan nomer urut mulai dari 1,2,3 dan seterusnya tergantung dari berapa banyak-nya tag `<h3>`.

berikut contoh code-nya

```html
<h3>Nomer</h3>
<h3>Nomer</h3>
<h3>Nomer</h3>
<h3>Nomer</h3>
<h3>Nomer</h3>
```

```css

h3::after {
    content: " Ke - " counter(urutan);
}

h3 {
    counter-increment: urutan;
}

```



Fungsi dari `::before` dan `::after` tidak hanya sederhana seperti itu. Fungsi ini sangat digunakan ketika membuat web kompleks. Animasi CSS keren juga dapat dibuat dengan memanfaatkan fungsi dari kedua pseudo element ini.