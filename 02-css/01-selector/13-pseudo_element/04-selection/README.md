# ::Selection

Pseudo element ini dipakai untuk mengakses selection pada sebuah element. Default dari web browser biasanya selection berwarna latar biru dan warna teks putih.

Dengan menggunakan pseudo element ini, saya dapat mengubah style warna bawaan-nya.

berikut contoh penerapan-nya

```html
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe ea delectus enim quaerat, ipsum dignissimos ratione iure nisi, velit, consequatur accusantium quod asperiores autem doloremque voluptate pariatur molestiae consequuntur iusto!</p>
```

```css
p::selection {
    background-color: black;
    color: white;
}
```

Jika dijalankan, terlihat bahwa tag `<p>` akan memiliki selection yang telah didefinisikan, saya menggunakan element spesific agar terjadi pada tag `<p>` saja. Jika ingin menerapkan pada global value maka bisa saja.

berikut contoh penerapan-nya

```css
::selection {
    background-color: black;
    color: white;
}
```