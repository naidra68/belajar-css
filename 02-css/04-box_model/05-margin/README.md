# Margin

Lapisan terluar atau terakhir dari Box Model adalah `margin`. Margin merupakan sebuah property yang berfungsi sebagai pemisah antar element.

Contohnya seperti ini, saya memiliki 2 element yang telah di style dengan property lain. Namun saat dilihat, 2 element tersebut tampak menyatu. Tampak tidak ada space diantar 2 element tersebut.

Untuk menyelesaikan masalah ini, property `margin` adalah solusinya.

Sama seperti penulisan `padding` yang memiliki 2 notasi penlisan, `margin` juga dapat ditulis dengan Longhand Notation dan Shorthand Notation.

## Longhand Notation

Sama seperti `padding`, terdapat 4 arah yang dapat ditulis.

- margin-top
- margin-bottom
- margin-left
- margin-right

Untuk mengingatnya, biasanya saya gunakan jarum jam dan TRouBLe.

berikut contoh penerapan-nya

```html
<div class="satu m"></div>
<div class="dua m"></div>
<div class="tiga m"></div>
```

```css
* {
    padding: 0;
    margin: 0;
}

.m {
    width: 100px;
    height: 100px;
    background-color: green;
    text-align: center;
}
.satu {
    margin-top: 20px;
    margin-left: 40px;
    margin-bottom: 20px;
}

.dua {
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 60px;
    margin-left: 80px;
}

.tiga {
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 0px;
    margin-left: 120px;
}
```

Saya memakai universal selector digunakan sebagai mereset `padding` dan `margin` bawaan dari web browser. Memberikan style juga pada tag `div` agar tidak menulis kode berulang kali.

Jika dijalankan, terlihat bahwa 3 element `<div>` akan akan berpindah ke sebelah sisi kanan dan memiliki space antar element. Mengggunakan penulisan longhand cukup membantu jika tidak ingin ribet dengan penggunaan shorthand.

## Shorthand Notaion

Dengan penulisan ini menulis `margin` cukup ringkas. Saya bisa membuat kode seperti diatas dengan sedikit lebih rapi dan ringkas.

berikut contoh penerapan-nya

```html
<div class="empat m"></div>
<div class="lima m"></div>
<div class="enam m"></div>
```

```css
.empat {margin: 20px 40px;}
.lima {margin: 0 0 60px 80px;}
.enam {margin: 0 0 0 120px;}
```

Jika dijalankan, hasilnya sama persis seperti menggunakan longhand. Lebih ringkas dan gampang di maintain, yang terpenting hafal arah jarum jam atau dengan kalimat TRouBLe


## Mengenal Margin Collapse

Mungkin ini cukup sulit jika tanpa melihat langsung perbedaan-nya dengan cara ngoding. Margin Collapse seperti intruksi web browser agar menggugurkan salah satu arah margin jika terdapat dua element dengan margin yang sama.

berikut contoh penerapan-nya

```html
<div class="pertama mc"></div>
<div class="kedua mc"></div>
```

```css
.mc {
    width: 200px;
    height: 50px;
    background-color: aqua;
    text-align: center;
}
.pertama {margin: 20px;}
.kedua {margin: 20px;}
```

Ketika dijalankan, berjalan dengan normal dan tidak terjadi apa-apa. Namun jika diteliti lagi, seharus-nya class `.pertama` memiliki `margin bottom: 20px` dan class `.kedua` memiliki `margin top: 20px`. Jika ditambah maka harusnya menjadi `40px`. Tapi yang terjadi mengapa hanya `20px`?

Inilah yang disebut sebagai margin collapse. Hanya ada 1 nilai yang dipakai jika ada 2 nilai yang memiliki nilai sama.

Pada web browser, margin collapse memiliki aturan apabila sebuah element memiliki margin yang lebih besar daripada margin element lain, maka yang dipakai adalah element dengan margin terbesar.

berikut contoh penerapan-nya

```html
<div class="ketiga mc">Ketiga</div>
<div class="keempat mc">Keempat</div>
```

```css
.ketiga {margin-bottom: 20px;}
.keempat {margin-top: 40px;}
```

Jika dijalankan, akan terlihat perbedaan-nya, jarak antara kedua element tersebut sebesar `40px` yang seharusnya adalah `60px`. Namun karena adanya margin collapse maka margin terbesar lah pemenang-nya yaitu `40px`.


## Horizontal Centering

Salah satu keunikan margin yang selalu dipakai oleh developers dan programmer untuk membuat element menjadi ditengah posisi secara horizontal adalah `margin auto`.

Nilai auto pada margin akan memberikan instruksi kepada web browser bahwa hitung secara otomatis nilai-nya. `margin auto` sama seperti `margin 0`. 

Terdapat perilaku khusus jika suatu element memiliki width, jika ada `margin auto`, maka akan mengambil sisa lebar yang tersedia. Dengan memberikan nilai auto pada margin arah kiri dan kanan maka sisa ruang-nya akan dibagi sama besar. Hasilnya, element tersebut berada tepat di tengah (center).

berikut contoh penerapan-nya

```html
<div class="tujuh ma"></div>
```

```css
.ma {
    width: 80%;
    height: 300px;
    border: 1px solid black;
}

.tujuh {margin: 0 auto;}
```

Jika dijalankan, akan nampak bahwa element tersebut akan tepat berada di tengah secara horizontal, ini terjadi karena jika saya definisikan `margin` maka.

- nilai pertama adalah `0` akan merujuk ke arah atas dan bawah. 
- nilai kedua adalah `auto` akan merujuk ke arah kiri dan kanan.


Perbedaan dengan `text-align:center`?

Untuk menyingkat penjelasan, maka lihat list berikut.

- ingin mengatur **element** maka gunakan `margin: 0 auto`.
- ingin mengatur **teks** maka gunakan `text-align:center`.