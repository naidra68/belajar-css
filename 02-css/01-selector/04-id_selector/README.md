# Id Selector

Id Selector merupakan selector yang sering dipakai setelah class selector. Selector ini akan mencari setiap tag HTML yang memiliki atribut id dengan nama tertentu. Untuk menulis class selector, diawali dengan tanda crash/pagar: `#`. 

Agar sebuah paragraf bisa diakses dengan id selector, maka perlu menambahkan atribute id pada tag HTML.

<hr>

contoh penerapan html
```html
<p id="pesan">Selamat datang di CSS</p>
```

contoh penerapan css
```css
#pesan {
    background-color: aqua;
}
```

Lihat tanda pagar pada kata `#pesan`, inilah yang membedakan antara id selector dan class selector. Perbedaan paling dasar adalah id selector hanya bisa digunakan 1 kali di dalam setiap halaman HTML. Atau dengan kata lain setiap id harus unik, tidak boleh terdapat 2 buah tag dengan atribut id yang sama.

Berdasarkan pengalaman developers, **class selector** digunakan lebih sering daripada **id selector**. Alasan-nya akan jelas jika sudah masuk ke prioritas urutan di css yang disebut sebagai cascade dan inheritance.

Biasanya id selector digunakan paling sering ketika sudah menggunakan javascript untuk manipulasi DOM.

Berikut ringkasan singkat mengenai id selector.
- Id selector harus unik. Jangan gunakan 2 tag HTML yang memiliki id selector sama. Gunakan Id selector hanya digunakan untuk 1 element HTML saja.
- Developers dan Programmer memiliki aturan tak tertulis bahwa untuk menulis id selector menggunakan penulisan camelCase. **camelCase** merupakan istilah penulisan yang menjadikan awalan kata kedua, ketiga dan seterus-nya menggunakan huruf besar.
- Id selector cukup penting digunakan jika saya hanya membuat selector tersebut berlaku pada satu element pada setiap halaman.