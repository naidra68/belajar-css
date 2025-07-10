# Border

Lapisan ketiga adalah garis tepi `border`. Secara default, garis tepi dan konten akan menempel satu sama lain jika tidak terdapat padding pada element konten tersebut.

Untuk isi dari `border` sama halnya dengan padding, saya bisa menulis semua property nya dari segala arah atau bisa juga dengan penulisan shorthand notation.

Pada property `border` ada istilah longhand notation, penulisan seperti itu digunakan ketika saya ingin menampilkan border secara detail dan berbeda-beda style di setiap arah. Sebelum masuk ke dalam penulisan shorthand notation, saya akan gunakan longhand notation terlebih dahulu.

## Longhand Notation

Untuk penulisan longhand notation, ada 3 aspek dari sebuah border yaitu : **width**, **style**, dan **color**.

1. `border width` digunakan untuk mengatur ketebalan border, nilai nya bisa di isi dengan satuan length seperti `px`,`em`,`rem`.
2. `border style` digunakan untuk mengatur jenis border, nilai-nya menggunakan keyword seperti `solid`,`dotted`,`dashed`,`double`,`groove`,`ridge`,`inset`, dan `outset`.
3. `border color` sigunakan untuk mengatur warna border, nilai-nya bisa menggunakan keyword warna,rgb dan lain-lain.

berikut contoh penerapan-nya

```html
<div class="satu"></div>
```

```css
.satu {
    border-top-width: 5px;
    border-top-style: solid;
    border-top-color: red;

    border-bottom-width: 10px;
    border-bottom-style: dotted;
    border-bottom-color: blue;

    border-left-width: 15px;
    border-left-style: solid;
    border-left-color: green;

    border-right-width: 5px;
    border-right-style: dashed;
    border-right-color: orange;
}
```

Terlihat cukup banyak, memang cara ini jarang dipakai karena biasa-nya border akan tampil sama pada semua arah. Namun, jika saya ingin border tampil dengan style berbeda-beda pada setiap arah. Maka cara ini sangat cocok untuk melakukan hal itu.

## Shorthand Notation

Penulisan dengan shorthand Notation ini lebih sedikit daripada menulis seperti tadi. Namun tetap, penulisan seperti ini digunakan untuk mengatur tiap arah.

berikut contoh penerapan-nya

```html
<div class="dua"></div>
```

```css
.dua {
    border-top: 5px solid red;
    border-bottom: 10px dotted blue;
    border-left: 15px solid green;
    border-right: 5px dashed orange;
}
```

Hasilnya akan sama seperti penulisan longhand notation, terlihat lebih singkat dan ringkas.

Apabila saya ingin membuat border secara beragam pada setiap posisi maka penulisan-nya akan lebih ringkas yaitu menggunakan property `border`.

```html
<div class="tiga"></div>
```

```css
.tiga {
    border: 5px dotted purple;
}
```

## Border Style

Penggunaan border style cukup menarik jika dibuat pada semua arah.

berikut contoh penerapan-nya

```html
<div class="bs-1 bs"></div>
<div class="bs-2 bs"></div>
<div class="bs-3 bs"></div>
<div class="bs-4 bs"></div>
<div class="bs-5 bs"></div>
<div class="bs-6 bs"></div>
<div class="bs-7 bs"></div>
<div class="bs-8 bs"></div>
<div class="bs-9 bs"></div>
```

```css
.bs {
    width: 100px;
    height: 100px;
    float: left;
    margin: 10px;
}

.bs-1 {border: 6px solid black;}
.bs-2 {border: 6px dashed black;}
.bs-3 {border: 6px dotted black;}
.bs-4 {border: 6px double black;}
.bs-5 {border: 6px groove black;}
.bs-6 {border: 6px ridge black;}
.bs-7 {border: 6px inset black;}
.bs-8 {border: 6px outset black;}
```

Jika dijalankan, akan menampilkan semua border style dalam berbagai style. Saya tambahkan `float: left` dan `margin` agar tampilan bisa lebih rapi berjejer.


# Border Radius

Pernah melihat situs web yang memiliki tombol berbentuk bulat? atau tampak bulat di sisi kiri dan kanan? Jika pernah, maka untuk membuat sesuatu seperti itu menggunakan property `border-radius`. Property ini dikenalkan waktu CSS3 rilis.

Sama seperti border, terdapat 2 cara penulisan untuk property ini, bisa menggunakan Longhand Notation dan Shorthand Notation.

## Longhand Notation

Karena berurusan dengan sudut (corner) maka penulisan harus diperhatikan arahnya. Terdapat 4 sudut yang bisa digunakan.

- border-top-left-radius
- border-top-right-radius
- border-bottom-right-radius
- border-bottom-left-radius

berikut contoh penerapan-nya

```html
<div class="br-1 br">Box1</div>
<div class="br-2 br">Box2</div>
```

```css
.br {
    width: 200px;
    height: 200px;
    border: 4px solid red;
    float: left;
    margin: 10px;
    line-height: 200px;
    text-align: center;
}

.br-1 {
    border-top-left-radius: 10px;
    border-top-right-radius: 20px;
    border-bottom-right-radius: 30px;
    border-bottom-left-radius: 40px;
}
.br-2 {
    border-top-left-radius: 1em;
    border-top-right-radius: 2em;
    border-bottom-right-radius: 3em;
    border-bottom-left-radius: 4em;
}
```

Jika dijalankan, saya akan melihat jika sudut border akan ditampilkan berbeda sesuai nilai yang dimasukkan kedalam property tersebut.

## Shorthand Notation

Penulisan Longhand memang cukup banyak dan terkesan detail. Untuk penulisan shorthand akan lebih ringkan namun cukup sulit dipahami waktu pertama kali belajar.

Penulisan ini memiliki 4 nilai yang bisa di isi, sama seperti penulisan shorthand dari property `padding`. Saya bisa memakai penjelasan pada `padding` untuk menentukan penulisan-nya.

berikut contoh penerapan-nya

```html
<div class="br-3 br1">Box3</div>
<div class="br-4 br1">Box4</div>
<div class="br-5 br1">Box5</div>
<div class="br-6 br1">Box6</div>
```

```css
.br1 {
    width: 100px;
    height: 100px;
    line-height: 100px;
    margin: 10px;
    float: left;
    background-color: black;
    color: white;
    text-align: center;
}

.br-3 {border-radius: 20px;}
.br-4 {border-radius: 10px 20px;}
.br-5 {border-radius: 10px 20px 30px;}
.br-6 {border-radius: 10px 20px 30px 40px;}
```

Jika dijalankan, terlihat bahwa semua isi akan menyesuaikan apa yang telah di defisinikan. Penjelasan mengani border-radius sangat penting dipahami jika ingin membuat button atau element yang memiliki sudut bulat.