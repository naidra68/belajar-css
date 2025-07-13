# Float

Property `float` digunakan untuk mengatur posisi sebuah element dan mencari cara utama (dulu-nya) mengatur layout sebuah web. Property ini memiliki 4 nilai seperti `none`, `left`, `rigth`, `inherit`.

- `none` berfungsi untuk menghapus efek property float.
- `left` berfungsi untuk mengatur posisi element ke kiri.
- `right` berfungsi untuk mengatur posisi element ke kanan.
- `inherit` berfungsi untuk mengikut property float parent element, konsep inheritance (pewarisan).

## Left

Seperti nama-nya, nilai ini akan mengatur posisi element ke sebelah kiri. Contoh paling jelas bisa terlihat ketika ada sebuah element inline.

berikut contoh penerapan-nya

```html
<div class="float-left">
    <h1>Semangka</h1>
    <img src="../img/fruit1.png">
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. In inventore obcaecati impedit possimus repellat aut id. Officiis autem culpa, voluptate laudantium, totam cum temporibus, sequi in natus fuga voluptatem expedita.</p>
</div>
```

```css
.float-left {
    margin: 1em;
}
.float-left > img {
    width: 200px;
    float: left;
    margin: 0 1em 1em 0;
    border: 1px solid black;
    padding: 0.5em;
}
```

Jika dijalankan, terlihat bahwa tulisan dari tag `<p>` akan tampil disebelah tag `<img>`. Padahal image merupakan element `inline` dan paragraf merupakan element `block`. Apabila terdapat `float` maka element dibawah `float` tersebut akan ikut berada di sisi kiri. Coba untuk hilangkan `float` pada image dan lihat perbedaan-nya.

## Right

Seperti nama-nya, nilai ini akan mengatur posisi element ke sebelah kanan.

berikut contoh penerapan-nya

```html
<div class="float-right">
    <h1>Semangka</h1>
    <img src="../img/fruit2.png">
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. In inventore obcaecati impedit possimus repellat aut id. Officiis autem culpa, voluptate laudantium, totam cum temporibus, sequi in natus fuga voluptatem expedita.</p>
</div>
```

```css
.float-right {
    margin: 1em;
}
.float-right > img {
    width: 200px;
    padding: 0.5em;
    border: 1px solid black;
    margin: 0 0 1em 1em;
    float: right;
}
```

Ketika dijalankan, terlihat bahwa posisi gambar akan ada disebelah kanan. Dengan pemahaman memahami property `float` ini, saya dapat membuat sebuah navbar dengan rapi.

<hr>

## Membuat Navbar Sederhana

Dari pemahaman mengenai property css sebelumnya ditambah property `float` akan membuat navbar tampak mudah.

berikut contoh penerapan-nya

```html
<ul>
    <li><a class="active" href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Project</a></li>
    <li><a href="#">Contact</a></li>
</ul>
```

```css
ul li {
    list-style: none;
    float: left;
}
ul li a {
    text-decoration: none;
    padding: 1em;
    background-color: slateblue;
    color: white;
}
ul li a:hover,
ul li a.active {
    background-color: red;
}
```

Jika dijalankan, saya berhasil membuat navbar sederhana. Sudah selesai seperti itu. Apabila saya lihat, mengapa lebar dari navbar-nya tidak full selayar? namun hanya pada tulisan-nya saja?

Biasanya ini membuat bingung, inilah yang disebut sebagai container collapse, dimana penampung-nya menghilang dan navbar hanya mengikuti konten-nya, lebar-nya akan bertambah apabila konten navbar-nya bertambah.

Untuk mengatasi hal ini, saya bisa menambahkan property `float` juga pada element container-nya yaitu pada tag `ul`.

```css
ul {
    float: left;
    width: 100%;
    padding: 1em 0;
    background-color: slateblue;
}
```

Jika dijalankan, navbar akan full memenuhi layar ke sebelah kanan, seperti navbar pada website sekarang ini. Menggunakan `float` untuk membuat navbar memang cukup menantang karena saya harus teliti agar tidak terjadi container collapse seperti tadi.

Ini adalah cara lama untuk membuat navbar menggunakan `float`. Sekarang ini pembuatan navbar bisa lebih mudah jika menggunakan **Flexbox** dan **Grid**.