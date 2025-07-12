# Background Shorthand Notation

Setelah mengetahui banyak mengenai property `background`, sekarang saat-nya mencoba menggunakan property `background` dengan penulisan shorthand notation.

Property ini mencakup 8 property lain, diantara-nya.

- `background-image`
- `background-position`
- `background-size`
- `background-repeat`
- `background-attachment`
- `background-origin`
- `background-clip`
- `background-color`

berikut contoh penerapan-nya

```html
<div class="satu"></div>
```

```css
.satu {
    width: 960px;
    height: 500px;
    border: 3px solid black;
    margin: 0 auto;
    background: url('../img/jeruk.jpg') bottom left / 700px 400px no-repeat scroll padding-box content-box red;
}
```

Semua property akan ditampilkan menjadi satu ketika menggunakan property `background`. Penulisan seperti ini cukup ringkas jika dilihat, namun penulisan seperti ini terlalu beresiko jika saya tidak paham urutan dari penulisan property awal.

Apabila salah satu tidak ditulis, maka nilai yang tidak ditulis tersebut akan secara otomatis di set default oleh web browser.

Selain itu, ketika saya membuat property `background` dan dibawah property tersebut saya definisikan lagi property `background-color`, maka warna dari property `background` akan tertimpa oleh property `background-color`.