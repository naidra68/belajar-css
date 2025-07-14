# Transform Translate

Nilai dari `translate` dipakai untuk memindahkan posisi suatu element. Jika dilihat hasilnya nanti, nilai ini mirip seperti relative positioning.

Nilai yang di isi ada 2 yaitu `translateX` untuk memindahkan element secara horizontal dan `translateY` untuk memindahkan element secara vertical.

Untuk penulisan shorthand notation bisa menggunakan `translate` dan di isi dengan 2 nilai yaitu `translateX` dan `translateY`.

berikut contoh penerapan-nya

```html
<div class="box box1">Box 1</div>
<div class="box box2">Box 2</div>
<div class="box box3">Box 3</div>
<div class="box box4">Box 4</div>
<div class="box box5">Box 5</div>
```

```css
.box {
    width: 200px;
    height: 50px;
    background-color: green;
    float: left;
    margin: 1.5em;
    line-height: 50px;
    text-align: center;
    color: white;
}
.box1 {transform: translate(0);}
.box2 {transform: translateX(20px);}
.box3 {transform: translateY(30px);}
.box4 {transform: translateX(50px) translateY(30px);}
.box5 {transform: translate(30px, 50px);}
```

Ketika dijalankan, terlihat bahwa mencoba semua fungsi translate mulai dari horizontal dan vertical serta penggunaan translate shorthand notation.

<hr>

Dengan menggabungkan property `transform` dan pseudo element selector `:hover` akan menciptakan button atau element yang bisa memiliki efek menarik untuk interaksi pengguna.

berikut contoh penerapan-nya

```html
<div class="box box6">Click Me</div>
```

```css
.box6:hover {
    transform: translate(50px);
}
```

Ketika dijalankan, terlihat jika mensorot element tersebut akan membuat element itu pindah posisi.