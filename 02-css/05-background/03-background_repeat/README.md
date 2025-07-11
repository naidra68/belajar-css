# Background Repeat

Property ini berfungsi untuk mengatur agar sebuah gambar background tidak tampil secara berulang-ulang (repeat) atau tidak. Nilai yang bisa di isi oleh property ini antara lain, `repeat`, `repeat-x`, `repeat-y`, `no-repeat`.


- `repeat` merupakan nilai default jika tidak di definisikan.
- `no-repeat` digunakan agar gambar tidak diulang.
- `repeat-x` digunakan agar gambar terulang secara horizonal.
- `repeat-y` digunakan agar gambar terulang secara vertical.

berikut contoh penerapan-nya

```html
<div class="satu">
    <span>Background-Repeat : Repeat</span>
</div>
<div class="dua">
    <span>Background-Repeat : no-repeat</span>
</div>
<div class="tiga">
    <span>Background-Repeat : repeat-x</span>
</div>
<div class="empat">
    <span>Background-Repeat : repeat-y</span>
</div>
```

```css
div {
    width: 400px;
    height: 400px;
    line-height: 400px;
    text-align: center;
    border: 3px solid black;
    background-color: green;
    float: left;
    margin: 10px;
    background-image: url('../img/jeruk.jpg');
}
span {
    background-color: aqua;
    padding: 0.5em;
}
.satu {background-repeat: repeat;}
.dua {background-repeat: no-repeat;}
.tiga {background-repeat: repeat-x;}
.empat {background-repeat: repeat-y;}
```

Jika dijalankan, akan terlihat perbedaan paling jelas.

# Background Repeat CSS3

Pada CSS3, `background-repeat` memiliki property baru yaitu `space` dan `round`. Setiap property baru ini memiliki ciri khas masing-masing.

berikut contoh penerapan-nya

```html
<div class="lima">
    <span>Background-Repeat : space</span>
</div>
<div class="enam">
    <span>Background-Repeat : round</span>
</div>
```

```css
.lima {width: 100%;height: 500px;background-repeat: space;}
.enam {width: 100%;height: 500px;background-repeat: round;}
```
Secara internal, ketika saya menulis `background-repeat: round`, yang diproses oleh web browser sebenarnya `background-repeat: round round`. 

Perhatikan ada 2 kali penulisan nilai round. Nilai pertama adalah untuk sumbu x (horizontal), sedangkan nilai kedua adalah untuk sumbu y (vertikal).