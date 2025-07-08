# UI Element State Pseudo Class Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

UI Element State Pesudo Class Selector merupakan jenis selector yang digunakan untuk mencari element HTML berdasarkan kondisi dari element tersebut.

Secara umum, pseudo class selector ini digunakan untuk element from HTML. Beberapa selector yang dibahas sebagai berikut.

1. :disabled
2. :enabled
3. :checked

Sesuai nama-nya, saya bisa berikan style pada setiap pseudo class ini. Saya akan mencoba-nya satu persatu.

## 1. :disabled

```html
<p><input type="text" name="nama" disabled></p>
```

```css
input:disabled {
    border: 3px solid red;
}
```

Jika dijalankan, maka setiap input yang memiliki attribute `disabled` akan di style.

## 2. :enabled

```html
<p><input type="text" name="umur"></p>
```

```css
input:enabled {
    border: 3px solid green;
}
```

Jika dijalankan, maka semua input yang tidak memiliki kondisi akan di style. Karena nilai default dari input ini adalah enabled.

## 3. :checked

```html
<p><input type="checkbox" name="windows">Windows</p>
<p><input type="checkbox" name="linux">Linux</p>
```

```css
input:checked {
    margin: 30px;
}
```

Jika dijalankan, maka semua input yang memiliki attribute `checked` akan di style.



