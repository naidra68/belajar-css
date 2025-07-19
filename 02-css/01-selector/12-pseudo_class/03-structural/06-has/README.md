# :has() Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Pseudo Class ini digunakan untuk memberi style pada element yang mengandung suatu elemen lain bahkan element itu sendiri.

berikut contoh penerapan-nya

```html
<div>
    Div Pertama
    <p>Paragraf Pertama</p>
</div>
```

```css
div:has(p) {
    color: red;
}
```

Jika dijalankan, ini berarti pilih semua tag `<div>` yang setidaknya memiliki satu tag `<p>` didalam-nya. Bahkan kalimat **"Div Pertama"** pun tetap terkena style karena menggunakan `:has` ini.

Bagaimana dengan descendant selector? Bukankah menggunakan itu juga bisa? Jawabannya tidak sama. Apabila menggunakan descendant selector, maka jika terdapat konten yang ada di tag `<div>` itu sendiri tidak ikut terkena style.

berikut contoh code css-nya

```css
div p {
    color: red;
}
```

Jika dijalankan, terlihat bahwa paragraf memang mendapatkan style-nya, namun lihat lagi bahwa kalimat **"Div Pertama"** tidak memiliki style karena sifat dari descendant adalah turunan.

Saya akan mencoba membuat sebuah studi kasus sederhana untuk melihat bahwa `:has()` ini lebih powerful daripada descendant.

Contoh studi kasus : Saya akan membuat 2 buah tag `<div>` yang masing-masing memiliki 2 tag yaitu `<h2>` dan `p`. Namun pada tag `<div>` kedua saya menambahkan tag `<span>` didalam tag `<h2>`.

berikut contoh penerapan-nya

```html
<div>
    <h2>Judul</h2>
    <p>Paragraf Pertama</p>
</div>

<div>
    <h2>Judul <span>Baru</span></h2>
    <p>Paragraf Pertama</p>
</div>
```

Selanjutnya, saya akan style seluruh div dengan warna yang sama, nantinya semua element yang berada didalam tag `<div>` terkena warna yang sama semua.

berikut contoh penerapan-nya

```css
div {
    color: red;
}
```

Setelah semua warna menjadi sama, saya ingin tag `<div>` yang **memiliki** atau **didalam-nya** terdapat tag `<span>` akan saya ubah seluruh warna-nya, **Ingat!!** bahwa yang memiliki tag `<span>` saja.

berikut contoh penerapan-nya

```css
div:has(span) {
    color: blue;
}
```

Jika dijalankan, terlihat bahwa tag `<div>` yang memiliki tag `<span>` didalam-nya akan berubah warna. Mengapa menggunakan descendant tidak bisa? kan tinggal pake saja descendant seperti berikut :

```css
div span {
    color: blue;
}
```

Ini tidak bisa, jika dijalankan pun. Akan terlihat bahwa yang berubah warna nya hanyalah tag `<span>` yang memiliki isi kalimat **"Baru"** saja. Karena saya ingin mengubah semuanya bukan hanya tag `<span>` saja, maka dari itu descendant tidak cocok sama sekali dengan studi kasus seperti ini. `:has()` selector lah yang sangat cocok untuk mengatasi hal ini.

Sebenarnya, masih banyak keunggulan `:has()` ini. Namun karena terlalu kompleks maka saya skip dulu karena belum mengerti.