# Transform Rotate

Nilai dari Rotate digunakan untuk memutar element dengan sudut tertenu. Nilainya berupa satuan sudut (angle unit). Satuan sudut berupa `degree(deg)`, `gradian(grads)`, `radian(rad)`, dan `turn`. Dari keempat nilai yang telah diketahui, paling sering digunakan adalah `degree(deg)`.

Saya akan membuatnya dengan sudut `degree(deg)` karena didukung oleh web browser secara luas.

```html
<div class="container">
    <div class="box box1">Box 1</div>
    <div class="box box2">Box 2</div>
    <div class="box box3">Box 3</div>
    <div class="box box4">Box 4</div>
</div>
```

```css
.container {
    background-color: dimgray;
    width: 80%;
    height: 400px;
    margin: 1em auto;
}

.box {
    width: 200px;
    height: 50px;
    background-color: green;
    float: left;
    margin: 2em;
    line-height: 50px;
    text-align: center;
    color: white;
}
.box1 {transform: rotate(0deg);}
.box2 {transform: rotate(15deg);}
.box3 {transform: rotate(-30deg);}
.box4 {transform: rotate(-90deg);}
```

Jika dijalankan, terlihat bahwa element-nya akan berubah sesuai sudut yang telah didefinisikan. Efek rotate ini titik pusat-nya berada di tengah-tengah element tersebut.

# Transform Origin

Untk mengubah titik pusat ini, terdapat property tambahan yang disandingkan dengan property `transform` ini yaitu property `transform-origin`.

Dengan menggunakan property tersebut, maka saya bisa mengatur titik pusat nya dimulai dari mana.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box5">Box 1</div>
    <div class="box box6">Box 2</div>
    <div class="box box7">Box 3</div>
    <div class="box box8">Box 4</div>
</div>
```

```css
.box5 {transform: rotate(0deg);}
.box6 {
    transform: rotate(15deg);
    transform-origin: left top;
}
.box7 {
    transform: rotate(15deg);
    transform-origin: left bottom;
}
.box8 {
    transform: rotate(45deg);
    transform-origin: left bottom;
}
```

Jika dijalankan, terlihat tidak ada perbedaan dengan rotate biasa. Namun yang sebenarnya terjadi, pusat rotasi element telah berubah tergantung nilai property `transform-origin`.

