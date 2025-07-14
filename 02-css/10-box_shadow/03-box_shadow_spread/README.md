# Box Shadow Spread

Nilai ke empat pada property `box-shadow` diisi dengan spread. Berfungsi untuk mengatur seberapa jauh efek bayangan yang terjadi. Jika diberikan nilai negatif, maka bayangan akan lebih kecil daripada dimensi element.

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
.box1 {box-shadow: 10px 10px 10px 10px;}
.box2 {box-shadow: 10px 10px 10px 20px;}
.box3 {box-shadow: 10px 10px 10px -10px;}
.box4 {box-shadow: 20px 20px 10px -20px;}
```

Jika dijalankan, terlihat bahwa semakin tinggi nilai spread, maka semakin hilang pula efek bayangan karena efeknya kecil.

