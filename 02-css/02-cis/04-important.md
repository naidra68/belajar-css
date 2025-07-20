# !important

Ketika sudah mempelajari mengenai specificity, saya memahami bahwa nilai dari `Id Selector` memiliki prioritas tertinggi. Namun, ada satu senjata pamungkas developer web dan programmer yang paling ampun untuk mengalahkan prioritas tertinggi, yaitu perintah `!important`.

`!important` adalah keyword sakti jika saya mengalami masalah dengan selector maupun property CSS yang tidak berjalan sesuai keinginan saya. Dengan menambah perintah `!important`, sebuah property CSS akan memiliki prioritas paling tinggi dan hanya bisa dikalahkan oleh perintah `!important` lain yang lebih spesifik.

berikut contoh penerapan-nya

```html
<p class="paragraf" id="paragrafPertama">Tebak warna paragraf</p>
```

```css
#paragrafPertama {color: red;}
.paragraf {color: blue;}
p {color: green;}
```

Jika dijalankan, terlihat bahwa code diatas tanpa menggunakan `!important`. Maka pemenangnya sudah pasti `id selector`. Namun gimana jika saya tambahkan `!important` diakhir element selector?

berikut contoh penerapan-nya

```html
<p class="paragraf" id="paragrafPertama">Tebak warna paragraf</p>
```

```css
#paragrafPertama {color: red;}
.paragraf {color: blue;}
p {color: green !important;}
```

Jika dijalankan, terlihat bahwa warna-nya akan berubah menjadi hijau. Menggunakan keywoard `!important` diakhir penulisan warna akan memenangkan nilai element selector.

Apabila di logika, nilai specificity dari `!important` ini sepertinya sebesar **99999**, mungkin? karena betapa hebatnya `!important` dapat mengalahkan semua selector.

Namun, jangan terlalu nyaman dengan `!important` karena membuat logic tidak bekerja dan hanya ingin hasil instant jika terdapat masalah mengenai CSS. Gunakan `!important` jika memang tidak ada pilihan lain selain itu.