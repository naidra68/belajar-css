# :focus Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

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