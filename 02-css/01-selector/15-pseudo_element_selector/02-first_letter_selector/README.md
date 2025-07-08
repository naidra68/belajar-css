# ::first-letter Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Apabila selector `::first-line` dipakai untuk mengakses baris pertama sebuah element, maka selector `::first-letter` berguna untuk mengakses huruf/karakter pertama dari sebuah element.
Dengan `::first-letter`, saya bisa membuat efek drop cap, dimana huruf pertama dibuat besar 

berikut contoh penerapan-nya.

```html
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus, dolor veniam? Voluptatibus, deleniti neque asperiores quasi, quod, iste odio fugiat perferendis debitis vitae fuga tempore aliquam similique sint officiis assumenda.</p>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus, dolor veniam? Voluptatibus, deleniti neque asperiores quasi, quod, iste odio fugiat perferendis debitis vitae fuga tempore aliquam similique sint officiis assumenda.</p>
```

```css
p::first-letter {
    font-size: 30px;
    font-weight: bold;
}
```

Jika dijalankan, maka karakter pertama pada huruf pertama akan di style. Sebelum adanya fungsi ini, cukup susah untuk membuat hal yang sama karena saya harus menggunakan tag `<span>` dan style tersendiri, itu cukup merepotkan. 

Fungsi `::first-letter` ini berguna jika ingin membuat web berita dengan artikel kata pertama huruf besar. Namun, saat ini teknik seperti ini jarang digunakan lagi.
