# Media Query Introduce

Pada dasarnya, **media query** adalah versi upgrade dari **media type**. Mengingat kembali bahwa **media type** adalah teknik yang dipakai untuk menampilkan kode css secara berbeda-beda tergantung dari media apa website tersebut diakses.

Karena hal itu, **media query** ini adalah versi terbaru dari **media type** yang telah lama ditinggalkan. Untuk menggunakan **media querty**, penulisan-nya sangat mirip dengan **media type** namun terdapat tambahan aturan yang lebih fleksible.

contoh code css

```css
@media not print {
    /* Kode CSS */
}
@media only screen {
    /* Kode CSS */
}
```

Terdapat dua perintah pada media query yaitu `not` dan `only`. Apablia perintah `not|only` tidak ditulis maka akan dianggap tampil pada semua jenis tipe media.

Dengan ini, developers bisa mengatur supaya code css hanya berjalan pada dimensi tertentu, resolusi tertentu, atau aturan-aturan lain.