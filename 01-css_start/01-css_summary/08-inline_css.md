# Inline CSS

cara paling mudah untuk menerapkan css adalah dengan cara menulis langsung dalam document html menggunakan atribute style.

contoh :
```html
<h1 style="color: red">Belajar CSS dasar</h1>
```

Apabila menulis 2 property atau lebih maka gunakan titik koma pada akhir value.

contoh :
```html
<h1 style="color: red; font-size: 24px;">Belajar CSS dasar</h1>
```

berikut penerapan dalam document html.

```html
<html>
    <head>Belajar CSS</head>
<body>
    <h1 style="color: red;">Belajar CSS Dasar</h1>
    <h1 style="color: red; font-size: 23px;">Belajar CSS Dasar</h1>
</body>
</html
```

Walaupun cara ini terkesan mudah dan gampang, namun cara penulisan seperti ini tidak direkomendasikan karena css tercampur pada html. Hal ini sangat bermasalah ketika kode html saya sudah banyak. Jika kode saya sudah banyak dan saya ingin mengubah warna maka saya ubah satu-prrsatu. Hal tersebut cukup merepotkan.