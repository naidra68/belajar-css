# Overflow

Property ini ada kaitan dengan `width` dan `height`. Overflow digunakan untuk menampung isi konten yang telah melimpah keluar element. Property ini memiliki isi `visible`, `hidden`, `scroll`, dan `auto`.

Sebelum masuk ke contoh overflow, saya lihat terlebih dahulu maksud dari konten yang melimpah keluar element itu seperti apa.

berikut contoh code-nya

```html
<p class="satu">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi aut quam veritatis! Quaerat assumenda atque laborum, perferendis tempora itaque maiores numquam libero non id deserunt distinctio laboriosam eveniet fugit. Cupiditate.</p>
```

```css
.satu {
    width: 300px;
    height: 50px;
    background-color: yellow;
}
```

Jika dijalankan, terlihat bahwa isi konten dan background konten tidak sinkron atau sama. Inilah yang disebut sebagai content melimpah keluar element.

Untuk mengatasi masalah ini, property `overflow` adalah solusi yang tepat.

berikut contoh penerapan-nya

```html
<p class="visible">Visible : Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam, totam eos corrupti soluta maiores sit nulla dolores voluptates doloremque quos id. Voluptate aut quis culpa eius deleniti aspernatur sequi assumenda?</p>
<br><br>
<p class="hidden">Hidden : Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam, totam eos corrupti soluta maiores sit nulla dolores voluptates doloremque quos id. Voluptate aut quis culpa eius deleniti aspernatur sequi assumenda?</p>
<br>
<p class="scroll">Scroll : Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam, totam eos corrupti soluta maiores sit nulla dolores voluptates doloremque quos id. Voluptate aut quis culpa eius deleniti aspernatur sequi assumenda?</p>
<br>
<p class="auto">Auto : Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam, totam eos corrupti soluta maiores sit nulla dolores voluptates doloremque quos id. Voluptate aut quis culpa eius deleniti aspernatur sequi assumenda?</p>
```

```css
p {
    width: 300px;
    height: 50px;
    background-color: cyan;
}

.visible {
    overflow: visible;
}
.hidden {
    overflow: hidden;
}
.scroll {
    overflow: scroll;
}
.auto {
    overflow: auto;
}
```

Terdapat beberapa isi dari overflow yang telah ditulis. Berikut pembahasan mengenai isi dari property.

1. `visible` merupakan nilai default `overflow` jika tidak didefinisikan.
2. `hidden` merupakan nilai yang berfungsi untuk menyembunyikan konten melimpah tersebut.
3. `scroll` merupakan nilai yang berfungsi untuk menyembunyikan konten agar nanti-nya dapat discroll.
4. `auto` merupakan nilai yang sama seperti `scroll` namun lebih fleksible.

Property `overflow` ini memiliki sumbu x dan sumbu y untuk mengatur setiap konten-nya. Sumbu x untuk Horizontal dan sumbu y untuk Vertical.

Untuk mengatur sumbu x menggunakan property `overflow-x` dan untuk mengatur sumbu y menggunakan property `overflow-y`.

berikut contoh penerapan-nya.

```html
<p class="overflow-xy">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium soluta suscipit eius quisquam repudiandae est, doloribus corrupti numquam natus asperiores illo beatae, ratione et fuga assumenda! Quae provident obcaecati iure.</p>
```

```css
.overflow-xy {
    overflow-x: hidden;
    overflow-y: scroll;
}
```

Jika dijalankan, tampak seperti `overflow: auto`. Karena saya buatnya agar mirip seperti itu biar mudah saya mengerti.