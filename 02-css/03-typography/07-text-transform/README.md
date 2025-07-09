# Text Transform

Property ini berfungsi untuk mengatur penulisan huruf pada teks element maupun paragraf. Property ini memiliki isi yang beragam.

- capitalize
- uppercase
- lowercase
- none

`capitalize` berguna jika ingin kata pertama disetiap teks akan menjadi huruf besar.

`uppercase` berguna jika ingin semua huruf disetiap teks menjadi huruf besar.

`lowercase` berguna jika ingin semua huruf disetiap teks menjadi huruf kecil.

`none` merupakan nilai default jika text-transfrom tidak didefinisikan.

berikut contoh penerapan-nya

```html
<p class="satu">paragraf pertama</p>
<p class="dua">paragraf kedua</p>
<p class="tiga">PARAGRAF KETIGA</p>
<p class="empat">paragraf keempat</p>
```

```css
.satu {text-transform: capitalize;}
.dua {text-transform: uppercase;}
.tiga {text-transform: lowercase;}
.empat {text-transform: none;}
```

Jika dilihat struktur HTML, saya menuliskan teks dalam huruf kecil semua kecuali paragraf ketiga. Perbedaan akan terlihat dimasing-masing class kecuali `none`.