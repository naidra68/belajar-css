# :First nth Child and :Last nth Child Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Tanda kurung di dalam selector :nth-child() dan :nth-last-child() adalah tempat bagi huruf atau angka yang dipakai untuk mencari tag HTML berdasarkan urutannya atau pola tertentu. Hal seperti ini mirip seperti argument function pada bahasa pemrograman.

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