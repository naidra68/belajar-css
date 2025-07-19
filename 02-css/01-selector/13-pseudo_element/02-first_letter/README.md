# ::first-letter Selector

Apabila selector `::first-line` dipakai untuk mengakses baris pertama pada sebuah element, maka selector `::first-letter` berguna untuk mengakses kata pertama dari huruf pada sebuah element. Dengan `::first-letter`, saya bisa membuat efek drop cap, dimana kata pertama dibuat besar.

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

Fungsi `::first-letter` ini berguna jika ingin membuat web berita dengan artikel kata pertama huruf besar. Namun, saat ini pada web modern, jarang ada yang menggunakan pseudo element ini.
