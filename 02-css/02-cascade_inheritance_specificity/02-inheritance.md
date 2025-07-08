# Inheritance

Inheritance atau dalam Bahasa Indonesia diartikan sebagai penurunan/pewarisan adalah konsep dimana sebuah style bisa diturunkan dari parent (induk) kepada child element (anak).


contoh penerapan-nya

```html
<h1>Belajar CSS</h1>
<p>Paragraf pertama</p>
<div>
    <h2>Header 2 didalam div</h2>
    <p>Paragraf pertama didalam div</p>
</div>
<div>
    <h3>Header 3 didalam div</h3>
    <p>Paragraf pertama didalam div</p>
</div>
```

```css
body {
    color: red;
}
```

Jika kode tersebut dijalankan, akan membuat semua tulisan berwarna hijau. Mengapa ini terjadi? 

Saya bedah struktur html-nya. Kalau dilihat dari logika, seharunya element yang berada didalam `<div>` tidak akan terkena style. Namun tetap kena. Itulah konsep inheritance atau penurunan.

Meskipun saya sudah mengelompokkan menjadi parent dan child, namun itu tidak bekerja karena element `<body>` akan menimpa semua-nya. Untuk mengetasi hal ini, saya bisa menimpa-nya dengan menambahkan element spesific setelah `<body>`.

contoh penerapan-nya

```css
body {
    color: red;
}
div {
    color: blue;
}
```

Apabila dijalankan, semua element yang ada didalam `<div>` akan berubah warna menjadi biru, ini akan menimpa warna dari element `<body>`. Konsep cascading dan inheritance terpakai disini.


Konsep ini cukup membuat bingung. Apalagi jika mempunyai kasus seperti contoh code berikut

```html
<h1>Belajar CSS</h1>
<p>Paragraf pertama</p>
<div>
    <h2>Header 2 didalam div</h2>
    <p><strong>Paragraf pertama</strong> didalam div</p>
</div>
```

```css
strong {color: blue;}
div {color: red;}
body {color: green;}
```

Jika dijalankan tampak normal, namun konsep ini tidak mencerminkan cascading. Seharusnya kan cascading memiliki aturan style paling terakhir menang. Seharusnya `<body>` akan menimpa semua-nya karena konsep cascading tersebut.

Namun. konsep cascading hanya berlaku jika menimpa element yang sama. Jika saya menimpa dengan element yang berbeda maka konsep inheritance yang akan digunakan.

Cukup membingungkan buat saya yang baru belajar, akan tetapi dengan begini saya mengerti kenapa kode css saya terkadang tidak berubah padahal sudah diganti. Ternyata konsep seperti ini cukup krusial.