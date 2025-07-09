# Font Variant

Property `font-variant` memiliki fungsi cukup unik. Apabila saya definisikan sebuah teks menjadi huruf besar atau huruf kapital semua dan menggunakan `font-variant: samll-caps` maka efek-nya cukup menarik, karena teks akan tampil huruf kapital namun font-size nya agak mengecil.

Terdapat dua nilai dari font-variant ini
- small-caps
- normal

`small-caps` sudah dijelaskan, intinya tetap mempertahankan huruf kapital (jika menggunakan huruf kapital) dan menurunkan size-nya.

`normal` digunakan untuk menghapus efek dari `font-variant`.

berikut contoh penerapan-nya

```html
<h1 class="normal">Header 1 normal</h1>
<h1 class="smallcaps">Header 1 smallcaps</h1>
```

```css
.normal {font-variant: normal;}
.smallcaps {font-variant: small-caps;}
```

Hasilnya cukup unik, property ini bisa digunakan ketika membutuhkan semua huruf capital namun kata pertama lebih tinggi size nya. Jika mengatur menggunakan property lain cukup rumit.