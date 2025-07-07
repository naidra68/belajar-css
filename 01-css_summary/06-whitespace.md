# Whitespace

Whitespace merupakan istilah untuk karakter spasi yang tidak tampil di layar, termasuk juga tab, dan enter. Dalam penulisan declaration (property dan value), whitespace akan diabaikan.

Berikut penulisan kode CSS berikut akan dianggap sama:

```css
h1 {
    color: red;
    font-size: 24px;
    text-decoration: underline;
}
h1 {color: red;font-size: 24px;text-decoration: underline;}
```

Penulisan pertama sangat mudah dibaca, sedangkan penulisan kedua tidak mudah dibaca. Penulisan pertama lrbih direkomendasikan.

Namun pada penulisan selector, tambahan tanda spasi bisa membuat perbedaan besar seperti contoh berikut:

```css
h1.first {
    color: red;
    font-size: 24px;
    text-decoration: underline;
}
h1 .first {
    color: red;
    font-size: 24px;
    text-decoration: underline;
}
```

Selector h1.first berarti cari seluruh paragraf yang memiliki atribut class="first", sedangkan selector h1 .first berarti cari seluruh tag HTML yang memiliki class="first" dan berada di dalam sebuah paragraf. Kesimpulannya, tanda spasi sangat berpengaruh.