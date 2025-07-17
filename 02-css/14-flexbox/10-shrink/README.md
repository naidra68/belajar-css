# Flex Shrink

Property ini merupakan kembalikan dari `flex-grow`. Property flex-shrink berfungsi untuk menentukan skala pengecilan pada **child element (flex item)**.  Property ini akan berfungsi apabila parent element memiliki lebar atau tinggi. Nilai yang dapat diisi oleh property ini adalah angka tanpa satuan seperti 1,2,3, dst.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box">Box 1</div>
    <div class="box fs-1">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container">
    <div class="box">Box 1</div>
    <div class="box fs-2">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container">
    <div class="box">Box 1</div>
    <div class="box fs-3">Box 2</div>
    <div class="box fs-2">Box 3</div>
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
.box {
    width: 300px;
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.fs-1 {flex-shrink: 1;}
.fs-2 {flex-shrink: 2;}
.fs-3 {flex-shrink: 3;}
```

Jika dijalankan, terlihat apabila jendela web browser diperkecil maka property ini akan terlihat perbedaan-nya. Silahkan coba dengan developer tools atau extension responsive viewer.