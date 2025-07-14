# Box Shadow Inset

Nilai ini digunakan untuk mengatur bayangan agar tampil berada didalam element. Penulisan keyword `inset` ini harus ditulis diawal penulisan nilai `box-shadow`.

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
.box1 {box-shadow: inset 5px 5px red;}
.box2 {box-shadow: inset 10px 10px 3px;}
.box3 {box-shadow: inset 10px 5px 5px 2px rgba(255,88,75,0.8);}
.box4 {box-shadow: inset 7px 7px 3px 2px hsl(100,100%,50%);}
```

Ketika dijalankan, terlihat bahwa `box-shadow` akan tampil pada kiri atas sebuah element, ini menandakan bahwa `box-shadow` berada didalam element tersebut.