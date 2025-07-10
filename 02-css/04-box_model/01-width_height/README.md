# Width and Height

Pembahasan mengenai `width` and `weight` akan merujuk ke lapisan terdalam Box Model yaitu `content`. Kedua property
ini mendukung seluruh satuan nilai length yang telah kita pelajari di bab sebelumnya, seperti `px`, `em`, `%`, dan `rem`.

## 1. pixel (px)

Pembahasan pertama menggunakan satuan pixel yang cukup sering digunakan untuk pemula.

berikut contoh penerapan-nya

```html
<div class="wh-px-1">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sed cumque quisquam error voluptatum pariatur fuga ut laboriosam quidem neque nisi quam sapiente totam, voluptate labore praesentium velit eaque accusantium! Qui.</div>
<div class="wh-px-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime sunt veniam dolor repellat vero cumque quae esse. Rerum aliquid quaerat assumenda voluptatibus. Quo dolore suscipit officiis maxime neque, praesentium doloremque.</div>
```

```css
.wh-px-1 {
    width: 300px;
    height: 150px;
    background-color: red;
}
.wh-px-2 {
    width: 600px;
    height: 150px;
    background-color: cyan;
}
```

Ketika dijalankan, content yang terdapat pada `<div>` dengan class `.wh-px-1` dan class `.wh-px-2` akan tampil lebar sesuai value dan tinggi sesuai value dengan konstant atau fixed.


## 2. percent (%)

Selain pixel, saya juga dapat mendefinisikan isi dari `width` and `height` menggunakan satuan percent.

berikut contoh penerapan-nya

```html
<div class="wh-percent-1">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sed cumque quisquam error voluptatum pariatur fuga ut laboriosam quidem neque nisi quam sapiente totam, voluptate labore praesentium velit eaque accusantium! Qui.</div>
<br>
<div class="wh-percent-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime sunt veniam dolor repellat vero cumque quae esse. Rerum aliquid quaerat assumenda voluptatibus. Quo dolore suscipit officiis maxime neque, praesentium doloremque.</div>
```

```css
.wh-percent-1 {
    width: 30%;
    height: 15%;
    background-color: red;
}
.wh-percent-2 {
    width: 60%;
    height: 15%;
    background-color: cyan;
}
```

Jika dijalankan, akan tampil menyesuaikan lebar layar web browser. 

Apa perbedaan dari `px` dan `%` untuk mengatur `width` `height` pada content element?

Perbedaan paling mendasar adalah nilai `px` itu relatif dan `%` itu absolute. Dimana nilai relatif sudah ditentukan atau fixed sedangkan nilai absolut fleksible tergantung parent element nya.

Ketika layar di perkecil dan di perbesar, maka nilai `px` akan tetap tampil seperti itu sedangkan nilai `%` akan fleksible mengikuti parent element-nya. Teknik mengatur `width` `height` menggunakan `%` ini dulu-nya dipakai untuk membuat element tampil responsive pada perangkat smartphone.

Karena saya menggunakan contoh tag `<div>` maka tidak perlu memberikan `width` dan `height` pada parent element yaitu tag `<div>`. Jika menggunakan tag seperti `<span>` maka perilaku-nya akan sedikit berbeda.

## 3. em

Ketika menggunakan satuan `em` untuk mengatur `width` dan `height` pada element, maka nilai tersebut berpatokan pada ukuran font-size element tersebut.

Contohnya, jika sebuah element memiliki font-size sebesar `20px` dan saya set `width: 30em`, maka sama dengan `30 * 20 = 600px`.

berikut contoh penerapan-nya

```html
<div class="wh-em-1">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sed cumque quisquam error voluptatum pariatur fuga ut laboriosam quidem neque nisi quam sapiente totam, voluptate labore praesentium velit eaque accusantium! Qui.</div>
<br>
<div class="wh-em-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime sunt veniam dolor repellat vero cumque quae esse. Rerum aliquid quaerat assumenda voluptatibus. Quo dolore suscipit officiis maxime neque, praesentium doloremque.</div>
```

```css
.wh-em-1 {
    font-size: 20px;
    width: 30em;
    height: 8em;
    background-color: red;
}
.wh-em-2 {
    width: 600px;
    height: 80px;
    background-color: cyan;
}
```

Ketika dijalankan, tampilan kedua `<div>` itu akan tampil dengan lebar yang sama namun beda pada font-size. Inilah perbedaan-nya. Karena `<div>` ke 2 menggunakan `px` dan tidak mengisi font-size maka font-size nya sesuai parent element secara default `16px`.

## 4. rem

Mengatur `width` dan `height` menggunakan satuan `rem` harus diperhatikan perbedaan-nya dengan `em`. Kalau dengan `em` saya tau bahwa sesuai font-size element-nya maka berbeda dengan `rem` yang sesuai font-size dari root element-nya.

berikut contoh penerapan-nya

```html
<div class="wh-rem-1">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sed cumque quisquam error voluptatum pariatur fuga ut laboriosam quidem neque nisi quam sapiente totam, voluptate labore praesentium velit eaque accusantium! Qui.</div>
<br>
<div class="wh-rem-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime sunt veniam dolor repellat vero cumque quae esse. Rerum aliquid quaerat assumenda voluptatibus. Quo dolore suscipit officiis maxime neque, praesentium doloremque.</div>
```

```css
.wh-rem-1 {
    font-size: 20px;
    width: 30rem;
    height: 8rem;
    background-color: yellow;
}
.wh-rem-2 {
    width: 600px;
    height: 80px;
    background-color: lightsalmon;
}
```

Jika dijalankan, terlihat bahwa satuan `rem` tidak akan mengambil `width` dan `height` dari font-size element-nya, namun tetap merujuk kepada root element-nya. Meskipun font-size tetap ada, namun tidak digunakan sebagai patokan `width` dan `height`.

> Apabila saya ingin fleksible dari font-size root element, maka menggunakan satuan `rem` sangat cocok.

## 5. Block and Inline Element

Perilaku `width` dan `height` akan berbeda tergantung dari jenis element-nya. Apabila element tersebut adalah Block element, maka `width` dan `height` akan berpengaruh pada element tersebut.

Sedangkan jika element tersebut adalah Inline element, maka `width` dan `height` tidak bekerja pada element tersebut.

berikut contoh penerapan-nya.

```html
<!-- Inline -->
<span class="inline">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium fugiat libero asperiores necessitatibus cumque, earum quisquam explicabo eos totam cum et dolorem vel perspiciatis, sapiente molestias repudiandae neque laborum corrupti!</span>
<span class="inline">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium fugiat libero asperiores necessitatibus cumque, earum quisquam explicabo eos totam cum et dolorem vel perspiciatis, sapiente molestias repudiandae neque laborum corrupti!</span>

<!-- Block -->
<div class="block">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium fugiat libero asperiores necessitatibus cumque, earum quisquam explicabo eos totam cum et dolorem vel perspiciatis, sapiente molestias repudiandae neque laborum corrupti!</div>
<div class="block">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium fugiat libero asperiores necessitatibus cumque, earum quisquam explicabo eos totam cum et dolorem vel perspiciatis, sapiente molestias repudiandae neque laborum corrupti!</div>
```

```css
.inline {
    width: 500px;
    height: 200px;
    background-color: lime;
}

.block {
    width: 500px;
    height: 200px;
    background-color: lime;
}
```

Saat dijalankan, perbedaan akan terlihat antara block dan inlin element. Dimana inline tidak akan terpengaruh oleh property `width` dan `height` sedangkan block akan terpengaruh oleh property `width` dan `height`.



# Min-Width and Min-Height
