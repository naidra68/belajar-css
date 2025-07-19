# :focus Selector

Selector :focus akan aktif jika sebuah element HTML di-fokuskan. Selector ini lebih cocok digunakan pada tag `<input>` pada pengisian form.

berikut contoh penerapan-nya.

```html
<form action="" method="get">
    <p><input type="text" name="nama"></p>
    <p><input type="text" name="umur"></p>
</form>
```

```css
input:focus {
    border: 2px solid red;
    outline: none;
}
```

Jika dijalankan, maka inputan akan berubah style-nya ketika disorot atau ketika user akan mengetikkan sesuatu di inputan.