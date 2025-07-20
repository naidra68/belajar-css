# Letter Spacing dan Word Spacing

Property `letter-spacing` dan `word-spacing` digunakan untuk mengatur jarak spasi antar huruf (letter) atau antar kata (word). Kedua property ini bisa di isi satuan px, em atau rem, dan juga bisa bernilai negatif.

## Letter Spacing

berikut contoh penerapan-nya

```html
<p class="satu">Paragraf Pertama</p>
<p class="dua">Paragraf Kedua</p>
<p class="tiga">Paragraf Ketiga</p>
```

```css
.satu {letter-spacing: 5px;}
.dua {letter-spacing: 0.7em;}
.tiga {letter-spacing: -0.1em;}
```


## Word Spacing

berikut contoh penerapan-nya

```html
<p class="empat">Paragraf Keempat</p>
<p class="lima">Paragraf Kelima</p>
<p class="enam">Paragraf Keenam</p>
```

```css
.empat {word-spacing: 5px;}
.lima {word-spacing: 1.2em;}
.enam {word-spacing: -0.4em;}
```

Disarankan menggunakan satuan `em` agar lebih fleksible untuk menghitung font-size dari parent element-nya.