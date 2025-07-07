# External CSS

Cara penulisan ini sangat direkomendasikan karena saya memisahkan style css dan document html menjadi file terpisah. Untuk menggunakan external css terdapat 2 cara yaitu menggunakan tag `<link>` atau `@import`.

### buat dan isi style.css
```css
h1 {
    color: red;
}
h2 {
    color: blue;
}
```

### Tag Link
```html
<html>
    <head>Belajar CSS</head>
    <link rel="stylesheet" href="style.css">
<body>
    <h1>Belajar CSS Dasar</h1>
    <h2>Belajar CSS Dasar</h2>
</body>
</html>
```

### @import
```html
<html>
    <head>Belajar CSS</head>
    <style>
        @import url("style.css");
    </style>
<body>
    <h1>Belajar CSS Dasar</h1>
    <h2>Belajar CSS Dasar</h2>
</body>
</html>
```

Namun, mayoritas developers sekarang memilih menggunakan tag `<link>` daripada `@import`. Alasannya? web browser memproses tag `<link>` lebih efisien ketimbang `@import`.