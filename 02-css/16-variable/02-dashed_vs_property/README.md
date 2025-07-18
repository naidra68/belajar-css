# 2 Dashes ( - - ) vs @property

Jadi apa perbedaan menggunakan prefix 2 dashed dan `@property` rule? Perbedaan paling jelas adalah terletak pada pewarisan element.

Apabila saya membuat sebuah nested div (div bersarang) menggunakan prefix 2 dashed untuk mengatur style-nya, maka setiap element akan mewarisi style tersebut.

Untuk mengatur pewarisan ini, menggunakan `@property` rule adalah pilihan yang tepat dan efektif karena ada pengaturan mengenai perwarisan harus ada atau tidak.

contoh permasalahan pada pewarisan dengan prefix 2 dashed `( - - )`.

berikut contohnya

```html
<div class="parent">
    <p>Parent</p>
    <div class="child">
        <p>child</p>
        <div class="grandchild1"><p>Grandchild</p></div>
        <div class="grandchild2"><p>Grandchild</p></div>
    </div>
</div>
```

```css
:root {
    --bg-color: teal;
}
div {
    width: 50%;
    margin: 0.5rem auto;
    border: 2px solid black;
    padding: 0.5em;
    text-align: center;
}

div {
    background-color: var(--bg-color);
}
.child {
    --bg-color: aqua;
}
.grandchild1 {
    --bg-color: yellow;
}
```

Jika dijalankan, terlihat bahwa warna yang diwariskan dari element `child` akan masuk ke `grandchild` semua tanpa terkecuali, apabila salah satu element `grandchild` ditimpa oleh background-color lain maka akan berubah, selain itu maka dia akan mewarisi element parent-nya.

Untuk mengatasi mengenai pewarisan ini, bisa dicoba menggunkaan `@property` rule. berikut contoh pewarisan pada `@property` rule jiak tidak ada.

berikut contohnya

```html
<div class="parent">
    <p>Parent</p>
    <div class="child">
        <p>Child</p>
        <div class="grandchild1"><p>GrandChild1</p></div>
        <div class="grandchild2"><p>GrandChild2</p></div>
    </div>
</div>
```

```css
@property --bg-color {
    syntax: "<color>";
    inherits: false;
    initial-value: pink;
}

div {
    width: 50%;
    margin: 0.5rem auto;
    border: 2px solid black;
    padding: 0.5em;
    text-align: center;
}

div {
    background-color: var(--bg-color);
}
.child {
    --bg-color: magenta;
}
```

Jika dijalankan, terlihat bahwa class `grandchild` tidak akan mewarisi warna dari class `child` karena pada `@property` bagian pewarisan saya tulis `false` yang berarti tidak ada pewarisan.

Namun, mengapa warna dari class `grandchild` sama seperti `parent`? Ini terjadi karena class `grandchil` tidak memiliki warna, maka dari itu dia akan menambil warna parent awal-nya.