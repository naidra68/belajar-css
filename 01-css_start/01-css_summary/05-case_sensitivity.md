# Case Sensitivity

Case Sensitivity merupakan bahasan apakah sebuah bahasa membedakan penulisan huruf kecil atau huruf besar. CSS bersifat case-insensitive, jadi penulisan huruf kecil atau huruf besar tidak akan berpengaruh.

```css
p {
    font-size: 28px;
}
p {
    FoNt-sIzE: 28Px;
}
```

```html
<html>
    <head>Belajar CSS</head>
    <style>
        .belajar {
            color: red;
        }
    </style>
<body>
    <h1 class="belajar">Belajar CSS Dasar</h1>
    <h1 class="Belajar">Belajar CSS Dasar</h1>
</body>
</html>
```