# :First nth Child and :Last nth Child Selector

Tanda kurung di dalam selector `:nth-child()` dan `:nth-last-child()` adalah tempat bagi huruf atau angka yang dipakai untuk mencari tag HTML berdasarkan urutannya atau pola tertentu. Tanda kurung menandakan bahwa pseudo class tersebut merupakan sebuah fungsi.

Pola yang bisa diterapkan untuk kedua selector cukup beragam. Selain angka, saya bisa menulis keyword khusus seperti "odd" atau "even", serta pola matematis seperti penambahan.

berikut contoh penerapan-nya

```css
li:nth-child(odd) {
    background-color: purple;
}
li:nth-child(even) {
    background-color: steelblue;
}
```

Jika dijalankan, nampak warna selang-seling antara list tersebut. Hal seperti ini digunakan untuk memberikan style pada list agar terlihat menarik.

Untuk `:last-nth-Child` sama seperti `:nth-child` fungsi-nya, cuma perbedaan pada urutan kolom. Jika `:nth-child` dilakukan dari atas list, maka `:last-nth-child` dilakukan dari bawah list.