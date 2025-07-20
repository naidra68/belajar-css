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

Jika kode tersebut dijalankan, akan membuat semua tulisan berwarna merah. Mengapa hal ini terjadi? Jika di logika, seharusnya hanya warna pada tag `<body>` saja yang berubah warna-nya, namun semua element yang didalam tag `<body>` berubah semua warna-nya.

Ini bisa terjadi karena ada konsep inheritance (pewarisan), ingat bahwa struktur HTML diatas adalah sebuah struktur DOM. Dimana struktur DOM ini memiliki struktur data seperti pohon dan akar. Jadi, semua element yang berada di dalam tag `<body>` akan terkena style.

Bagaimana jika saya timpa warna-nya dengan mengubah warna pada element div? Jawaban-nya bisa, nantinya element div akan berubah warna.

berikut contoh penerapan-nya

```css
body {
    color: red;
}
div {
    color: blue;
}
```

Apabila dijalankan, semua element yang ada didalam `<div>` akan berubah warna menjadi biru, ini akan menimpa warna dari element `<body>`. Konsep cascading dan inheritance terpakai disini.


Contoh lain mengenai konsep cascading dan inheritance ini. Berikut contoh penerapan-nya.

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

Jika dijalankan, terlihat bahwa tag `<strong>` berubah warna menjadi biru, mengapa hal ini bisa terjadi? bukankah style terakhir yang harusnya menang? Jika mengacu pada konsep cascading (last rules apply).

Jawabannya adalah efek cascading yang telah digunakan sebelum-nya hanya berlaku jika selector element-nya sama. Seperti contoh, saya membuat selector body 2x, maka body yang terakhir lah yang menang.

Konsep ini penting untuk dipahami agar tidak kebingung jika memiliki masalah mengenai style css. Terkadang saat saya memberikan style pada element, biasanya tidak berefek atau tidak bisa di style. Ini bisa terjadi karena ada cascading yang timpa menimpa atau inheritance yang memiliki pewarisan pada element sebelumnya.