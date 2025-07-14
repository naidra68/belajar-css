# Border Image Source

Property ini berfungsi untuk menentukan letak lokasi gamba border-nya. Isi dari property ini sama seperti `background-image` yang menggunakan `url()`.

berikut contoh penerapan-nya

```html
<div class="border-image-source"></div>
```

```css
.border-image-source {
    width: 200px;
    height: 200px;
    background-color: red;
    margin: 1em auto;
    border: 40px solid transparent;
    border-image-source: url('../img/border1.png');
}
```

Jika dijalankan, terlihat bahwa gambar border-nya akan tampil sebanyak 4 kali dengan ukuran 40px. Kenapa tidak tampil secara merata dipinggir seperti `border` kebanyakan?

Untuk melakukan hal itu ada property lain yang harus ditambahkan setelah saya menampilkan gambar border-nya.