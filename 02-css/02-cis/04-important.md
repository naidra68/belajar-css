# !important

Apabila melihat dari specificity, id selector memiliki nilai yang paling tertinggi daripada lain.

Namun, ada satu senjata pamungkas developers dan programmer yang muak dengan css, yaitu perintah `!important`.

!important adalah keyword sakti jika saya mengalami masalah dengan selector maupun property CSS yang tidak berjalan sesuai keinginan. Dengan
menambah perintah !important, sebuah property CSS akan memiliki prioritas paling tinggi dan hanya bisa dikalahkan oleh perintah !important lain yang lebih spesifik.


berikut contoh kasus-nya

```html
<p class="paragraf" id="paragrafPertama">Tebak warna paragraf</p>
```

```css
#paragrafPertama {color: red;}
.paragraf {color: blue;}
p {color: green;}
```

Jika tanpa menggunakan `!important` maka pemenangnya sudah pasti id_selector. Namun gimana jika saya tambahkan `!important` diakhir element selector?

berikut contoh code-nya
```html
<p class="paragraf" id="paragrafPertama">Tebak warna paragraf</p>
```

```css
#paragrafPertama {color: red;}
.paragraf {color: blue;}
p {color: green !important;}
```

Jika kode diatas dijalankan, sudah pasti yang menang adalah element selector dengan important.

Nilai specificity dari `!important` ini sebesar 99999, mungkin? karena betapa hebatnya `!important` dapat mengalahkan semua selector.


Namun, jangan terlalu nyaman dengan `!important` karena membuat logic tidak bekerja dan hanya ingin hasil instant jika terdapat masalah mengenai CSS. Gunakan `!important` jika memang tidak ada pilihan lain selain itu.