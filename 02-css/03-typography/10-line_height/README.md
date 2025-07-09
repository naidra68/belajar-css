# Line Height

Property ini berfungsi untuk mengatur spacing teks atau baris spasi pada teks. `line-height` bisa disebut sebagai spasi paragraf karena fungsi-nya memang seperti itu.

berikut contoh penerapan-nya

```html
<p class="satu">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam dignissimos ex sit ipsam quae! Officiis saepe, corrupti id eveniet dolore labore sit sapiente. Accusamus voluptate, non aliquid dicta laudantium aliquam.</p>
<p class="dua">Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure minima cupiditate fuga, eius, reprehenderit repellat natus quasi necessitatibus harum hic amet? Modi debitis numquam placeat unde porro excepturi autem alias.</p>
<p class="tiga">Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ratione fugit nisi maiores, a, iure corporis rem soluta ducimus asperiores, facilis beatae harum similique sapiente error in quasi corrupti! Odio!</p>
```

```css
.satu {line-height: 1.2em;}
.dua {line-height: 140%;}
.tiga {line-height: 1.9;}
```

Secara default, spasi paragraf oleh web browser adalah 1,2x ukuran teks. Jika saya definsikan menggunakan `em` maka sebesar `1.2em`.

Selain itu, saya dapat mendefinisikan nilai nya tanpa satuan apapun seperti `1.9` maka dia akan diset 1,9x ukuran teks. Terdapat sebuah trik agar posisi teks berada ditengah dengan posisi vertikal.

berikut contoh penerapan-nya

```html
<div class="pertama">
Teks akan diposisikan ditengah secara vertikal
</div>
<div class="kedua">
Teks akan diposisikan ditengah secara vertikal
</div>
```

```css
.pertama {
    line-height: 50px;
    background-color: green;
}
.kedua {
    line-height: 150px;
    background-color: tomato;
}
```

Trik seperti ini sering dipakai dulu oleh developers dan programmer untuk membuat teks dapat berata ditengah dengan vertical. Hal ini cukup lumrah sebelum datang-nya `flexbox`.