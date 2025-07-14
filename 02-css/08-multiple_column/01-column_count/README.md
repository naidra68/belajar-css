# Column Count

Property `column-count` digunakan untuk mengatur pembagian kolom teks-nya. Nilai yang bisa diisi berupa angka seperti 2,3 atau 4. Web browser akan membagi kolom teks secara otomatis.

berikut contoh penerapan-nya

```html
<div class="column-count">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum minima reiciendis molestiae error itaque iure sequi nostrum totam provident, obcaecati quam eos dolorum minus cumque asperiores ea sapiente eum ullam!</p>
    <p>Nihil, expedita, ex unde sed nesciunt cupiditate iusto cumque dolore explicabo, reiciendis quo aperiam hic fuga nam optio alias nemo autem. Deleniti alias repudiandae iusto voluptas, omnis consequatur. Iste, exercitationem!</p>
    <p>Fugit corporis repellendus amet dicta laborum enim minima saepe expedita assumenda nihil mollitia neque, cumque quod nobis asperiores adipisci aliquid totam! Cumque illum animi natus nulla consequuntur libero aspernatur neque.</p>
</div>
```

```css
.column-count {
    column-count: 3;
    margin: 1em;
}
```

Jika dijalankan, terlihat bahwa saya membagi 3 paragraf nya menggunakan `column-count` yang berisi nilai 3.

