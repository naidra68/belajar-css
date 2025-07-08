# Font Size

CSS menyediakan beragam satuan untuk mengatur ukuran font, yang semuanya di-set melalui property font-size.

contoh penggunaan

```html
<p>Paragraf pertama</p>
```

```css
p {
    font-size: 36px;
}
```

> jika tidak mendefinisikan ukuran font, maka teks secara default akan ditampilkan seebsar 16 pixel. Ini ukuran oleh web browser.

Property font-size dan berbagai property lain di dalam CSS butuh nilai dalam satuan length, yakni satuan 'panjang' seperti pixel, cm, mm, em, atau persen.

Secara garis besar, nilai satuan length dikategorikan ke dalam 2 kelompok: **nilai absolut** dan **nilai relatif**.

## Nilai Absolut

Nilai absolut (absolute-size) adalah satuan length yang nilainya tetap dan tidak terpengaruh oleh element di sekelilingnya. Contoh dari absolute-size adalah pixel (px), centimeter (cm), milimeter (mm), point (pt), inches (in) dan pica (pc).

contoh penerapan-nya

```html
<p class="px">Paragraf ukuran 24 pixel</p>
<p class="mm">Paragraf ukuran 12 milimeter</p>
<p class="cm">Paragraf ukuran 1,5 centimeter</p>
<p class="pt">Paragraf ukuran 18 point</p>
<p class="in">Paragraf ukuran 0,5 inci</p>
<p class="pc">Paragraf ukuran 2,2 pica</p>
```

```css
.px {font-size: 24px;}
.mm {font-size: 12mm;}
.cm {font-size: 1.5cm;}
.pt {font-size: 18pt;}
.in {font-size: 0.5in;}
.pc {font-size: 2.2pc;}
```


## Nilai Relatif

Selain nilai absolut, CSS juga menyediakan nilai relatif, seperti satuan persen (%), em dan rem. Sesuai dengan namanya, nilai relatif akan berubah-ubah tergantung posisi dan parent
element.


### Nilai Percent (%)

contoh penerapan-nya

```html
<p class="percent">paragraf ukuran 120%</p>
```

```css
.percent {
    font-size: 120%;
}
```

Untuk nilai percent, akan merujuk ke parent element, apabila parent element tidak didefinisikan font-size nya, dengan kata lain pakai default font-size web browser. Maka perhitungannya sebagai berikut

> 120% * 16 pixel = 19,2 pixel.

Nilai percent pada font-size dapat diakumulasikan ketika didefinisikan kepada element yang sama.

contoh penerapan-nya

```html
<div>Child Element 1
    <div>Child Element 2
        <div>Child Element 3
            <div>Child Element 4
            </div>
        </div>
    </div>
</div>
```

```css
body {
    font-size: 16px;
}
div {
    font-size: 110%;
}
```

Jika dijalankan, setiap tag `<div>` akan terakumulasi font-size nya. Karena saya definisikan font-size dari parent element yakni tag `<body>` maka, perhitungan pada ukuran terakhir tag `<div>` adalah sebagai berikut.

> 110% * 110% * 110% * 110% * 16px = 23.43px

Penting diperhatikan agar efek akumulasi seperti ini dapat dipertimbangkan lagi sebelum menggunakan satuan persen untuk font-size.


### Nilai Em

Satuan **em** berasal dari istilah typography media cetak yang merujuk kepada tinggi karakter `m` pada suatu font. Dalam CSS, nilai em sangat mirip seperti persen (%), dimana hasilnya juga dihitung berdasarkan nilai parent element.


contoh penerapan-nya

```html
<p class="em">Paragraf ukuran 1.1em</p>
```

```css
.em {
    font-size: 1.1em;
}
```

Sama seperti percent, nilai em dapat diakumulasikan kepada element yang sama.

contoh penerapan-nya

```html
<div>Child Element 1
    <div>Child Element 2
        <div>Child Element 3
            <div>Child Element 4
            </div>
        </div>
    </div>
</div>
```

```css
body {
    font-size: 16px;
}
div {
    font-size: 1.1em;
}
```

> Lalu, apa perbedaan antar `%` dan `em`?

> Kedua nilai ini tidak akan ada perbedaan jika dipakai untuk font-size. Satuan tersebut akan berbeda jika diterapkan pada property lain seperti menentukan lebar atau tinggi suatu element.

- Menggunakan `%` untuk mengatur lebar (width) element maka akan merujuk kepada lebar (width) parent element.
- Menggunakan `em` untuk mengatur lebar (width) element maka akan di hitung dari nilai font-size parent element.

### Nilai Rem

Rem merupakan singkatan dari "root em". Berbeda dengan satuan em yang tergantung kepada parent element, rem bergantung kepada 'root element', atau element akar.

Dalam struktur DOM HTML, yang dimaksud sebagai root element adalah tag `<html>`. Tag ini merupakan akar dari semua tag, termasuk tag `<body>`, `<div>` dan lain-lain.

Jika menggunakan referensi parent child, maka tag `<html>` ini bisa dibilang sebagai grant parent atau mbah (bahasa jawa). Istilah ini saya buat agar saya paham konteks-nya.

Karena merujuk pada root element, maka nilai Rem tidak akan diakumulasi. tidak peduli dimana element tersebut didefinisikan. Saya bisa melihat perbandingan-nya jika saya ubah ukuran tag `<html>` dan tag `<body>`.

```html
<p class="satu">paragraf ini ada didalam body</p>
<p class="dua">paragraf ini ada didalam body</p>
```

```css
html {
    font-size: 20px;
}
body {
    font-size: 16px;
}
.satu {
    font-size: 1em;
}
.dua {
    font-size: 1rem;
}
```

Ketika dijalankan, saya lihat sendiri perbandingan antara satuan `em` dan `rem` secara jelas jika tag `<html>` dan tag `<body>` memiliki font-size berbeda.

Paragraf dengan class selector `satu` di definisikan dengan satuan `em`. Jadi, dia merujuk kepada parent element yakni tag `<body>`.

Paragraf dengan class selector `dua` di definisikan dengan satuan `rem`. Jadi, dia merujuk kepada root element yakni tag `<html>`.


## Sebaiknya pakai?

Tergantung selera masing-masing, jika menggunakan pixel lebih mudah karena semua tutorial menggunakan itu ya silahkan atau jika menggunakan `em` karena lebih fleksible juga silahkan.

Saya menggunakan kedua-nya, pixel dan juga `em`. Untuk mobile ya saya gunakan `em` si karena web kompleks tidak hanya terpaku pada layar monitor, namun juga ada layar smartphone maka lebih fleksible menggunakan satuan `em`.