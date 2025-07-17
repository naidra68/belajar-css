# Flex Wrap

Property ini berguna untuk menentukan apakah **child element (flex item)** akan membuat baris baru jika **parent element (flex container)** tidak cukup lebar. Nilai yang bisa diisi adalah `nowrap` (default), atau `wrap`.

Property `flex-wrap` hanya berfek jika **parent element (flex container)** di set dengan `row` atau `row-reverse` saja dan akan diabaikan jika di set sebagai `column` atau `column-reverse`.

berikut contoh penerapan-nya

```html
<div class="container nowrap">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
</div>
<div class="container wrap">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
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
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.nowrap {
    flex-flow: nowrap;
}
.wrap {
    flex-flow: wrap;
}
```

Jika dijalankan, terlihat bahwa dengan menambahkan `wrap` akan menjadikan child element responsive dan membuat baris baru jika parent element tidak muat menampung child element terakhir.

Untuk melihat perbedaan ini, silahkan gunakan **developer tools** untuk uji responsive atau gunakan extension **Responsive View**.