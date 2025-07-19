# :First Child and :Last Child Selector

Selector `:first-child` dan `:last-child` dipakai untuk mencari anak pertama (first child) dan anak terakhir (last child) dari struktur DOM HTML. Umumnya selector ini digunakan bersama element spesific selector untuk menentukan tag HTML yang akan dicari.

berikut contoh penerapan-nya.
```html
<ul>
    <li>List 1</li>
    <li>List 2</li>
    <li>List 3</li>
    <li>List 4</li>
    <li>List 5</li>
</ul>
```

```css
li:first-child {
    background-color: red;
}
li:last-child {
    background-color: green;
}
```

Jika dijalankan, terlihat bahwa tag `<li>` pertama dan tag `<li>` terakhir memiliki style warna. Penulisan ini tidak boleh ada spasi diantar element spesific dan pseudo class.

Bagaimana kalau saya ubah struktur html nya dan lihatlah apa yang terjadi jika saya menggunakan struktur html dan css dibawah ini :

```html
<div>
    <h2>header 1 didalam tag div</h2>
    <p>paragraf didalam tag div</p>
</div>
<div>
    <p>Paragraf pertama didalam tag div</p>
    <p>Paragraf kedua didalam tag div</p>
</div>
```

```css
p:first-child {
    color: red;
}
```

Mengapa hanya paragraf ditengah yang hanya terkena style? bukannya tadi first child itu harus di urutan pertama? Jika saya berpikir demikian, itu hal yang wajar karena baru belajar. Saya cek kembali struktur HTML nya dan lihat apa yang terjadi?

Ternyata, kode dibawah ini

```html
<div>
   <h2>header 1 didalam tag div</h2>
   <p>paragraf didalam tag div</p>
</div>
```

Paragraf bukanlah berada pada urutan pertama atau anak pertama dari tag `<div>`. Yang jadi anak pertama adalah tag `<h2>`. Itulah mengapa pseudo class ini tidak berfungsi.

Bagaimana jika struktur html nya seperti ini :

```html
<div>
    <p>Paragraf pertama didalam tag div</p>
    <p>Paragraf kedua didalam tag div</p>
</div>
```

Jika dijalankan, terlihat bahwa hanya tag `<p>` pertama saja yang akan diberikan style dan tag `<p>` setelahnya tidak mendapatkan style. Jika diperhatikan, pseudo class ini mirip seperti adjacent selector, bukan? memang mirip. Jadi perbedaan-nya ada dimana?

Menurut google, Perbedaan utama antara pseudo-class `:first-child` dan adjacent sibling selector (`+`) dalam CSS terletak pada bagaimana mereka memilih element.

`:first-child` memilih anak pertama dari induknya, tanpa memandang jenis element-nya. Sedangkan adjacent selector memilih elemen yang tepat mengikuti elemen lain dengan jenis yang sama. 

Jika dipahami, memang sangat membingungkan, namun akan terlihat gampang jika mencoba melihat perbedaan-nya secara langsung dan berlatih menggunakan selector dan pseudo class tersebut.