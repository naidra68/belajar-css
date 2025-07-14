# Column Gap

Property ini digunakan untuk mengatur jarak antar kolom. Nilai yang bisa diisi adalah satuan length seperti pixel.

berikut contoh penerapan-nya

```html
<div class="column-gap">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
</div>
```

```css
.column-gap {
    column-count: 3;
    column-gap: 100px;
}
```

Ketika dijalankan, terlihat bahwa baris antar kolom akan berjarak sebesar 100px. Dengan property ini maka mengatur baris antar kolom akan sangat mudah.