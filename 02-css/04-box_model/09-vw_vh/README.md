# vw and vh

Satuan yang sering digunakan saat ini untuk mengisi lebar dan tinggi konten adalah `vw` (viewport width) dan `vh` (viewport height).

Viewport merujuk ke jendela tampilan web browser. satuan Viewport ini sama seperti satuan `%` yang merujuk ke persentase, namun perbedaan pada cara pengukuran-nya.

Viewport akan marujuk ke jendela web browser, sedangkan persentage akan merujuk ke parent element.

Perbedaan ini sama seperti perbedaan antara satuan `em` dan satuan `rem`.

berikut contoh penerapan-nya

```html
<div class="satu">Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia possimus, rerum unde quod eveniet eaque maxime tenetur exercitationem modi architecto assumenda blanditiis saepe itaque aperiam molestiae veniam. Non, quae incidunt.</div>
```

```css
.satu {
    width: 80vw;
    height: 90vh;
    background-color: aqua;
    padding: 0.2em;
}
```

Jika dijalankan, akan tampil ukuran sesuai lebar jendela web browser dan ketika diperkecil ataupun diperbesar akan sama seperti itu.

Saat ini, satuan viewport terdapat upgrade terbaru yaitu `dvw` (dynamic view width) dan `dvh` (dybamic view height).


# dvw and dvh

Sama seperti satuan viewport, namun lebih dinamis. Perbedaan dari satuan viewport ini tidak terlalu berefek jika dilihat dalam desktop ataupun tablet, namun akan ber efek ketika sudah masuk responsive mobile device.

Pada mobile device, terkadang aplikasi browser menampilkan url bar dan juga navbar bawaan dari browser. Hal ini tidak fleksible jika menggunakan satuan viewport, karena tampilan tidak akan konsisten.

Maka dari itu, untuk menghilagkan kelemahan itu, terciptalah dynamic viewport.

berikut contoh penerapan-nya.

```html
<div class="dua">Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia possimus, rerum unde quod eveniet eaque maxime tenetur exercitationem modi architecto assumenda blanditiis saepe itaque aperiam molestiae veniam. Non, quae incidunt.</div>
```

```css
.dua {
    width: 80dvw;
    height: 90dvh;
    background-color: aqua;
    padding: 0.2em;
}
```

Jika dijalankan, tidak terasa perubahan-nya. Namun ini penting untuk perangkat mobile, karena saat ini mayoritas web dapat diakses dengan smartphone maka perlu dipertimbahkan untuk memakai satuan viewport ini.

<hr>

Saat ini, penggunaan dynamic viewport menjadi pertimbangan baru untuk menyajikan web dalam bentuk perangkat mobile. Karena web harus dinamis bisa diakses dimana saja, maka itu menjadi tantangan tersendiri oleh developers dan programmer.