# :First Child and :Last Child Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Selector :first-child dan :last-child dipakai untuk mencari anak
pertama (first child) dan anak terakhir (last child) dari struktur DOM. Umumnya selector ini digunakan bersama element spesific selector untuk menentukan tag HTML yang akan dicari.

berikut contoh penerapan-nya.

```css
li:first-child {
    background-color: red;
}
li:last-child {
    background-color: green;
}
```

Perhatikan bahwa penulisan selector ini tidak boleh ada spasi antara nama element dengan pseudo selector. Jika dijalankan, setiap tag li yang akan di style hanya pada list pertama dan terakhir saja.

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

paragraf bukanlah berada pada urutan pertama atau anak pertama dari tag `<div>`. Yang jadi anak pertama adalah tag `<h2>`. Itulah mengapa, pada kode berikut ini baru tampil.

```html
<div>
    <p>Paragraf pertama didalam tag div</p>
    <p>Paragraf kedua didalam tag div</p>
</div>
```

Karena paragraf pertama adalah anak pertama dari tag `<div>`. 

Memang melihat penjelasan mengenai parent child ini cukup membingungkan. Namun saya yakin, dengan semakin banyak berlatih maka penjelasan seperti ini akan cepat dipahami.