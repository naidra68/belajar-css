# Text Align

Property ini berfungsi untuk mengatur rata teks dari sebuah element maupun paragraf. CSS menyediakan `text-align` dengan berbagai isi sebagai berikut.

- left
- center
- right
- justify

`left` merupakan nilai default jika property ini tidak didefinisikan. Fungsi-nya akan meratakan teks ke sebelah kiri.

`center` berfungsi agar teks akan rata ke tengah.

`right` berfungsi agar teks rata ke kanan.

`justify` berfungsi agar teks sama rata (kiri kanan), biasanya tampilan-nya agar rapi.

berikut contoh penerapan-nya

```html
<p class="left">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam dignissimos ex sit ipsam quae! Officiis saepe, corrupti id eveniet dolore labore sit sapiente. Accusamus voluptate, non aliquid dicta laudantium aliquam.</p>
<p class="center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure minima cupiditate fuga, eius, reprehenderit repellat natus quasi necessitatibus harum hic amet? Modi debitis numquam placeat unde porro excepturi autem alias.</p>
<p class="right">Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ratione fugit nisi maiores, a, iure corporis rem soluta ducimus asperiores, facilis beatae harum similique sapiente error in quasi corrupti! Odio!</p>
<p class="justify">Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae repellat quaerat vitae, sequi excepturi hic accusamus laborum velit iure corporis magni obcaecati nisi quibusdam. Adipisci, inventore. Deserunt reiciendis consequuntur tempora?</p>
```

```css
.left {text-align: left;}
.center {text-align: center;}
.right {text-align: right;}
.justify {text-align: justify;}
```

> Jika dilihat, `justify` terlihat lebih rapi daripada rata kiri. Namun untuk sekarang, `justify` sangat kurang bagus untuk UX (User Experience). Bahkan, web sekarang ini tidak memakai `justify` pada konten mereka.