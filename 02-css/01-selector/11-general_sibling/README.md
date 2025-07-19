# General Sibling Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

General sibling selector sangat mirip dengan adjacent selector. Bedanya, jika pada adjacent selector hanya cocok dengan satu tag yang menjadi sibling (saudara), general sibling selector akan cocok dengan seluruh sibling (saudara). Karakter tilde `~` dipakai untuk membuat general sibling selector.

Menggunakan strukur HTML sebelumnya, berikut contoh penerapan-nya.

```html
<div>
    <h2>Header 2 dalam tag div</h2>
    <p>Paragraf pertama dalam tag div</p>
    <p>Paragraf kedua dalam tag div</p>
</div>
<div>
    <h2>Header 2 dalam tag div</h2>
    <p>Paragraf pertama dalam tag div</p>
    <p>Paragraf kedua dalam tag div</p>
</div>
<h2>Header h2 di luar tag div</h2>
<p>Paragraf yang berada di luar tag div</p>
```

```css
h2 ~ p {
    color: red;
}
```

Jika dijalankan, terlihat bahwa semua tag `<p>` setelah `<h2>` akan memiliki style warna yang sama. Jika menggunakan adjacent selector, maka tag `<p>` yang di style hanyalah satu tag saja dan tag setelahnya tidak akan di style.

coba jalankan code css berikut

```css
h2 + p {
    color: red;
}
```

Code diatas adalah adjacent selector, jika dijalankan maka terlihat bahwa tag `<p>` hanya akan di style 1x dan tag `<p>` dibawahnya tidak terkena style.

Baiklah, sekarang apa perbedaan-nya general sibling ini dengan descendant selector? Bukankah menggunakan descendant maka bisa seperti itu? Jawabannya berbeda.

berikut contoh penerapan-nya

```html
<h2 class="general">General Sibling</h2>
<p>Paragraf Pertama</p>
<p>Paragraf Kedua</p>

<div>
    <h2 class="descendant">Descendant</h2>
    <p>Paragraf Pertama</p>
    <p>Paragraf Kedua</p>
</div>
```

```css
 .general ~ p {
     color: red;
 }
 .descendant p {
     color: red;
 }
```

Jika dijalankan, terlihat bahwa general sibling akan mencari tag `<p>` setelah tag `<h2>`. Sedangkan descendant akan mencari anak-nya, apakah tag `<h2>` memiliki anak berupa tag `<p>` jika iya maka style, jika tidak maka tidak style.

Kesimpulannya adalah gunakan sibling selector apabila stuktur html berupa sibling. Berikut contoh struktur html yang dikatakan sebagai sibling element.

```html
<h2>Saudara pertama</h2>
<p>Saudara kedua</p>
```

Gunakan descendant selector apabila struktur html berupa parent child. Berikut contoh struktur html yang dikatakan sebagai parent child element.

```html
<div> <!-- parent element -->
    <h2>Anak pertama</h2> <!-- child element -->
    <p>Anak kedua</p> <!-- child element -->
</div>
```

Memang cukup rumit dan membingungkan jika melihat perbedaan antara descendant, child, adjacent dan general sibling. Namun, dengan memahami ini maka nantinya akan lebih mudah untuk membuat struktur HTML yang proper ketika ingin di style.