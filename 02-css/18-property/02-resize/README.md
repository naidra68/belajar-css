# Resize

Property ini berfungsi untuk membuat element bisa di atur ukuran-nya menggunakan mouse. Nilai yang dapat diisi pada property ini seperti `horizontal`, `vertical`, dan `both`. **Perlu diperhatikan** bahwa ketika menggunakan property ini, maka harus ada property `overflow` agar dapat bekerja.

Mengapa demikian? Karena saya harus memberitahu web browser bahwa element yang saya beri `resize` itu nanti akan memiliki konten yang meluap, apabila ada konten yang meluap dari ukuran element tersebut, maka saya harus memberikan overflow pada element tersebut. Bisanya, property `overflow: auto` menjadi pilihan yang tepat ketika berhadapan dengan element `resize`.

berikut contoh penerapan-nya

```html
<main>  
    <div class="resize horizontal">Horizontal</div>
    <div class="resize vertical">Vertical</div>
    <div class="resize both">Both</div>
</main>
```

```css
main {
    width: 80%;
    margin: 1rem auto;
    border: 2px solid;
    background-color: yellow;
    display: flex;
    padding: 1.5rem;
}
.resize {
    width: 100px;
    height: 50px;
    display: flex;
    border: 2px solid;
    margin-right: 1rem;
    justify-content: center;
    align-items: center;
    background-color: aqua;
    overflow: auto;
}
.horizontal {resize: horizontal;}
.vertical {resize: vertical;}
.both {resize: both;}
```