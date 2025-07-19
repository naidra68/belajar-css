# Element Spesific Selector

> Saat melihat file style css akan terlihat bahwa semua code css sudah di comment semua dan ketika dijalankan tidak akan tampil style-nya. Ini digunakan agar tidak terjadi timpa menimpa <s>text</s> style, karena css ada penjelasan mengenai cascade dan inheritance.

> Untuk memastikan semua style tampil, setiap selesai menggunakan dan memahami code css maka yang perlu dilakukan adalah memberikan comment lagi pada code tersebut. Untuk memberi atau menghilangkan comment bisa block code tersebut dan gunakan shortcut keyboard dengan cara pencet `ctrl` + `/`.

Element Spesific Selector merupakan istilah yang sama seperti Group Selector, namun element spesific selector menggabungkan selector yang lebih spesific. Saya buat contoh kasus agar mudah dipahami.

Contoh kasus :
***Saya membuat 3 buah header, masing-masing memiliki class yang sama yaitu **sorot**. Jika menggunakan class selector maka semua header akan memiliki style yang sama, bukan? namun jika saya ingin spesific hanya pada header ke-3? maka element spesific selector ini adalah solusi yang tepat.***

berikut contoh penerapan-nya

```html
<h1 class="judul">Header 1 dengan class judul</h1>
<h2 class="judul">Header 2 dengan class judul</h2>
<h3 class="judul">Header 3 dengan class judul</h3>
```

```css
h3.judul {
    color: red;
}
```

**Perlu diperhatikan!!** element selector dan class selector harus digabung dan **tidak boleh ada spasi** diantara mereka. Karena jika ada spasi maka itu sudah berbeda lagi fungsi-nya. Penasaran? Coba aja.


Contoh lain, saya bisa menggabungkan element spesific selector ini dengan group selector untuk mendapatkan element yang sangat spesific agar lebih jelas di style. Coba pahami kode dibawah ini.

```css
h4#judul, p.text, span[title] {
    color: green;
}
```