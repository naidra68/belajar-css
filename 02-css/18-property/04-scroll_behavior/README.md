# Scroll Behavior

Property ini berfungsi untuk mengatur proses pemindahan tampilan layar pada suatu link internal. Secara default, jika klik link internal, maka layar web browser akan **"lompat"** menuju tempat yang dituju. Dengan menambah property `scroll-behavior`, proses ini bisa dibuat menjadi efek scrolling yang berjalan secara perlahan dan halus.

berikut contoh penerapan-nya

```html
<h1 id="judul">JUDUL BESAR</h1>
<a href="#judul">UP</a>
```

```css
html { scroll-behavior: smooth; }
h1 { height: 2000px; }
```

Ketika dijalankan, terlihat bahwa saat saya klik tulisan up, maka dia akan otomatis scroll ke atas secara halus dan tidak hanya loncat saja. Biasanya property ini wajib digunakan di web modern agar efek scroll lebih menarik.