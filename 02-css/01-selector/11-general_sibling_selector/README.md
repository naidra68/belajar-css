# General Sibling Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

General sibling selector sangat mirip dengan adjacent selector. Bedanya, jika pada adjacent selector hanya cocok dengan satu tag yang menjadi sibling, general sibling selector akan cocok
dengan seluruh sibling. Karakter tilde " ~ " dipakai untuk membuat general sibling selector. Berikut contoh kode-nya.

```css
h2 ~ p {
    color: red;
}
```

1. `General Sibling Selector` = Cari tag 1 dan style tag berikutnya (semua tag).
2. `Adjacent Selector` = Cari tag 1 dan style tag berikutnya (namun hanya satu tag).



Bukankah ini mirip seperti Descendant Selector? Jika menggunakan Descendant kan bisa gunakan code berikut.

```css
div p {
    color: red;
}
```

Hasilnya sama, lalu apa bedanya?

Perbedaan paling mendasar adalah antara sibling dan parent child. Ketika saya menggunakan descendant seperti kode diatas, maka saya menggunakan *parent child relationship*. Sedangkan jika saya menggunakan adjacent atau general sibling maka saya menggunakan *sibling relationship*.

> Jika kode descendant selector dijalankan, maka paragraf yang berada di luar tag `<div>` tidak akan di style.

Bagaimana jika menggunakan kode berikut :

```css
div ~ p {
    color: red;
}
```

Bukankah ini akan membuat tag `<p>` yang berada didalam tag `<div>` akan di style?

> Jawabannya iya. Jika kode tersebut dijalankan akan memberikan style pada tag `<p>`. Namun, tag `<p>` yang di style bukanlah di dalam tag `<div>` melainkan di luar. Inilah penting memahami perbedaan antara *parent child relationship* dan *sibling relationship*.