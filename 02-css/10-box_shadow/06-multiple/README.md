# Multiple Box Shadow

Cara untuk membuat lebih dari 1 efek bayangan dapat dilakukan. Caranya adalah dengan membuat `box-shadow` memiliki 2 nilai yang dipisahkan dengan koma `,`.

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
.box1 {box-shadow: 10px 10px red,
                    20px 20px blue;}
.box2 {box-shadow: inset 10px 10px 10px,
                    inset -10px -10px 10px;}
.box3 {box-shadow: inset 7px 7px 3px hsl(100,100%,50%),
                    inset -7px -7px 3px hsl(150,100%,50%);}
.box4 {box-shadow: 5px 5px, -5px -5px;}
```

Ketika dijalankan, terlihat bahwa saya membuat 2 tumpukan `box-shadow` pada element dan memisahkan-nya dengan koma untuk membedakan nilai pertama dan nilai selanjutnya.