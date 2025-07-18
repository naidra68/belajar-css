# Clamp()

Fungsi ini berguna untuk menentukan nilai awal dan nilai maksimal serta nilai di antara kedua-nya. Ini seperti menentukan minimal, center, maksimal. Biasanya fungsi ini digunakan untuk pembuatan layout responsif yang lebih fleksible dengan mengontrol ukuran elemen dalam rentang tertentu.

Argumen yang di isi dengan fungsi `clamp()` ini terdapat 3 nilai. Nilai `min`,`val`,`max`. Berikut penjelasan mengenai nilai tersebut.

- `min` : Ini adalah nilai minimal dari suatu ukuran element.
- `val` : Ini adalah nilai yang diset diantar nilai minimal dan maksimal.
- `max` : Ini adalah nilai amksimal dari suatu ukuran element.

Sebagai contoh, saya akan membuat responsive font-size agar ukuran berbeda setiap jendela web browser diperbesar atau diperkecil.

```html
<div class="container">
    <p class="clamp1">Font Size ini akan tampil secara responsive dengan fungsi clamp()</p>
    <p class="clamp2">Font Size ini akan tampil secara responsive dengan fungsi clamp()</p>
    <p class="clamp3">Font Size ini akan tampil secara responsive dengan fungsi clamp()</p>
</div>
```

```css
.container {
    width: 80%;
    border: 2px solid black;
    margin: 1rem auto;
    padding: 1rem;
}
.clamp1 {font-size: clamp(1rem, 2.5vw, 2rem);}
.clamp2 {font-size: clamp(1.5rem, 2.5vw, 4rem);}
.clamp3 {font-size: clamp(1rem, 10vw, 2rem);}
```