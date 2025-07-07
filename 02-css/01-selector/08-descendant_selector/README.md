# Descendant Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Descendant Selector merupakan selector untuk mencari tag HTML berdasarkan struktur antara hubungan parent-child. Istilah ini cukup sulit dipahami, namun ini cukup dapat dimengerti jika saya paham mengenai Document Object Model (DOM).

Contoh kode html yang memiliki struktur DOM adalah sebagai berikut.


```html
<div>
    <h1>Header 1 di dalam tag div</h1>
    <p><span>Span yang ada didalam paragraf.</span> Sebuah paragraf yang ada didalam tag div</p>
</div>
```

Perhatikan bahwa tag `<div>` merupakan induk (parent) element karena dia memiliki anak (child). Anak dari tag `<div>` bisa dilihat tuh ada banyak. `<h1>, <p>, <span>`.

Descendant selector berfungsi untuk cari tag HTML berdasarkan struktur tersebut. Untuk penggunaan-nya, setiap element yang akan di descendant harus dipisahkan dengan **spasi**. Contoh lengkap-nya seperti kode berikut ini.

```html
<h1>Belajar CSS</h1>
<p>Paragraf pertama</p>
    <div>
        <h2>Header 2 di dalam tag div</h2>
        <p><span>Span yang ada didalam paragraf.</span> Sebuah paragraf yang ada didalam tag div</p>
    </div>
<h2>Header 2 di luar tag div</h2>
```

```css
div h2 {
    color: red;
}
p span {
    color: blue;
}
body h1 {
    color: green;
}
```

Pahami kode css tersebut. Pada struktur HTML, saya membuat 2 buah header. 

Pertama, saya masukkan ke dalam tag `<div>`.
Kedua, saya tidak masukkan ke dalam tag `<div>`.

Ketika saya ingin style tag `<h2>` yang berada di dalam `<div>` maka saya bisa gunakan descendant selector. Cara ini cukup wajar karena jika tidak, maka `<h2>` yang berada diluar `<div>` akan terkena style juga. Selain itu, ada juga tag `<p> dan <span>` serta tag `<body> dan <h1>`.

Memang cukup rumit namun saya paham jika dilihat secara teliti.

> penulisan descendant selector dan element spesific selector terkadang cukup membingungkan bruh. Karena mereka berdua terpisah oleh spasi namun memiliki fungsi yang sangat berbeda sekali. Berikut contohnya.

```css
/* Ini merupakan Element Spesific Selector */
div.header {
    color: red;
}

/* Ini merupakan Descendant Selector */
div .header {
    color: red;
}
```