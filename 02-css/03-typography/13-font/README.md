# Font

Property ini merupakan property khusus yang berisi dari semua property `font` dan biasanya property ini dikenal sebagai shorthand notation. Intinya untuk menyingkat penulisan `font`.

Semua property `font` yang telah dipraktekkan bisa disingkat dengan property ini. Berikut daftar property apa saja yang bisa disingkat oleh `font`.

- font-style
- font-variant
- font-weight
- font-size
- line-height
- font-family

berikut contoh penerapan-nya

```html
<p class="satu">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sint vero, voluptas libero perferendis non quisquam quo tempora temporibus est recusandae laborum exercitationem blanditiis deleniti ipsum rerum unde quod ex similique?</p>
<p class="dua">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur corporis laudantium nulla, deleniti repudiandae, cupiditate, velit ab rem fuga sapiente ipsum aperiam ipsam facilis aliquam? Eaque dolores tempora expedita illo.</p>
<p class="tiga">Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel sed architecto enim. Asperiores, vel. Temporibus beatae accusantium obcaecati ipsa. Dolore illo rem minima esse corporis ea libero adipisci alias facere.</p>
<p class="empat">Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum nisi aliquid, tempore ea culpa dolore placeat rerum fugiat debitis est doloremque atque quod quia aliquam hic iste? Sit, officiis explicabo!</p>
```

```css
.satu {
    font: 18px sans-serif;
}
.dua {
    font: bold 12px Arial;
}
.tiga {
    font: 400 italic 20px sans-serif;
}
.empat {
    font: italic small-caps bolder 16px/2 cursive;
}
```

Penulisan Shorthand Notation ini membuat kode saya sangat ringkas. Namun, penulisan ini memiliki kelemahan ketika developers atau programmer tidak mengerti aturan penulisan-nya.

Jika dilihat pada class `.satu`, saya cuma mendefinisikan `font-size` dan `font-family` saja. Namun yang sebenarnya adalah semua property yang tidak tertulis akan diset `normal` secara otomatis oleh web browser.

berikut contoh penerapan-nya

```html
<h1 class="pertama">Header Pertama</h1>
<h1 class="kedua">Header Kedua</h1>
```

```css
.pertama {
    font-size: 20px;
    font-family: sans-serif;
}
.kedua {
    font: 20px sans-serif;
}
```

Jika dijalankan, header 1 akan tampak normal, namun header 2 tidak normal karena teks tebal-nya tiba-tiba hilang. Mengapa ini bisa terjadi? Penjelasannya ada diatas.

jika saya menulis berikut

> `font: 20px sans-serif;`

maka web browser akan menjalankan berikut

> `font: normal normal normal 20px/normal sans-serif;`

Inilah kelemahan yang saya maksud, pastikan sudah paham konsekuensi jika menggunakan property `font`.