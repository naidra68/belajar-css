# Background Position

Property ini berfungsi untuk mengatur posisi background, nilai yang bisa di isi oleh property ini semua satuan length seperti `px`, `em`, `%` dan keyword seperti `top`, `bottom`, `right`, `left`, dan `center`.

Apabila gambar terlalu besar daripada element-nya, maka `background-position` tidak akan terasa efek-nya.

Untuk isi dari property nya ada 2 posisi, `posisi sumbu x` dan `posisi sumbu y`. 2 Posisi dipisah dengan spasi.


# nilai pixel (px)

berikut contoh penerapan-nya

```html
<div class="satu"></div>
```

```css
div {
    width: 500px;
    height: 250px;
    border: 3px solid black;
    margin: 0 auto;
    background-image: url('../img/kiwi100x100.png');
    background-repeat: no-repeat;
}

.satu {background-position: 200px 60px;}
```

Jika dijalankan, terlihat bahwa gambar pada tag `<div>` akan berpindah tempat.

# nilai percent (%)

berikut contoh penerapan-nya

```html
<div class="dua"></div>
```

```css
.dua {background-position: 70% 20%;}
```

Jika dijalankan, terlihat bahwa gambar pada tag `<div>` akan berpindah tempat, dengan nilai percent akan lebih responsive.

# nilai keyword

berikut contoh penerapan-nya

```html
<div class="tiga"></div>
```

```css
.tiga {background-position: center center;}
```

Jika dijalankan, terlihat bahwa menggunakan nilai keyword akan membuat gambar tersebut lebih presisi disetiap sisi-nya. Dengan `center center` maka terlihat bahwa gambarnya akan tampil ditengah-tengah element.

<hr>

Ada beberapa hal yang harus dipahami jika memakai property ini, nilai dari property `background-position` ditulis dalam satu nilai, maka nilai kesatu akan diset pada sumbu x dan sumbu y secara otomatis akan diset menjadi `center`.

Selain itu, terdapat 3 dan 4 nilai yang bisa di isi pada property ini. Semua nilai ini berbeda-beda penjelasan dan hasilnya.

berikut contoh penerapan-nya

```html
<div class="empat"></div>
<div class="lima"></div>
```

```css
/* 3 Nilai */
.empat {background-position: right 60px bottom;}
/* 4 Nilai */
.lima {background-position: right 20px top 50px;}
```

Pahami kode tersebut, jika dijalankan terlihat perbedaan yang cukup membingungkan. Apabila ditulis 3 nilai maka penjelasan sebagai berikut.

> ubah posisi gambar background 60 px dari kanan (right), dan berada di bagian bawah (bottom)

Apabila ditulis 4 nilai maka penjelasan sebagai berikut.

> ubah posisi gambar abckground 20 px dari kanan dan 50px dari atas.


# Background Position CSS3

Pada CSS3, background-position dapat digunakan untuk menempatkan lebih dari satu gambar untuk background, seperti background-image. Apabila terdapat beberapa gambar, maka setiap gambar dapat diatur posisinya secara terpisah.

berikut contoh penerapan-nya

```html
<div class="enam"></div>
```

```css
.enam {
    background-image: url('../img/jeruk100x100.png'),
                        url('../img/strawberry100x100.png'),
                        url('../img/bluebarry100x100.png');
    background-position: right bottom, 50% 0%, left bottom;
}
```

Jika dijalankan, terlihat bahwa setiap gambar memiliki posisi yang berbeda-beda.