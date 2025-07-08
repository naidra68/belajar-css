# ::first-line Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

selector ::first-line dipakai untuk mengakses baris pertama dari
sebuah element HTML.

berikut contoh penerapan-nya.

```html
<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ratione, culpa! Ratione facere delectus debitis ipsam, odit ullam aspernatur nemo, obcaecati sunt unde provident labore vitae laboriosam iure eveniet eligendi veritatis!</p>
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem libero harum quis reiciendis omnis iste alias culpa pariatur modi laboriosam minus, enim est commodi mollitia numquam animi consectetur! Necessitatibus, iusto.</p>
```

```css
p::first-line {
    color: green;
}
```

Jika dijalankan, maka setiap baris pertama akan di style. Hal ini tetap konsisten meskipun jendela web browser diperkecil maupun diperbesar. Tetap baris pertama saja yang akan di style.
