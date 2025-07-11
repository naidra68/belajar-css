# Background Size

Property background-size merupakan property baru yang dikenalkan pada CSS3 waktu itu. Property ini berfungsi untuk emngatur ukuran gambar background.

Nilai dari property ini dapat di isi oleh semua satuan length seperti `px`, `em`, `%` dan bisa juga menggunakan keyword berupa `auto`, `contain`, dan `cover`.

Pada satuan length, property ini dapat di isi oleh 1 atau 2 nilai. Jika menggunakan 1 nilai maka yang diatur adalah lebar gambar tersebut, jika menggunakan 2 nilai maka yang diatur adalah lebar dan tinggi gambar tersebut.

# satuan length

berikut contoh penerapan-nya

```html
<!-- 1 nilai -->
<div class="satu"></div>
<!-- 2 nilai -->
<div class="dua"></div>
```

```css
div {
    width: 500px;
    height: 500px;
    border: 3px solid black;
    margin: 10px;
    background-image: url('../img/bluebeerry.png');
    background-repeat: no-repeat;
}

/* 1 Nilai */
.satu {background-size: 300px;}

/* 2 Nilai */
.dua {background-size: 250px 500px;}
```

Jika dijalankan, element ke dua yang memiliki 2 nilai akan terasa melebar atau stretching ke bawah. Ini terjadi karena element saya set `500px` dan `background-size` nya juga `500px`, sedangkan lebar nya setangah dari lebar element.

Itulah yang menjadikan element ke dua tampak melebar terpaksa menurut saya.

Apabila menggunakan percent, maka sedikit berbeda dengan pixel. Contoh diatas saya menggunakan pixel maka yang dihitung adalah lebar dan tinggi gambar, sedangkan jika menggunakan percent akan dihitung lebar dan tinggi element-nya.

berikut contoh penerapan-nya

```html
<div class="tiga"></div>
```

```css
.tiga {
    background-repeat: repeat;
    background-size: 50% 50%;
}
```

Jika dijalankan, gambar akan tampil sebanyak 4x untuk memenuhi element-nya. Saya gunakan `repeat` agar terlihat perbedaan antara percent dengan pixel.

# keyword

Efek menarik terjadi pada property ini jika saya menggunakan 2 nilai keyword yaitu `contain` dan `cover`.

Apabila menggunakan `contain`, maka web browser akan berusaha menampilkan gambar background itu utuh, namun tetap mempertahankan rasio gambar. Ketika ukuran gambar tidak pas terhadap element, maka akan terdapat sisa ruang kosong.

berikut contoh penerapan-nya

```html
<div class="empat"></div>
```

```css
/* contain */
.empat {
    width: 500px;
    height: 200px;
    background-image: url('../img/bluebarry100x100.png');
    background-size: contain;
}
```

Terlihat ada ruang sisa di sisi kanan gambar yang menandakan size akan ditampilkan sesuai rasio gambar.

Apabila menggunakan `cover`, maka web browser akan berusaha menampilkan gambar background utuh sampai menutupi element. Caranya dengan memperbedar gambar backround dan tetap mempertahankan rasio gambar. Hasilnya, akan terjadi potongan gambar yang tidak terlihat.

berikut contoh penerapan-nya

```html
<div class="lima"></div>
```

```css
/* contain */
.lima {
    width: 500px;
    height: 200px;
    background-image: url('../img/bluebarry100x100.png');
    background-size: cover;
}
```

Jika dijalankan, terlihat bahwa gambar background akan terpaksa direnggangkan hingga menutupi element. Terakhir, ada keyword `auto`. Ketika property ini di isi oleh satu nilai, proses yang sebenarnya terjadi adalah nilai kedua di isi oleh auto

contohnya

> background-size: 250px;

akan diproses menjadi

> background-size: 250px auto;