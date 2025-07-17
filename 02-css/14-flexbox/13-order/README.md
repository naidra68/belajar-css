# Order

Property ini digunakan untuk mengatur urutan **child element (flex item)** satu dengan **child element (flex item)** lain. Nilai yang bisa diisi pada property ini berupa angka tanpa satuan dan bisa bernilai negatif. Nilai paling kecil akan berada di bagian awal **parent element (flex container)**.

berikut contoh penerapan-nya

```html
<h1>Row</h1>
<div class="container row">
    <div class="box">Box 1</div>
    <div class="box order-1">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container row">
    <div class="box order-3">Box 1</div>
    <div class="box order-1">Box 2</div>
    <div class="box order-2">Box 3</div>
</div>
<div class="container row">
    <div class="box">Box 1</div>
    <div class="box order-min-1">Box 2</div>
    <div class="box">Box 3</div>
</div>
<h1>Column</h1>
<div class="container column">
    <div class="box">Box 1</div>
    <div class="box order-1">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container column">
    <div class="box order-3">Box 1</div>
    <div class="box order-1">Box 2</div>
    <div class="box order-2">Box 3</div>
</div>
<div class="container column">
    <div class="box">Box 1</div>
    <div class="box order-min-1">Box 2</div>
    <div class="box">Box 3</div>
</div>
```

```css
.container {
    height: 150px;
    border: 2px solid #FF734F;
    background-color: #09A8C8;
    margin: 1em;
    display: flex;
}
.row {flex-direction: row;}
.column {flex-direction: column;}
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.order-1 {order: 1;}
.order-2 {order: 2;}
.order-3 {order: 3;}
.order-min-1 {order: -1;}
```

Jika dijalankan, terlihat bahwa setiap child element yang memiliki `order` akan berubah posisi atau bertukar posisi dari child element disebelahnya. Jika diisi nilai positif maka dia akan bertukar element arah kanan dan jika menggunakan nilai negatif maka dia akan bertukar element darah kiri.

