# Transition Timing Function

Property ini berfungsi untuk ememntukan bagaimana efek transisi berjalan. Terdapat beebrapa nilai keyword yang bisa digunakan untuk property ini sebagai berikut.

- `linear`
- `ease`
- `ease-in`
- `ease-out`
- `ease-in-out`

Berikut penjelasan mengenai emua efek dari property `transition-timing-function` :

- **Linear** : efek transisi berlangsung merata mulai dari awal hingga akhir.
- **Ease** : efek transisi mulai dengan pelan, kemudian dipercepat, dan kembali pelan di akhir proses. Ini adalah nilai default.
- **Ease-in** : efek transisi mulai dengan pelan, kemudian dipercepat hingga akhir proses.
- **Ease-out** : efek transisi mulai dengan cepat, kemudian diperlambat hingga akhir proses
- **Ease-in-out** : efek transisi mulai dengan pelan, kemudian dipercepat, dan kembali pelan di akhir proses. Ini mirip dengan efek ease, tetapi tidak se-dramatis ease.

berikut contoh penerapan-nya

```html
<div class="container">
   <div class="box box1">Box 1</div>
   <div class="box box2">Box 2</div>
   <div class="box box3">Box 3</div>
   <div class="box box4">Box 4</div>
   <div class="box box5">Box 5</div>
</div>
```

```css
.box {
    width: 200px;
    height: 50px;
    line-height: 50px;
    text-align: center;
    color: white;
    margin: 1em;
    transition-duration: 1s;
    background-color: red;
}
.box1 {transition-timing-function: linear;}
.box2 {transition-timing-function: ease;}
.box3 {transition-timing-function: ease-in;}
.box4 {transition-timing-function: ease-out;}
.box5 {transition-timing-function: ease-in-out;}

.box1:hover,.box2:hover,
.box3:hover,.box4:hover,
.box5:hover {
    width: 400px;
    background-color: maroon;
}
```

Jika dijalankan, terlihat bahwa semua isi dari property `transition-timing-function` akan membuat transisi yang berbeda sesuai penjelasan diatas.