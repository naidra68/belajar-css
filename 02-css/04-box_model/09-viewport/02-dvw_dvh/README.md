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