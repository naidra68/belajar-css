# Cursor

Property ini berfungsi untuk mengubah tampilan cursor mouse saat berada di atas sebuah element. Nilai yang bisa diisi cukup beragam, diantaranya `default`, `pointer`, `help`, `wait`, `not-allowed` dan `crosshair`.

berikut contoh penerapan-nya

```html
<div class="cursor default">Default</div>
<div class="cursor pointer">Pointer</div>
<div class="cursor help">Help</div>
<div class="cursor wait">Wait</div>
<div class="cursor notallowed">Notallowed</div>
<div class="cursor crosshair">Crosshair</div>
```

```css
body {
    display: flex;
    padding: 1em;
}
.cursor {
    width: 100px;
    height: 50px;
    border: 2px solid;
    background-color: magenta;
    margin-right: 1em;
    display: flex;
    justify-content: center;
    align-items: center;
}
.default {cursor: default;}
.pointer {cursor: pointer;}
.help {cursor: help;}
.wait {cursor: wait;}
.notallowed {cursor: not-allowed;}
.crosshair {cursor: crosshair;}
```