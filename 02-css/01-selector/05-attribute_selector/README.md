# Attribute Selector

Attribute selector merupakan selector yang dipakai untuk mencari setiap tag html yang ada atau tidak-nya memiliki attribute. Selector ini sama seperti class dan id, attribute selector bersifat lebih global karena bisa dipakai untuk seluruh attribute HTML. Untuk menulis attribute selector, diawali dengan tanda kurung: `[]`. 

Sebuah link pasti memiliki attribute `href`. Dengan attribute selector maka saya perlu menggunakan attribute `href` untuk style link daripada menggunakan element/tag selector.


> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

<hr>

contoh penerapan html
```html
<a href="https://www.google.com">Google Search Engine</a>
```

contoh penerapan css
```css
[href] {
    color: red;
}
```

Lihat tanda kurung pada `[href]`, tanda kurung siku inilah yang menandakan attribute selector. Atribut yang ingin dicari ditulis dalam tanda kurung siku.

Namun, jika saya ingin spesifik bahwa attribute href yang berada pada tag `<a>` saja yang akan digunakan, maka bisa memakai kode sebagai berikut

```css
a[href] {
    color: red;
}
```

Attribute selector memiliki fitur yang memudahkan proses saya mencari attribute yang akan di style nanti-nya berdasarkan nilai awalan (prefix) dan nilai akhiran (suffix). Attribute selector sebenarnya berasal dari CSS3, namun saya taruh disini karena ini cukup penting pada saat saya belajar pertama kali CSS.


Contoh lain penerapan dari attribute selector dapat digunakan pada unordered list yang dimana setiap list memiliki attribute title yang akan saya style nantinya. Ada 6 percobaan yang akan saya buat untuk memahami lebih jelas mengenai attribute selector ini.

<hr>

Copy kode html dibawah ini jika malas ngetik. Pada index sudah tersedia sih.
```html
<ul>
    <li>Belajar HTML</li>    
    <li title="belajar">Belajar CSS</li>    
    <li title="belajar javascript">Belajar Javascript</li>    
    <li title="belajar java">Belajar Java</li>    
    <li title="belajar PHP">Belajar PHP</li>    
    <li><a title="belajar MYSQL" href="https://www.w3schools.com/MySQL/default.asp">Belajar MYSQL</a></li>    
    <li><a title="belajar Bootstrap" href="https://www.w3schools.com/bootstrap5/index.php">Belajar Bootstrap</a></li>
    <li><a href="https://www.w3schools.com">Belajar Programming</a></li>   
</ul>
```

## 1. Percobaan Pertama

Saya akan style attribute `title`. Maka setiap tag yang memiliki attribute `title` akan berubah.

contoh penerapan css

```css
[title] {
    color: green;
}
```

## 2. Percobaan Kedua

Saya akan style element `li` dan attribute `title`. Maka setiap tag `li `yang hanya memiliki attribute `title` lah yang akan berubah.

contoh penerapan css

```css
li[title] {
    color: magenta;
}
```

## 3. Percobaan Ketiga

Selain nama attribute, saya juga bisa mengakses value dari attribute tersebut seperti contoh. Jika saya ingin hanya title `belajar javascript` yang akan di style maka bisa memasukkan kode sebagai berikut.


contoh penerapan css

```css
[title="belajar javascript"] {
    color: yellow;
}
```

## 4. Percobaan Keempat

Sekarang saya ingin style value dari attribute namun hanya pada kata **belajar**. Apakah bisa? Tentu saja bisa. Dengan menambahkan karakter tilde `~` sebelum tanda `=` maka ini menandakan bahwa saya sedang mencari kata **kota** di dalam attribute title.


contoh penerapan css

```css
[title~="belajar"] {
    color: blue;
}
```

## 5. Percobaan Kelima

Jika saya ingin mencari value didalam attribute title namun mengandung kata tertentu? Jawabannya bisa. Contoh, jika saya ingin style value yang mengandung kata **java** maka ini tidak bisa jika menggunakan tilde, karena tilde butuh satu kata full. Untuk mengatasi hal tersebut, kita bisa menggunakan bintang `*`.


contoh penerapan css

```css
[title*="java"] {
    color: orange;
}
```

## 6. Percobaan Keenam

Untuk mencari **value awal** dari attribute yang dituju atau **value akhir** dari attribute yang dituju maka bisa menggunakan karakter sebagai berikut.

- `^` = untuk value awal
- `$` = untuk value akhir


contoh penerapan css

```css
/* Nilai Awal */
[href^="https"] {
    color: green;
}

/* Nilai Akhir */
[href$=".com"] {
    color: red;
}
```

