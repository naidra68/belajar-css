# Specificity Selector

Konsep terakhir untuk menyelesaikan 'pertentangan antar selector' adalah specificity.

Specificity merupakan metode perhitungan nilai untuk menentukan selector mana yang akan didahulukan.

Sesuai dengan namanya, semakin spesifik atau semakin detail sebuah selector, akan semakin tinggi nilainya.

berikut contoh kasus-nya

```html
<p class="paragraf" id="paragrafPertama">Tebak warna paragraf</p>
```

```css
#paragrafPertama {color: red;}
.paragraf {color: blue;}
p {color: green;}
```

Jika dijalankan, maka paragraf akan berwarna merah. Mengapa terjadi? Karena konsep Specificity. Setiap element memiliki nilai berbeda-beda. Id selector memiliki nilai tertinggi daripada class selector dan element selector.

Untuk perhitungan mengenai Specificity bisa gunakan web berikut ini.

- [CSS Specificity Calculator](https://polypane.app/css-specificity-calculator/)