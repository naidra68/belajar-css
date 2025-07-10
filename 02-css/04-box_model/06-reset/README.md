# Reset

Sepanjang perjalanan belajar CSS, saya pernah membuat universal selector dengan mendefinisikan `margin` dan `padding`. Jadi itu untuk apa?

Jawabannya adalah Reset. Salah satu tantangan web design adalah membuat web dengan design sendiri, setiap web browser memiliki style bawaan sendiri-sendiri.

Hal tersebut tidak fleksible jika saya sebagai developers dan programmer ingin membuat program dan design secara fresh. Maka dari itu diperulkan CSS Reset.

CSS Reset bertujuan men-nol-kan seluruh perbedaan ini. Dengan kata lain, kita menghapus seluruh margin, padding, border, serta beberapa property lain. Kode * {margin: 0; padding: 0} adalah versi paling sederhana dari CSS Reset.

Saat ini tersedia berbagai teknik terkait CSS Reset, yang paling terkenal yaitu Eric Meyer's CSS Reset. Eric Meyer adalah seorang web desainer Amerika Serikat dan penulis buku terkenal
tentang CSS. Ia merupakan salah satu web desainer yang pertama kali menerapkan CSS reset untuk mengatasi perbedaan default style pada web browser.

Untuk saat ini, cukup menggunakan universal selector dan menggunakan property `margin` dan `padding` dengan set 0 sudah cukup.

berikut contoh penerapan-nya

```css
* {
    padding: 0;
    margin: 0;
}
```

Perlukah menggunakan CSS Reset? Saat ini cukup perlu karena dari style web browser berbeda-beda, maka diperlukan CSS Reset agar style pada web bisa diatur ulang oleh saya sebagai developers dan programmer.



