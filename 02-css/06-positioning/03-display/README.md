# Display

Property ini digunakan untuk mengatur tampilan dari sebuah element. Nilai dari property ini sangat banyak, namun saya akan memakai yang cukup sering dipakai oleh developers dan programmer saja.

- `none`
- `inline`
- `block`
- `inline-block`

## None

Nilai ini digunakan untuk menyembunyikan element seolah element tersebut tidak pernah ada.

berikut contoh penerapan-nya

```html
<div class="box box1">Box1</div>
<div class="box box2">Box2</div>
```

```css
.box {
    width: 100px;
    height: 100px;
    margin: 1em;
    line-height: 100px;
    text-align: center;
    font-size: 1.5em;
}
.box1 {
    background-color: aqua;
    display: none;
}
.box2 {
    background-color: magenta;
}
```

Ketika dijalankan, terlihat bahwa element box 1 tidak akan terlihat pada document html. Biasanya, nilai ini akan dipakai ketika ingin maanipulasi element untuk responsive design.

## Inline

Nilai dari `inline` digunakan untuk manipulasi display sebuah element menjadi *Inline Level Element*. Ketika mengetahui bahwa tag html memiliki **Block Level Element** dan **Inline Level ELement** dan setiap 2 hal tersebut dijelaskan perbedaan sikap-nya, maka saya bisa manipulasi element tersebut.

Apabila sebuah element adalah block element dan saya ingin mengubahnya menjadi inline element, maka saya bisa gunakan nilai `inline` untuk mengubahnya.

berikut contoh penerapan-nya

```html
<div class="inline">
    <h1>Header 1</h1>
    <p>Paragraf 1</p>
    <div>Sebuah div</div>
    <ul>
        <li>List 1</li>
        <li>List 2</li>
        <li>List 3</li>
    </ul>
</div>
```

```css
.inline * {
    display: inline;
}
```

Jika dijalankan, terlihat bahwa semua element html yang memiliki **Block Level Element** akan diubah menjadi **Inline Level Element**.

## Block

Kebalikan dari nilai `inline`. Nilai dari `block` akan menjadikan sebuah element html yang tadinya **Inline Level Element** akan menjadi **Block Level Element**.

```html
<div class="block">
    <span>Sebuah Span</span>
    <Strong>Teks Tebal</Strong>
    <i>Teks Miring</i>
</div>
```

```css
.block * {
    display: block;
}
```

Jika dijalankan, semua element html yang memiliki **Inline Level Element** akan menjadi **Block Level Element**.

## Inline Block

Nilai dari `inline-block` cukup menarik dilihat. Ketika menggunakan nilai ini maka sebuah element akan menjadi `inline` namun masih ada ciri khas dari `block`, dimana element bisa diberikan property `width` dan `height`.

Seperti yang saya tau bahwa element `inline` tidak dapat diberikan lebar dan tinggi element sedangkan `block` bisa.

```html
<div class="inline-block">
    <span>Teks Inline Block</span>
</div>
```

```css
.inline-block > span {
    display: inline-block;
    width: 200px;
    height: 200px;
    background-color: lime;
}
```

Jika dijalankan, terlihat bahwa element tersebut bisa diberikan lebar dan tinggi element. Apabila ingin sebuah element menjadi `inline`, namun tetap bisa diberikan lebar dan tinggi. Maka solusinya menggunkaan `inline-block`.


