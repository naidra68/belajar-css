# Clip Path

Property ini berfungsi untuk membuat bentuk lingkaran, nilai yang dapat diisi oleh property ini adalah `circle()`,`ellipse`,`inset()`, dan `polygon()`.


## circle()

fungsi `circle()` butuh 1 nilai input berupa besar jari-jari. Selain itu saya juga bisa menentukan titik koordinat lingkaran yang secara default berada di tengah-tengah element.

berikut contoh penerapan-nya

```html
<h2>Circle()</h2>
<div></div>
<div class="clip-path1"></div>
<div class="clip-path2"></div>
<div class="clip-path3"></div>
<div class="clip-path4"></div>
```

```css
div {
    display: inline-block;
    width: 200px;
    height: 200px;
    margin: 0.5rem;
    background-color: dimgray;
}
.clip-path1 {clip-path: circle(50%);}
.clip-path2 {clip-path: circle(50px);}
.clip-path3 {clip-path: circle(100px at top);}
.clip-path4 {clip-path: circle(200px at 0 0);}
```

## ellipse()

fungsi `ellipse()` digunakan untuk membentuk ellips. Nilai input fungsi `ellips()` berupa dua buah nilai yang dipisah dengan tanda spasi. Nilai ini mewakili jari-jari elips untuk **sumbu x** dan **sumbu y**. Selain itu saya juga bisa menentukan titik pusat `ellipse`.

berikut contoh penerapan-nya

```html
<h2>Ellipse()</h2>
<div></div>
<div class="clip-path5"></div>
<div class="clip-path6"></div>
<div class="clip-path7"></div>
<div class="clip-path8"></div>
```

```css
.clip-path5 {clip-path: ellipse(50% 20%);}
.clip-path6 {clip-path: ellipse(100px 40px);}
.clip-path7 {clip-path: ellipse(100px 40px at top);}
.clip-path8 {clip-path: ellipse(250px 100px at 0 0);}
```

## inset()

Fungsi ini digunakan untuk membuat bentuk persegi dengan cara memotong
sisi dalam element. Nilai yang bisa diisi berupa jarak untuk ke-4 sisi element. Urutan penulisan dari 4 sisi element ini sama persis seperti penulisan `margin` atau `padding`, dapat menggunakan arah jarum jam atau kata **TR**ou**BL**e.

berikut contoh penerapan-nya

```html
<h2>Inset()</h2>
<div></div>
<div class="clip-path9"></div>
<div class="clip-path10"></div>
<div class="clip-path11"></div>
<div class="clip-path12"></div>
```

```css
.clip-path9 {clip-path: inset(10px 10px 10px 10px);}
.clip-path10 {clip-path: inset(50px 50px 50px 50px);}
.clip-path11 {clip-path: inset(100px 100px 0 0);}
.clip-path12 {clip-path: inset(0px 50px 100px 50px);}
```

## polygon()

Fungsi `polygon()` digunakan untuk memotong element dalam bentuk apa saja. Pemotongan dilakukan dengan cara menulis pasangan titik koordinat dalam bentuk x1 y1, x2 y2, x3, y3,...dst. Di antara setiap titik koordinat akan ditarik garis lurus sampai membentuk sebuah gambar 2 dimensi. 

berikut contoh penerapan-nya

```html
<h2>Polygon()</h2>
<div></div>
<div class="clip-path13"></div>
<div class="clip-path14"></div>
<div class="clip-path15"></div>
<div class="clip-path16"></div>
```

```css
.clip-path13 {clip-path: polygon(0 0, 100% 100%, 0 100%);}
.clip-path14 {clip-path: polygon(0 0, 100px 100px, 0 200px);}
.clip-path15 {clip-path: polygon(0% 0%, 100% 0%, 100% 75%, 75% 75%, 75% 100%, 50% 75%, 0% 75%);}
.clip-path16 {clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);}
```

Bahkan, saya bisa menggunakan property ini untuk membuat gambar yang akan saya masukkan tampak seperti bentuk bintang.

berikut contoh penerapan-nya

```html
<main>
    <img src="photo02.jpg">
</main>
```

```css
main {filter: drop-shadow(1px 1px 10px);}
img {
    clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
}
```