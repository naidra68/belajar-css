# Media type

media type merupakan teknik menampilkan style CSS dengan tampilan menyesuaikan media itu sendiri. Terdapat 9 nilai media yang di dukung, yakni: all, aural, braille,handheld, projection, print, screen, tty, dan tv. Namun, dari 9 itu yang selalu dipakai hanyalah 2 yaitu all (device) dan print (printer).

### buat dan isi style.css
```css
h1 {
    color: red;
}
h2 {
    color: red;
}
```

### buat dan isi print.css
```css
h1 {
    color: blue;
}
h2 {
    color: blue;
}
```

### tag link
```html
<html>
    <head>Belajar CSS</head>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="print.css">
<body>
    <h1>Belajar CSS Dasar</h1>
    <h2>Belajar CSS Dasar</h2>
</body>
</html>
```

### @media
```html
<html>
    <head>Belajar CSS</head>
    <style>
        /* style untuk device */
        @media screen {
            h1 {
                color: red;
                }
            h2 {
                color: red;
                }
        }
        @media print {
            h1 {
                color: blue;
                }
            h2 {
                color: blue;
                }
        }
    </style>
<body>
    <h1>Belajar CSS Dasar</h1>
    <h2>Belajar CSS Dasar</h2>
</body>
</html>
```