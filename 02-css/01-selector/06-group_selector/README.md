# Group Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Group selector merupakan sebuah istilah untuk menggabungkan semua selector yang memiliki style sama. Alih-alih menulis selector satu-persatu dengan style yang sama maka saya bisa meng-gabungkan-nya menjadi group selector. Istilah ini bukanlah seperti selector pada kebanyakan, namun hanya menjadi acuan bagi developer atau programmer untuk membuat code css mereka tanpa lebih rapi.

Berikut code css yang dibuat sebelum mengenal group selector. Jika terlihat cukup banyak bukan? padahal saya ingin memberikan style yang sama pada setiap element.


```html
<h1>Belajar CSS</h1>
<p>Paragraf pertama</p>
<h2>Belajar CSS</h1>
<p>Paragraf kedua</p>
```

```css
h1 {
    color: red;
}
h2 {
    color: red;
}
p {
    color: red;
}
```


Cukup banyak ruang bukan? Nah, disinilah fungsi dari group, alih-alih menulis satu-persatu seperti code css diatas, saya bisa menyingkatnya jika menggunakan group selector sebagai berikut.

```css
h1, h2, p {
    color: red;
}
```

Tanda `,` menjelaskan bahwa group selector menjadikan semua element menjadi group dipisahkan dengan tanda `,` tersebut. Tambahan spasi setelah tanda `,` tidak akan mempengaruhi apapun, ini digunakan hanya semata agar terlihat rapi dan tidak mepet saja.

Menggunakan group selector dapat menggabungkan semua selector mulai dari class, id, dan attribute menjadi satu. Berikut contoh penggunaan-nya.

```css
.header-pertama, #headerKedua, [title~="info"] {
    color: blue;
}
```