# Clear

Property `clear` digunakan untuk membersihkan efek float dari element sebelumnya. Biasanya property ini digunakan bersamaan dengan `float`.

Nilai dari property `clear` ada 4 yaitu `none`, `right`, `left`, dan `both`.

- `none` nilai default clear jika tidak di definisikan. Biasanya jarang dipakai.
- `right` untuk membersihkan efek `float: right`.
- `left` untuk membersihkan efek `float: left`,
- `both` untuk membersihkan kedua efek dari kiri dan kanan.

## Left

berikut contoh penerapan-nya

```html
<div class="float-left">
    <h1>Semangka</h1>
    <img src="../img/fruit1.png">
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. In inventore obcaecati impedit possimus repellat aut id. Officiis autem culpa, voluptate laudantium, totam cum temporibus, sequi in natus fuga voluptatem expedita.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam voluptatum mollitia exercitationem unde delectus excepturi id harum est. Nulla ex tenetur soluta atque quas vitae laborum vero impedit sed ut!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate a, suscipit quis numquam nihil iusto, esse necessitatibus at dolorum nam reiciendis sed blanditiis, natus eum iste facere. Itaque, tempora molestiae.</p>
</div>
```

```css
.float-left {
    margin: 1em;
}
.float-left > img {
    width: 200px;
    float: left;
    margin: 0 1em 1em 0;
    border: 1px solid black;
    padding: 0.5em;
}
.float-left > p:last-child{
    clear: left;
}
```

Jika dijalankan, terlihat bahwa paragraf terakhir akan memulai baris baru dan tidak menempel ke kanan bersama gambar-nya. Inilah fungsi dari property `clear`.

## Right

berikut contoh penerapan-nya

```html
<div class="float-right">
    <h1>Jeruk</h1>
    <img src="../img/fruit2.png">
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. In inventore obcaecati impedit possimus repellat aut id. Officiis autem culpa, voluptate laudantium, totam cum temporibus, sequi in natus fuga voluptatem expedita.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam voluptatum mollitia exercitationem unde delectus excepturi id harum est. Nulla ex tenetur soluta atque quas vitae laborum vero impedit sed ut!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate a, suscipit quis numquam nihil iusto, esse necessitatibus at dolorum nam reiciendis sed blanditiis, natus eum iste facere. Itaque, tempora molestiae.</p>
</div>
```

```css
.float-right {
    margin: 1em;
}
.float-right > img {
    width: 200px;
    float: right;
    margin: 0 0 1em 1em;
    border: 1px solid black;
    padding: 0.5em;
}
.float-right > p:last-child{
    clear: right;
}
```

Ketika dijalankan, terlihat bahwa paragraf terakhir akan memulai baris baru dan tidak menempel ke kiri bersama gambar-nya. Inilah fungsi dari property `clear`.

# Both

Nilai `both` adalah gabungan dari `left` dan `right` pada property `clear`. Nilai ini digunakan ketika terdapat element gambar yang memiliki paragraf dibawah element tersebut, jika menggunakan `float` pada gambar secara `left` dan `right` pada masing-masing gambar, maka secara otomatis paragraf akan berada disamping gambar.

Untuk mengatasi hal ini bisa gunakan `clear: left` dan `clear:right`, namun cara lebih simple adalah menggunakan nilai `both` dan tidak perlu menulis property 2x.

berikut contoh penerapan-nya

```html
<div class="both">
    <h1>Semangka dan Jeruk</h1>
    <img src="../img/fruit1.png">
    <img src="../img/fruit2.png">
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Pariatur perferendis illum nostrum nesciunt laboriosam aliquid, magnam provident incidunt nisi nam necessitatibus obcaecati perspiciatis vero omnis qui repudiandae eos eaque animi.</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Pariatur perferendis illum nostrum nesciunt laboriosam aliquid, magnam provident incidunt nisi nam necessitatibus obcaecati perspiciatis vero omnis qui repudiandae eos eaque animi.</p>
</div>
```

```css
.both > img {
    margin: 0 0 1em 1em;
    border: 1px solid black;
    padding: 0.5em;
}

.both > img:nth-child(even) {
    float: left;
    width: 100px;
}
.both > img:nth-child(odd) {
    float: right;
    width: 200px;
}

p {
    clear: both;
}
```

Jika dijalankan, terlihat bahwa paragraf akan berada dibawah gambar. Silahkan coba comment code css `p{clear:both;}`, maka saya akan melihat bahwa paragraf berada disamping gambar.