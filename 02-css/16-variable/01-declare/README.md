# Declare

Pada CSS, untuk membuat deklarasi sebuah custom property adalah dengan cara menggunakan simbol minus 2x (`--`) atau menggunakan aturan `@property`.

> Aturan `@property` adalah fitur baru pada css saat ini (tahun 2025) dan fitur ini dapat digunakan sebagai deklarasi custom property.

## 1. Prefix 2 Dashes ( - - )

Untuk membuat custom property menggunakan prefix 2 dashed (`--`) adalah dengan cara menuliskan `--` lalu di ikuti dengan nama custom property. Untuk pemberian namanya bebas, namun pastikan berikan nama sesuai fungsi agar mudah mengerti dikemudian hari.

berikut contoh code css-nya

```css
div {
    --bg-color: limegreen;
}
```

Untuk memanggil custom property ini menggunakan sebuah fungsi bernama `var()` yang di definisikan pada isi property yang terdapat isian warna.


berikut contoh penerapan-nya

```html
<div>
    <h1>Belajar CSS Variable</h1>
    <p>Paragraf 1</p>
    <p>Paragraf 2</p>
    <pre>
        Sebuah teks didalam tag pre
    </pre>
    <section>Sebuah teks didalam tag section</section>
</div>
<section>
    <h1>Belajar CSS Variable</h1>
    <p>Paragraf 1</p>
    <p>Paragraf 2</p>
    <pre>
        Sebuah teks didalam tag pre
    </pre>
    <section>Sebuah teks didalam tag section</section>
</section>
```

```css
div {
    --bg-color: limegreen;
}

h1 {color: var(--bg-color);}
p {color: var(--bg-color);}
pre {color: var(--bg-color);}
section {color: var(--bg-color);}
```

Jika dijalankan, terlihat bahwa tag semua element yang berada didalam `<div>` akan berwarna limegreen. Mengapa tag `<section>` tidak dapat warna limegreen? Karena konsep cascade dan inheritance.

Agar semua element memiliki akses ke custom property maka perlu menambahkan selector khusus. Selector khusus ini merupakan sebuah pseudo-class untuk global variable yaitu `:root`.

Semua custom property biasanya akan ditaruh ke dalam selector ini dan pastinya selector ini akan dibuat diawwal pembuatan file `style.css`.

Sekarang saya akan coba perbaiki contoh code diatas menggunakan `:root` agar semua element memiliki warna yang sama. Tidak hanya ada di tag `<div>` saja.

berikut contoh penerapan-nya

```html
<div>
    <h1>Belajar CSS Variable</h1>
    <p>Paragraf 1</p>
    <p>Paragraf 2</p>
    <pre>
        Sebuah teks didalam tag pre
    </pre>
    <section>Sebuah teks didalam tag section</section>
</div>
<section>
    <h1>Belajar CSS Variable</h1>
    <p>Paragraf 1</p>
    <p>Paragraf 2</p>
    <pre>
        Sebuah teks didalam tag pre
    </pre>
    <section>Sebuah teks didalam tag section</section>
</section>
```

```css
:root {
    --bg-color: limegreen;
}
h1 {color: var(--bg-color);}
p {color: var(--bg-color);}
pre {color: var(--bg-color);}
section {color: var(--bg-color);}
```

Jika dijalankan, terlihat bahwa semua element memiliki warna yang sama. Ada satu lagi kesaktian menggunakan CSS Variable ini. Apabila saya ingin mengubah semua warna-nya, saya tidak perlu ubah satu persatu di element, namun hanya perlu mengubah di custom property yang terdapat di selector `:root` saja.

```css
:root {
    --bg-color: red;
}
```

> Pemberitahuan singkat, custom property memiliki case sensitive untuk penulisan nama-nya, sebagai contoh : `--bg-color` tidak sama dengan `--bg-Color`. Pastikan hati-hati memberi nama custom property.

## 2. @property Rule

Untuk penulisan menggunakan `@property` sedikit kompleks. Aturan ini akan memungkinkan untuk deklarasi secara eksplisit karena harus ada tipe data, pewarisan, dan nilai awal.

- Tipe data ini berfungsi untuk mengatur tag apa saja yang memiliki sistem serupa, seperti contoh-nya **warna**.
- Pewarisan (inheritance) ini pernah disinggung di CSS cascade dan inheritance, merupakan pewarisan untuk setiap tipe data yang sama.
- Nilai awal ini merupakan isi dari custom property, jika tipe data tadi di isi oleh warna. Maka isi-nya harus berupa satuan warna.

berikut contoh penerapan-nya

```html
<aside>Sebuah teks didalam tag aside</aside>
```

```css
@property --main-color {
    syntax: "<color>";
    inherits: false;
    initial-value: brown;
}

aside {color: var(--main-color);}
```

Jika dijalankan, terlihat bahwa hasilnya akan sama seperti menggunakan prefix 2 dashed.
