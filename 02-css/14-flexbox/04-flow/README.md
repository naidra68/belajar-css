# Flex Flow

Property ini merupakan penulisan singkat dan gabungan dari 2 property yaitu `flex-direction` dan `flex-flow`. Alih-alih menulis satu persatu property, saya bisa gunakan ini untuk meringkas 2 property sekaligus.

berikut contoh penerapan-nya

```html
<div class="container flow1">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container flow2">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
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
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}

.flow1 {
    flex-flow: row wrap;
}
.flow2 {
    flex-flow: column-reverse nowrap;
}
```

