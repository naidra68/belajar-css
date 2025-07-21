# Border Collapse

Property ini berfungsi untuk menyatukan `border` yang saling bersentuhan. Biasanya dipakai ketika men-style tabel HTML menggunakan property `border`. Sebagai contoh, ketika menggunakan property `border` pada semua tag mulai dari `<table>`,`<th>`, `<td>`. Maka, border dari tag `<table>` akan bersentuhan dengan tag `<th>` dan `<td>`.

berikut contoh-nya

```html
<table class="normal">
    <tr><th>Header A</th><th>Header B</th></tr>
    <tr><td>Item A</td><td>Item A</td></tr>
    <tr><td>Item B</td><td>Item B</td></tr>
</table>
```

```css
.normal, .normal th, .normal td {
    border: 1px solid;
}
```

Jika dijalankan, terlihat bahwa terdapat `border` pada tag `<th>` dan `<td>` akan terdapat jarak dengan `border` dari tag `<table>`. Ketika menambahkan property border-collapse, maka border pada semua tag akan saling bersentuhan dan tampak lebih rapi.

berikut contoh penerapan-nya

```css
.normal, .normal th, .normal td {
    border: 1px solid;
    padding: 1rem;
    border-collapse: collapse;
}
```

Jika dijalankan, terlihat bahwa border pada table HTML tersebut akan lebih rapi dan enak untuk dilihat, saya tambahkan `padding` agar terlihat ada jaraknya antar border dan konten.