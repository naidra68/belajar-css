# Column Fill

Property ini digunakan untuk mengatur tinggi baris kolom. Nilai yang dapat diisi adalah keyword `balance` atau `auto`.

keyword `balance` adalah nilai default untuk membagi tinggi baris kolom secara merata. Sedangkan keyword `auto` digunakan untuk memaksa web browser untuk mengisi kolom pertama terlebih dahulu, baru kemudian pindah ke kolom berikutnya apabila sudah mencapai tinggi maksimal.

Agar property ini bisa digunakan, maka saya perlu set dulu tinggi parent element-nya.

berikut contoh penerapan-nya

```html
<div class="column-fill">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum. Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
</div>
```

```css
.column-fill {
    height: 400px;
    column-width: 200px;
    column-fill: auto;
    margin: 1em;
}
```

Ketika dijalankan, terlihat bahwa baris kolomnya akan tetap berlanjut hingga mencapai tinggi 400px sebelum pindah baris.

