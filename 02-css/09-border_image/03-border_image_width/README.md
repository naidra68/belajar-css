# Border Image Width

Property ini digunakan untuk menentukan lebar dari gambar border. Nilai yang bisa diinput berupa satuan length seperti pixel dan persen.

berikut contoh penerapan-nya

```html
<div class="box box1"></div>
```

```css
.box1 {
    border-image-source: url('../img/border1.png');
    border-image-slice: 33;
    border-image-width: 70px;
}
```

Jika dijalankan, terlihat bahwa ukuran dari border gambar-nya membessar sesuai isi dari lebar-nya. Sebaiknya atur lebar gambar sesuai tebal border agar terlihat sama disemua sisi, namun untuk menghasilkan efek yang berbeda dapat mengaturnya berbeda.

