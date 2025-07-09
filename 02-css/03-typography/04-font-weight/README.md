# Font Weight

Property font-weight bertujuan untuk menebalkan teks (bold). Nilai untuk property ini bisa berupa angka 100, 200, 300, 400, 500, 600, 700, 800 dan 900 serta keyword normal, bold, bolder dan lighter.

Nilai angka 100 s/d 900 mencerminkan tingkat ketebalan huruf, mulai dari 100 untuk teks paling tipis, hingga 900 untuk teks dengan tingkat ketebalan tertinggi. Namun perlu dicatat nilai-nilai ini harus didukung oleh font yang dipakai.

> Kebanyakan font hanya mendukung teks normal atau bold (tebal), dan tidak mendukung tingkat ketebalan bertahap 100 s/d 900.

berikut contoh penerapan-nya

```html
<p class="weight100">Font Weight = 100</p>
<p class="weight200">Font Weight = 200</p>
<p class="weight300">Font Weight = 300</p>
<p class="weight400">Font Weight = 400</p>
<p class="weight500">Font Weight = 500</p>
<p class="weight600">Font Weight = 600</p>
<p class="weight700">Font Weight = 700</p>
<p class="weight800">Font Weight = 800</p>
<p class="weight900">Font Weight = 900</p>

<p class="normal">Font Weight = normal</p>
<p class="bold">Font Weight = bold</p>
<p class="lighter">Font Weight = lighter</p>
<p class="bolder">Font Weight = bolder</p>
```

```css
.weight100{font-weight: 100;}
.weight200{font-weight: 200;}
.weight300{font-weight: 300;}
.weight400{font-weight: 400;}
.weight500{font-weight: 500;}
.weight600{font-weight: 600;}
.weight700{font-weight: 700;}
.weight800{font-weight: 800;}
.weight900{font-weight: 900;}

.normal{font-weight: normal;}
.bold{font-weight: bold;}
.lighter{font-weight: lighter;}
.bolder{font-weight: bolder;}
```

Jika dijalankan, akan terlihat perbedaan setiap font-weight yang telah di definisikan. Apabila ingin melihat secara jelas perbedaan-nya maka bisa set font family menjadi "Segoe UI" pada tag `<p>`.

```css
p {font-family: "Segoe UI";}
```

