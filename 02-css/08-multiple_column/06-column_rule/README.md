# Column Rule

Property ini berfungsi sebagai penambah asset pada spasi kosong antar baris kolom. Alih-alih memperlihatkan ruang kosong spasi diantara baris kolom, saya bisa mengisinya dengan assets seperti `border`.

berikut contoh penerapan-nya

```html
<div class="column-rule">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
</div>
```

```css
.column-rule {
    column-count: 3;
    column-rule: 3px double black;
}
```

Jika dijalankan, terlihat bahwa terdapat border di isi baris kolom. Dengan menggunakan property ini akan terlihat lebih mudah dibaca dan dibedakan antar baris kolom.