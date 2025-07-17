# Flex

Property ini merupakan penulisan singkat shorthand notation dari `flex-basis`, `flex-grow`, dan `flex-shrink`. Property ini bisa diisi dengan 1,2 atay 3 nilai.

Jika menulis satu nilai tanpa satuan, maka yang di set adalah `flex-grow`. Jika menulis satu nilai dengan satuan seperti length, maka yang di set adalah `flex-basis`.

**flex grow**
- flex: 2;

**flex basis**
- flex: 20px;

Jika menulis dua nilai maka tinggal perhatikan nilai yang dimasukkan seperti apa.

**flex grow and flex basis**
- flex: 2 200px;

**flex basis and flex grow**
- flex: 200px 2;

Jika menulis dua nilai tanpa satuan maka :

**flex-grow and flex-shrink**
- flex: 2 1;
- flex: 3 2;

Jika menulis tiga nilai maka yang terjadi adalah `flex-grow`,`flex-shrink`, dan `flex-basis`.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box f-1">Box 1</div>
    <div class="box f-2">Box 2</div>
    <div class="box f-3">Box 3</div>
    <div class="box f-4">Box 4</div>
    <div class="box f-5">Box 5</div>
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

.f-1 {flex: none;}
.f-2 {flex: 0 1 auto;}
.f-3 {flex: 2 2;}
.f-4 {flex: 0 100px;}
.f-5 {flex: 1 4 200px;}
```
