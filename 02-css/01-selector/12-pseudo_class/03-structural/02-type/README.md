# :First Type and :Last Type Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Selector `:first-of-type` dan `:last-of-type` hampir mirip seperti selector `:first-child` dan `:last-child`. Perbedaan-nya? Hanya pada perilaku element-nya.

Saya gunakan contoh paragraf didalam div saja karena jika menggunakan `<li>` maka perbedaan-nya tidak terlihat. 

Jadi seperti ini, ketika menggunakan `:first-child` atau `:last-child`, maka saya perlu memastikan. Apakah sebuah paragraf itu ada di anak pertama dari sebuah div, bukan? Nah, disini letak perbedaan-nya.

Ketika menggunakan `:first-of-type` atau `:last-of-type` maka hal tersebut tidak berlaku. Meskipun paragraf tidak berada di anak pertama dari sebuah div, namun selagi paragraf tersebut berada di dalam sebuah div maka tetap akan di style. Inilah perbedaan kecil namun cukup rumit untuk dipahami.

berikut contoh penerapan-nya.

```html
<div>
    <h2>header 1 didalam tag div</h2>
    <p>paragraf pertama didalam tag div</p>
    <p>paragraf kedua didalam tag div</p>
</div>
<div>
    <p>Paragraf pertama didalam tag div</p>
    <p>Paragraf kedua didalam tag div</p>
    <p>Paragraf ketiga didalam tag div</p>
</div>
```

```css
p:first-of-type{
    color: red;
}

p:last-of-type{
    color: blue;
}
```

Jika dijalankan, `<div>` yang memiliki anak pertama berupa `<h2>` akan diabaikan dan tetap milih tag `<p>` sebagai first-type nya. Selain itu, masih sama untuk last-type tidak ada perubahan. Perilaku ini cukup kecil perbedaan, namun sangat krusial jika digunakan ketika menghadapi project.

Jika menggunakan `:first-child` atau `:last-child` maka hasil-nya akan berbeda. Penasaran? Dicoba saja biar ilang tuh rasa penasaran. :smile:
