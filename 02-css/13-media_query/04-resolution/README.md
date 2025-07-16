# Resolution

Pernah berpikiran bagaimana website non responsive tetap tampil bagus di layar smartphone yang beresolusi tinggi? Jawabannya karena perangkat ini menggunakan teknik device pixel ratio.

**Device pixel ratio (DPR)** adalah perbandingan yang dipakai perangkat beresolusi tinggi agar pixel di dalam CSS bisa tampil dengan ukuran normal.

Permasalahan muncul ketika menggunakan gambar, pixel ratio
bisa membuat gambar terlihat kabur di perangkat beresolusi tinggi. Oleh karena itu, css menyediakan `media query : resolution`.

Resolution merupakan konsep media query untuk mengatur style yang akan dipakai untuk perangkat beresolusi tinggi. Terdapat beragam satuan yang bisa digunakan, salah satunya adalah dots per pixel yang disingkat menjadi dppx.

berikut contoh code-nya

```css
div {
    background-image: url('logo.jpg');
}
@media (min-resolution: 2dppx) {
    div {
        background-image: url('logo_HD.jpg');
    }
}
```

Informasi ini memang terasa kurang relevan dan terasa kompleks bagi developer. Ini hanya sebagai informasi bagaimana web browser bekerja untuk menampilkan website sebaik-baiknya untuk perangkat desktop maupun smartphone.