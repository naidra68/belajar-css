# Counter()

Fungsi `counter()` ini digunakan untuk mengembalikan nilai tulisan kedalam sebuah element. Sebagai contoh, bagaimana membuat sebuah tag `<li>` namun tidak menggunakan tag tersebut, namun menggunakan tag `<p>`.

Hal ini bisa dilakukan jika menggunakan fungsi `counter()`.

berikut contoh penerapan-nya

```html
<h4>Cara membuat telor Ceplok :</h4>
<p>Siapkan telur, minyak, bumbu masako.</p>
<p>Panaskan minyak ke wajan sampai panas.</p>
<p>Masukkan telur ke dalam wajan.</p>
<p>Berikan bumbu masako diatas telur ceplok.</p>
<p>Balik telur ceplok agar matang merata.</p>
<p>Setelah selesai, siap disajikan.</p>
```

```css
p::before {
    content: counter(urut) ". ";
}
p {
    counter-increment: urut;
}
```

Jika dijalankan, terlihat bahwa tag `<p>` akan berperilaku seperti tag `<li>`, dimana memiliki nomer urut. Saya menggunakan pseudo element `::before` untuk menambahkan nomer urutnya berada di arah depan.

Property `counter-increment` digunakan untuk membuat nomor sesuai isian dari property tersebut. Apabila di isi oleh nama argumen dari fungsi `counter()`, maka dia akan menghitung sesuai element tag-nya.