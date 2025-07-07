# Class Selector

Class Selector merupakan selector yang paling sering di pakai. Selector ini akan mencari setiap tag HTML yang memiliki atribut class dengan nama tertentu. Untuk menulis class selector, diawali dengan tanda titik: `.`. 

Agar sebuah paragraf bisa diakses dengan class selector, maka perlu menambahkan atribute class pada tag HTML.

contoh penerapan html
```html
<p class="merah">Paragraf ini akan ditampilkan berwarna merah</p>
```

contoh penerapan css
```css
.merah {
    color: red;
}
```

Lihat tanda titik pada kata `.merah`, inilah yang menandakan bahwa class selector dibuat dan dia akan mencari tag html yang memiliki atribute class yang isi-nya sama.

Beberapa Class Selector dapat dipakai dalam 1 tag HTML.

contoh penerapan html
```html
<p class="info penting">Text yang berisi info penting.</p>
```

contoh penerapan css
```css
.info {
    color: limegreen;
}
.penting {
    font-weight: bold;
}
```