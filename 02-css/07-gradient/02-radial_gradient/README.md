# Radial Gradient

Radial Gradient adalah efek gradiasi yang berbentuk lingkaran dan elips.

berikut contoh penerapan-nya

```html
<div class="radial-gradient">
    <div class="box box1">Box 1</div>
</div>
```

```css
.radial-gradient {
    width: 80%;
    height: 300px;
    background: dimgray;
    margin: 1em auto;
}
.box {
    width: 150px;
    height: 150px;
    line-height: 150px;
    text-align: center;
    font-size: 1.3em;
}
.box1 {
    background-image: radial-gradient(white, red);
}
```

Jika dijalankan, terlihat bahwa nilai default dari radial gradient ini adalah berbentuk elips. Untuk membuat bentuk lain seperti lingkaran, maka perlu menambahkan keterangan diawal nilai.

berikut contoh penerapan-nya

```html
<div class="radial-gradient">
    <div class="box box2">Box 1</div>
    <div class="box box3">Box 2</div>
</div>
```

```css
.box2 {
    background-image: radial-gradient(circle, white, green);
}
.box3 {
    background-image: radial-gradient(ellipse, white, green);
}
```

Jika dijalankan, terlihat perbedaan antara circle dan ellipse. Pada contoh tidak terlihat karena lebar yang saya set kurang, untuk melihatnya bisa mengganti lebar element-nya menjadi 600px.

## Radial Position

Secara default, titik lingkaran gradient berada tepat ditengah element. Untuk mengubah titik lingkaran ini bisa diatur dengan posisi menggunakan keyword atau satuan length.

berikut contoh penerapan-nya

```html
<div class="radial-gradient1">
    <div class="box box4">Box 1</div>
    <div class="box box5">Box 2</div>
    <div class="box box6">Box 3</div>
    <div class="box box7">Box 4</div>
    <div class="box box8">Box 5</div>
    <div class="box box9">Box 6</div>
</div>
```

```css
.box4 {background-image: radial-gradient(circle at 100% 50%, red, yellow);}
.box5 {background-image: radial-gradient(ellipse at 100% 50%, red, yellow);}
.box6 {background-image: radial-gradient(circle at 100px 150px, red, yellow);}
.box7 {background-image: radial-gradient(ellipse at bottom right, blue, cyan);}
.box8 {background-image: radial-gradient(circle at top left, blue, cyan);}
.box9 {background-image: radial-gradient(ellipse at bottom left, blue, cyan);}
```

Ketika dijalankan, terlihat bahwa untuk mengatur posisi perlu keyword `at` setelah menuliskan bentuk apa yang dipilih, dilanjut dengan posisi yang akan ditentukan dengan satuan length atau keyword.

## Radial Extends

Radial Extends adalah istilah yang merujuk seberapa jauh batas lingkaran gradient yang akan ditetapkan. Untuk mengaturnya dengan cara menambahkan jarak tepat setelah memilih bentuk yang dipilih. Satuan length yang bisa dipakai seperti `px`,`em`,`rem`.

berikut contoh penerapan-nya

```html
<div class="radial-gradient">
    <div class="box box10">Box 1</div>
    <div class="box box11">Box 2</div>
    <div class="box box12">Box 3</div>
</div>
```

```css
.box10 {background-image: radial-gradient(circle 2rem, red, green);}
.box11 {background-image: radial-gradient(circle 4em, red, green);}
.box12 {background-image: radial-gradient(circle 100px, red, green);}
```

Jika dijalankan, terlihat bahwa titik lingkaran akan terset sesuai isi yang di definisikan. Cara ini untuk mengatur titik lebar atau tinggi lingkaran.

## Radial Stop

Radial Stop sama seperti Linear Stop, dimana sebuah warna dapat ditentukan kapan berhenti atau bergabung dengan warna lain.

berikut contoh penerapan-nya

```html
<div class="radial-gradient">
    <div class="box box13">Box 1</div>
    <div class="box box14">Box 2</div>
    <div class="box box15">Box 3</div>
    <div class="box box16">Box 4</div>
</div>
```

```css
.box13 {background-image: radial-gradient(circle 100px at 90% 90%, black, cyan, black);}
.box14 {background-image: radial-gradient(circle 100px at 10% 90%, black, cyan, black);}
.box15 {background-image: radial-gradient(circle 100px at 90% 10%, black, cyan, black);}
.box16 {background-image: radial-gradient(circle 100px at 10% 10%, black, cyan, black);}
```

Ketika dijalankan, terlihat bahwa saya membuat sebuah bentuk yang unik menggunakan radial stop ini dengan penambahan extend dan position.

## Radial Repeat

Efek terakhir adalah repeat, sama seperti repeat linear untuk mengulang bentuk radial. Namun pada kasus radial, ini terkesan cukup rumit karena bentuknya sudah bukan linear lagi, namun sudah radial.

berikut contoh penerapan-nya

```html
<div class="radial-gradient">
    <div class="box box17">Box 1</div>
    <div class="box box18">Box 2</div>
    <div class="box box19">Box 3</div>
    <div class="box box20">Box 4</div>
</div>
```

```css
.box17 {background-image: repeating-radial-gradient(circle, white,red 20%);}
.box18 {background-image: repeating-radial-gradient(circle at right top, white,red 10%, white 15%);}
.box19 {background-image: repeating-radial-gradient(circle at left, red,red 10px,white 15px);}
.box20 {background-image: repeating-radial-gradient(circle, red,white 1px, red 2px);}
```