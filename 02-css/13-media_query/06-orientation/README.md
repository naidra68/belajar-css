# Orientation

Pada perangkat smartphone dan tablet, terdapat 2 model tampilan: **portrait** dan **landscape**.

**Portrait** adalah ketika perangkat tersebut memiliki tinggi yang lebih besar daripada lebarnya. Sedangkan **Landscape** adalah ketika lebar perangkat lebih lebar daripada tingginya.

CSS juga mengakomodasi penggunaan media query berdasarkan apakah halaman tampil pada posisi portrait atau landscape.

berikut contoh penerapan-nya

```html
<div class="box"></div>
```

```css
.box {
    width: 300px;
    height: 100px;
    margin: 0 auto;
}

@media (orientation: portrait) {
    .box {
        background-color: green;
    }
}
@media (orientation: landscape) {
    .box {
        background-color: blue;
    }
}
```

Jika dijalankan, terlihat yang tampil adalah warna biru karena saya menggunakan laptop, dimana laptop itu mode-nya landscape.

Uniknya, dengan menggunakan device semacam desktop ataupun laptop. Maka saya tinggal mengecilkan atau memperbesar jendela web browser untuk mengetahui apakah layar itu landscape ataupun portrait. Untuk melihat perbedaan lebih jelas, bisa menggunakan layar smarthone