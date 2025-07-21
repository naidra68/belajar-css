# List Style

Ketika berhadapan dengan tag `<ul>` dan `<ol>` untuk membuat list yang terdiri dari kumpulan tag `<li>`. Secara default, saya melihat adanya nomer urut (untuk ordered list) atau karakter bullet (untuk unordered list) di sisi kiri dari tulisasn pada element tersebut.

Dengan property `list-style` ini, saya dapat memberikan style dan dapat mengganti, menghilang, atau merombaknya. Property ini memiliki 2 aturan penulisan, yaitu longhand notation dan shorthand notation. Untuk penulisan shorthand dapat ditulis langsung `list-style`. Untuk penulisan longhand ada 3 property sebagai berikut

- `list-style-type`
- `list-style-image`
- `list-style-position`

## List Style Type

Property list-style-type berfungsi untuk mengatur jenis karakter bullet. Nilai yang bisa diisi cukup beragam dan akan berbeda tergantung apakah saya memakainya pada ordered list tag `<ol>` atau unordered list tag `<ul>`. 

Untuk `<ol>` dapat diisi oleh nilai berikut :

- `decimal`
- `decimal-leading-zero`
- `lower-roman`
- `upper-roman`
- `lower-greek`
- `lower-latin`
- `upper-latin`
- `armenian`
- `georgian`
- `lower-alpha`
- `upper-alpha`
- `none`

berikut contoh penerapan-nya

```html
<div class="ordered-list">
    <ol class="decimal">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="decimal-leading-zero">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="lower-roman">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="upper-roman">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="lower-greek">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="lower-latin">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="upper-latin">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="armenian">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="georgian">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="lower-alpha">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="upper-alpha">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ol class="none">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ol>
    <ul class="disc">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
    <ul class="circle">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
    <ul class="square">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
    <ul class="none">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
</div>
```

```css
.ordered-list {
    width: 90%;
    display: flex;
    margin: 2rem auto;
    padding: 2rem;
    flex-wrap: wrap;
}
.ordered-list > * {
    margin: 2rem;
}

.decimal {list-style-type: decimal; background-color: #fc5c65;}
.decimal-leading-zero {list-style-type: decimal-leading-zero; background-color: #eb3b5a;}
.lower-roman {list-style-type: lower-roman; background-color: #fd9644;}
.upper-roman {list-style-type: upper-roman; background-color: #fa8231;}
.lower-greek {list-style-type: lower-greek; background-color: #fed330;}
.lower-latin {list-style-type: lower-latin; background-color: #f7b731;}
.upper-latin {list-style-type: upper-latin; background-color: #26de81;}
.armenian {list-style-type: armenian; background-color: #20bf6b;}
.georgian {list-style-type: georgian; background-color: #2bcbba;}
.lower-alpha {list-style-type: lower-alpha; background-color: #0fb9b1;}
.upper-alpha {list-style-type: upper-alpha; background-color: #45aaf2;}
.none {list-style-type: none; background-color: #2d98da;}
```

## List Style Image

Property ini berfungsi untuk mengubah karakter penanda list menjadi gambar. Nilai dari property ini berupa alamat gambar dalam format url(path/ke/gambar).

berikut conton penerpaan-nya

```html
<ul class="list-style-img">
    <li>List Item</li>
    <li>List Item</li>
    <li>List Item</li>
    <li>List Item</li>
    <li>List Item</li>
</ul>
```

```css
.list-style-img {
    list-style-image: url('star.png');
    margin-left: 2rem;
}
```

## List Style Position

Property ini digunakan untuk mengatur posisi bullet. Nilai yang dapat diisi oleh property ini ada 2 yaitu `inside` dan `outside`. Saya akan tambahkan border agar terlihat perbedaan antara 2 nilai tersebut.

berikut contoh penerapan-nya

```html
<div class="flex">
    <ul class="inside">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
    <ul class="outside">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
</div>
```

```css
.flex {
    display: flex;
}
.inside > li, .outside > li {
    border: 2px solid;
}
.inside {
    list-style-position: inside;
    margin: 0 2rem;
}
.outside {
    list-style-position: outside;
    margin: 0 2rem;
}
```

## List Style (Shorthand)

Property list-style adalah penulisan singkat (shorthand) dari gabungan `list-style-type`, `list-style-image`, dan `list-style-position`. Property ini bisa diisi dengan 1, 2 atau 3 nilai dengan urutan bebas, sesuai dengan nilai yang bisa diisi ke dalam tiga property tersebut.

berikut contoh penerapan-nya

```html
<div class="flex">
    <ul class="list-style1">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
    <ul class="list-style2">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
    <ul class="list-style3">
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
        <li>List Item</li>
    </ul>
</div>
```

```css
.list-style3 > li {
    border: 2px solid;
}
.list-style1 {
    list-style: decimal-leading-zero;
    margin: 0 2rem;
}
.list-style2 {
    list-style: url('star.png');
    margin: 0 2rem;
}
.list-style3 {
    list-style: inside;
    margin: 0 2rem;
}
```

Biasanya, nilai `none` sering dipakai untuk menghapus property `list-style` bawaan dari tag `<ol>` dan `<ul>` ketika ingin membuat navbar.