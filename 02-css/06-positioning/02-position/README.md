# Position

Pembahasan mengenai `position` sangat menarik dipahami, ketika sudah mempelajari mengenai cara kerja web browser menampilkan halaman web dengan normal document flow. Maka, agar element saya bisa keluar dari normal document flow tersebut harus menggunakan property `position`.

Nilai yang di isi adalah keyword seperti `static`, `relative`,`absolute`, `fixed`, dan `sticky`.

## Static

Nilai static merupakan default dari web browser apabila position tidak didefinisikan. Tanpa ditulis pun, halaman web yang dibuat sudah otomatis menggunakan nilai `static` untuk position.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1">Satu</div>
    <div class="box box2">Dua</div>
    <div class="box box3">Tiga</div>
</div>
```

```css
.container {
    width: 50%;
    height: 350px;
    background-color: grey;
    margin: 0 auto;
    margin-top: 2em;
}

.box {
    width: 100px;
    height: 100px;
    line-height: 100px;
    text-align: center;
    font-size: 1.2em;
    color: white;
}
.box1 {background-color: red;}
.box2 {background-color: green;}
.box3 {background-color: blue;}
```

## Relative

Isi dari `relative` ini digunakan untuk mengatur element agar bisa keluar dari document flow-nya. Biasanya `relative` digabungkan dengan `absolute` agar terjadi document flow parent child element.

Saat ini, saya akan coba secara terpisah terlebih dahulu agar saya semakin paham menggunakan `position` ini. Ketika menggunakan nilai `relative` maka harus ada property `top`,`bottom`,`left`,`right`.

Mengapa? Karena untuk mengatur element agar keluar adalah 4 property tersebut, meskipun 4 property tersebut tidak akan bekerja tanpa nilai `relative`. Seperti saling menguntungkan.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box4">Satu</div>
    <div class="box box5">Dua</div>
    <div class="box box6">Tiga</div>
</div>
```

```css
/* Relative */
.box4 {
    background-color: red;
    position: relative;
    left: 100px;
}
.box5 {
    background-color: green;
    position: relative;
    left: -100px;
}
.box6 {
    background-color: blue;
    position: relative;
    bottom: -50px;
}
```

Jika dijalankan, terlihat sedikit membingungkan, kenapa jika diset `left` malah element-nya bergeser ke `right`? Ini bisa terjadi karena sifat dari property tersebut.

Apabila saya set `left` dengan nilai positif maka dia akan bergeser ke arah `right`, namun berbeda jika saya set nilai negatif. Maka element akan bergeser ke arah `left`.

Ini berlaku untuk semua property seperti `right`,`top`, dan juga `bottom`. Jadi pastikan menggunakan property ini dengan tepat agar tidak salah perintah.

## Absolute

Sama seperti `relative`. Isi dari `absolutw` ini digunakan untuk mengatur element agar bisa keluar dari document flow-nya. Untuk mengatur juga saya butuh 4 property seperti pada `relative`.Namun ada sedikit perbedaan daripada `relative`.

berikut contoh penerpaan-nya

```html
<div class="container">
    <div class="box box7">Satu</div>
    <div class="box box8">Dua</div>
    <div class="box box9">Tiga</div>
</div>
```

```css
/* Absolute */
.box7 {
    background-color: purple;
    position: absolute;
    top: 0;
    left: 100px;
}
.box8 {
    background-color: orange;
    position: absolute;
    bottom: 0;
    right: 0;
}
.box9 {
    background-color: pink;
    position: absolute;
    left: 0;
    bottom: 0;
}
```

Jika dijalankan, terlihat bahwa ada sedikit berbedaan dengan `relative`. Menggunakan `absolute` maka yang terjadi adalah, jaraknya bukan bergantung pada parent element lagi namun sudah masuk ke jendela web browser (viewport).

Inilah mengapa, `relative` dan `absolute` biasanya digabung kedalam parent child element. Untuk parent element menggunakan `relative` agar patokan-nya pada element tersebut dan `absolute` untuk child element.

<hr>

berikut contoh penerapan-nya

```html
<div class="relative">
    <div class="absolute child1">Child Box1</div>
    <div class="absolute child2">Child box2</div>
    <div class="absolute child3">Child Box3</div>
</div>
```

```css
/* Relative and Absolute */

.relative {
    width: 80%;
    height: 400px;
    margin: 1.5em auto;
    background-color: dimgray;
    position: relative;
}

.absolute {
    width: 100px;
    height: 100px;
    line-height: 100px;
    text-align: center;
    position: absolute;
    color: white;
}

.child1 {
    background-color: red;
    top: 0;
    right: 0;
}
.child2 {
    background-color: green;
    bottom: 0;
    left: 100px;
}
.child3 {
    background-color: blue;
    top: 150px;
    left: 250px;
}
```

Jika dijalankan, terlihat bahwa ini tidak ada bedanya dengan isi dari `relative`. Namun, dengan cara seperti ini, saya dapat mengontrol posisi element agar lebih mudah dibaca.

Selain itu, jika menggunakan `relative` saja untuk mengontrol, apabila terdapat element bersarang (Element didalam element), maka hal tersebut cukup rumit di kontrol.

## Fixed

Sesuai namanya yaitu `fixed` (tetap). Apabila posisi element diberi `fixed`, maka tampilan dari element tersebut akan berpatokan pada jendela web browser (viewport).

berikut contoh penerapan-nya

```html
<!-- Fixed -->
<div class="container1">
    <div class="box box10">Satu</div>
    <div class="box box11">Dua</div>
    <div class="box box12">Tiga</div>
</div>
```

```css
/* fixed */

.container1 {
    width: 50%;
    height: 400px;
    background-color: grey;
    margin: 0 auto;
    margin-top: 2em;
}

.box10 {
    background-color: green;
    position: fixed;
    bottom: 0;
}
.box11 {
    background-color: lime;
}
.box12 {
    background-color: limegreen;
}
```

Ketika dijalankan, terlihat bahwa box pertama saya set posisi-nya menjadi `fixed` dengan property `bottom` 0, maka dia akan melayang di jendela web browser dari bawah ketika discroll.

Posisi `fixed` ini biasanya dipakai untuk navbar melayang yang biasanya terdapat di web-web luar sana.

<hr>

Saya coba membuat sebuah studi kasus sederhana. Saya ingin sebuah tag `<h1>` tampil melayang saat di scroll.

berikut contoh penerapan-nya

```html
<div class="fixed">
    <h1>Header1</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt quam saepe fuga dolor, earum eum, ipsa veniam iste libero, a possimus iure provident nisi dolores corrupti vitae repudiandae reprehenderit repellendus!</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga repudiandae accusamus adipisci cum illo deserunt necessitatibus quas assumenda, sequi inventore sit maiores dolore nisi sed, repellat amet iste tenetur odit.</p>
    <p>Totam quos sint et enim rem aperiam blanditiis veniam ex libero architecto, quia ratione velit! Maiores adipisci aspernatur nihil facilis, rerum, non sint, debitis cum sunt ab ratione asperiores laudantium.</p>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facere temporibus commodi ipsa corrupti? Magni iste rem eligendi vel iusto molestias, non saepe doloremque quidem molestiae cupiditate accusantium error nihil qui!</p>
    <p>Repellat provident quidem repudiandae rerum maxime beatae perspiciatis officiis minus! Perspiciatis velit repellendus error, accusantium recusandae non nostrum, officiis facere autem voluptatem reiciendis cum, sequi assumenda officia tenetur aperiam sint.</p>
    <p>Voluptatem velit asperiores ad fugit reprehenderit sequi vero non, nesciunt suscipit libero! Repellat ratione asperiores repudiandae ut sit vero blanditiis iure perspiciatis iste, perferendis nesciunt, optio a? Voluptatibus, ullam quos!</p>
    <p>Molestias exercitationem id consectetur, nihil odit ab, tempora mollitia accusamus ullam, rem aspernatur architecto corrupti? Quidem, maiores iure omnis nihil sint amet unde cum voluptate esse expedita dicta totam deleniti!</p>
</div>
```

```css
/* Fixed Study Case */

.fixed {
    width: 80%;
    height: 800px;
    background-color: dimgrey;
    margin: 0 auto;
}
h1 + p {
    padding: 1em;
    margin-top: 2em;
}
.fixed > p {
    padding: 1em;
}
.fixed > h1 {
    background-color: cyan;
    text-align: center;
    position: fixed;
    top: 0;
    width: 80%;
}
```

## Sticky

Sama seperti `fixed`, menggunakan `sticky` akan membuat element melayang pada jendela web browser (viewport). Namun, hanya ketika saya sudah melewati jendela browser tersebut.

Intinya gini, klo `fixed` itu melayang terus-terus an waktu pertama kali halaman web dimuat web browser. Sedangkan `sticky` itu hanya melayang ketika element yang diset tersebut akan dilewati oleh scrollbar.

Nilai dari `sticky` ini seperti gabungan dari nilai `static` dan `fixed`. Ketika pertama kali dimuat maka dia tampak `static`, namun ketika melewati element-nya, maka dia akan menjadi `fixed`.

berikut contoh penerapan-nya

```html
<div class="sticky">
    <h1 class="s-top">Belajar CSS</h1>
    <h2>Position Sticky</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum quam minus a omnis maxime mollitia velit, beatae voluptate tempora earum officiis nihil dolor? Doloribus dolorum recusandae consequuntur minus. Ab, maiores?</p>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur, necessitatibus non. Aliquid ut sequi optio suscipit amet consequuntur enim nesciunt, accusantium ea voluptates modi odit, quidem debitis possimus iste reiciendis!</p>
    <p>Quibusdam obcaecati voluptatem magni fuga illo id autem laboriosam nostrum quis voluptas culpa, quas dolorum quod a quidem, ut numquam dolores delectus nemo excepturi reprehenderit natus, ipsam molestias pariatur? Sint?</p>
    <p>Repellendus delectus explicabo deleniti ex itaque odio aut beatae tenetur eligendi. Est blanditiis nam enim consequatur eveniet eos nobis deleniti, consequuntur quos quam iste eaque praesentium nisi saepe explicabo libero.</p>
    <p>Perferendis deleniti illum placeat, optio earum minus. Iure, nobis quasi. Recusandae, quo nihil amet illum facere minima id ratione qui, aperiam molestias ad dolore. Temporibus deleniti a ipsa dolor illum.</p>
    <p>Commodi suscipit earum, qui neque animi libero accusamus necessitatibus odit laudantium. Similique suscipit velit et soluta, iure assumenda natus ratione, est consectetur, asperiores maxime delectus voluptates modi consequatur unde molestiae.</p>
    <p>In eum animi minus totam, sequi quisquam autem. Numquam fugit animi laboriosam eum esse. Similique quae, libero corporis voluptatum, aspernatur rerum, laborum quod necessitatibus cum adipisci doloribus quisquam alias nostrum.</p>
</div>
```

```css
/* Sticky */

.sticky {
    width: 80%;
    height: 1200px;
    background-color: dimgray;
    margin: 1em auto;
}
.s-top {
    text-align: center;
    background-color: aqua;
    margin-bottom: 2em;
}
h2 {
    text-align: center;
    background-color: red;
    position: sticky;
    top: 0;
}
```