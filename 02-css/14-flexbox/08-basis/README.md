# Flex Basis

Property ini digunakan untuk mengatur lebar atau tinggi dasar dari child element (flex item). Nilai yang dapat diisi berupa satuan length seperti px,em,% dan nilai keyword auto,content.

Apabila element yang di set dengan flex-basis memiliki nilai lebar atau tinggi, maka nilai tersebut akan ditimpa oleh flex-basis.

berikut contoh penerapan-nya

```html
<h1>Row</h1>
<div class="container row">
    <div class="box w-100 fb-0">Box 1</div>
    <div class="box w-100 fb-200">Box 2</div>
    <div class="box w-100 fb-300">Box 3</div>
    <div class="box w-100 fb-content">Box 4</div>
    <div class="box w-100 fb-auto">Box 5</div>
</div>
<h1>Column</h1>
<div class="container column">
    <div class="box h-100 fb-0">Box 1</div>
    <div class="box h-100 fb-200">Box 2</div>
    <div class="box h-100 fb-300">Box 3</div>
    <div class="box h-100 fb-content">Box 4</div>
    <div class="box h-100 fb-auto">Box 5</div>
</div>
```

```css
.container {
    border: 2px solid #FF734F;
    background-color: #09A8C8;
    margin: 1em;
    display: flex;
}
.row {flex-direction: row;}
.column {flex-direction: column;}
.w-100 {width: 100px;}
.h-100 {height: 100px;}
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.fb-0 {flex-basis: 0;}
.fb-200 {flex-basis: 200px;}
.fb-300 {flex-basis: 300px;}
.fb-content {flex-basis: content;}
.fb-auto {flex-basis: auto;}
```

Jika dijalankan, terlihat bahwa untuk direction row, maka lebar box element akan tertimpa yang tadinya 100px akan menjadi berbeda-beda sesuai isian dari `flex-basis`. Sedangkan untuk direction column, maka tinggi box elemenet akan tertimpa yang tadinya 100px akan menjadi berbeda-ebda sesuai isian dari `flex-basis`.