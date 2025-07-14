# Column Span

Property ini berfungsi untuk keluar dari efek kolom yang telah ditambah sebelumnya. Apabila saya ingin membuat 2 buah element kolom. Maka untuk memisahkan-nya adalah menggunakan `column-span`.

Property ini dapat diisi oleh salah satu dari 2 nilai yaitu `none` dan `all`. Nilai default nya adalah `none`.

berikut contoh penerapan-nya

```html
<div class="column">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora.</p>
    <h3 class="span">Belajar CSS</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora.</p>
</div>
```

```css
.column {
    column-count: 3;
    margin: 1em;
}
.span {
    margin: 1em auto;
    background-color: aqua;
    column-span: all;
}
```

Jika dijalankan, terlihat bahwa tag `<h3>` yang memiliki property `column-span` dengan isi `all` akan membuat baris baru ke bawah dan tidak bergabung ke baris atas.