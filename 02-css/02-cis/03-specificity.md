# Specificity Selector

Konsep terakhir untuk menyelesaikan **"pertentangan antar selector"** adalah specificity. Specificity merupakan metode perhitungan nilai untuk menentukan selector mana yang akan didahulukan atau di prioritaskan.

Sesuai dengan namanya, semakin spesifik atau semakin detail sebuah selector dibuat, maka akan semakin tinggi nilainya. Nilai specificity tidak hanya pada selector saja, melainkan ada pada inline style. Ini seperti nilai prioritas dari sebuah style.

berikut contoh penerapan-nya

```html
<p class="paragraf" id="paragrafPertama">Tebak warna paragraf</p>
```

```css
#paragrafPertama {color: red;}
.paragraf {color: blue;}
p {color: green;}
```

Jika dijalankan, maka paragraf akan berwarna merah. Mengapa hal ini bisa terjadi? Karena ada konsep Specificity. Setiap element memiliki nilai berbeda-beda. Id selector memiliki nilai tertinggi daripada class selector dan element selector.

Jika di jelaskan menggunakan table, berikut ini nilai masing-masing selector

| Selector                  | Contoh                | Nilai Specificity |
| -----------------------   | -------------------   | -----------       |
| Inline Style              | `style="color: red;"` | 1000              |
| Id Selector               | `#paragrafPertama`    | 100               |
| Class Selector            | `.paragraf`           | 10                |
| Attribute Selector        | `[href]`              | 10                |
| Pseudo-class Selector     | `:hover`              | 10                |
| Element Selector          | `p`                   | 1                 |
| Pseudo-element Selector   | `::before ::after`    | 1                 |
| Universal Selector        | `*`                   | 0                 |

Ketika melihat table diatas, ternyata banyak sekali ya nilai specificity. Apakah perlu saya menghafalkan semua ini? Jawabannya tidak perlu. Dizaman sekarang, terdapat banyak sekali website modern yang menyediakan perhitungan mengenai specificity selector ini. Berikut contoh website untuk perhitungan specificity.

- [CSS Specificity Calculator](https://polypane.app/css-specificity-calculator/)