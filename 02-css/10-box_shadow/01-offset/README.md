# Box Shadow Offset

Nilai untuk membuat efek bayangan adalah offset-x dan offset-y. Kedua nilai ini berfungsi untuk mengatur besar dan lokasi bayangan. Nilai yang bisa diinput berupa angka positif maupun negatif dengan satuan width (px, em, %, dll).

Untuk offset-x, jika bernilai positif maka bayangan akan berada di sisi kanan element. Jika diisi angka negatif, bayangan akan berada di sisi kiri element.

Untuk offset-y, jika bernilai positif maka bayangan akan berada di sisi bawah element. Jika diisi angka negatif, bayangan akan berada di sisi atas element.

berikut contoh penerapan-nya

```html
<div class="box box1"></div>
<div class="box box2"></div>
<div class="box box3"></div>
<div class="box box4"></div>
```

```css
.box {
    width: 200px;
    height: 200px;
    background-color: green;
    float: left;
    margin: 1.5em;
}
.box1 {box-shadow: 5px 5px;}
.box2 {box-shadow: 20px 20px;}
.box3 {box-shadow: -8px -10px;}
.box4 {box-shadow: -15px 20px;}
```

Jika dijalankan, terlihat bahwa saya membuat beberapa box shadow dengan nilai offset positif dan negatif. Hasilnya akan berbeda-beda tiap box.

