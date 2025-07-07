# Child Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Child selector digunakan untuk mencari anak pertama dari struktur DOM. Mirip seperti Descendant Selector yang dimana menggunakan strukur DOM parent-child relationship.

Jika dijelaskan tanpa contoh code memang membingungkan. Berikut contoh code-nya. Sebelum masuk ke child selector, saya coba dulu dengan descendant agar lebih mudah paham.


```html
<h1>Belajar CSS</h1>
<p>Paragraf Pertama diluar</p>
    <div>
        <p>Paragraf pertama dalam tag div</p>
        <p>Paragraf kedua dalam tag div</p>
        <article>
            <p>Paragraf yang berada di dalam tag div dan article</p>
            <p>Paragraf yang berada di dalam tag div dan article</p>
        </article>
        <p>Paragraf ketiga dalam tag div</p>
    </div>
```

```css
div p {
    color: blue;
}
```

Jika dijalankan, maka seluruh tag `<p>` yang berada di dalam tag `<div>` akan berubah warna-nya karena saya style, bahkan tag `<p>` yang berada didalam tag `<article>` pun tetap kena style. Karena tag `<article>` tetap berada di dalam tag `<div`.

<hr>

Perbedaan dari Child Selector adalah dia hanya mencari first child (anak pertama) dari tag parent (induk). Untuk menggunakan child selector maka dipisahkan dengan tanda lebih besar `>`.

Saya akan melakukan 2 percobaan mengenai child selector ini agar lebih paham cara pengunaan-nya.

> Perhatikan penjelasan berikut mengenai struktur DOM HTML diatas, ini perlu dipahami karena cukup membingungkan.

1. tag `<div>` memiliki anak yaitu tag `<p>` dan tag `<article>`.
2. tag `<div>` berarti memiliki 2 anak, karena 3 tag `<p>` dianggap anak pertama dan tag `<article>` dianggap anak kedua.
3. tag `<p>` anak pertama dari induk `<div>`
3. tag `<article>` anak kedua dari induk `<div>`


## 1. Percobaan Pertama

Berikut code menggunakan child selector.

```css
div > p {
    color: blue;
}
```

## 2. Percobaan Kedua

Coba child selector untuk diterapkan dalam list bersarang (nested list). List bersarang itu seperti list didalam list.
```html
<ol>
    <li>List 1</li>
    <li>List 2</li>
        <ul>
            <li>Sub List 1</li>
            <li>Sub List 2</li>
            <li>Sub List 3</li>
        </ul>
    <li>List 3</li>
    <li>List 4</li>
</ol>
```

```css
ul > li {
    color: blue;
}
```
