# Column Width

Property `column-width` digunakan untuk mengatur jumlah column berdasarkan lebar column.

Sebagai contoh, apabila saya set lebar column nya sebesar 200px, maka seluruh lebar layar akan menampung nilai 200px sebanyak apapun. Jika lebar layar adalah 960px, maka 4,8 kolom. `960 / 200 = 4,8 kolom`.

Namun didalam contoh, saya tidak set lebar parent element-nya. Maka yang terjadi adalah lebar nya otomatis akan terbagi sesuai lebar layar device saya.

berikut contoh penerapan-nya

```html
<div class="column-width">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore expedita provident fugiat quod dolores amet tenetur labore neque voluptates libero. Quisquam vitae voluptatem dignissimos impedit unde maiores tenetur deleniti rerum.</p>
    <p>Modi velit vel eaque blanditiis pariatur fuga in iure quisquam, delectus error, dolorum alias ipsa tempora. Impedit veniam iste nihil explicabo laudantium, ab distinctio reprehenderit assumenda magnam iure, ullam reiciendis!</p>
    <p>Asperiores dicta, illum doloremque expedita vel blanditiis. Atque culpa ducimus, eum veniam pariatur, animi necessitatibus, exercitationem corporis dolores dolorem et officiis eius laborum. Eaque sequi obcaecati dolore nesciunt sint corporis.</p>
</div>
```

```css
.column-width {
    column-width: 200px;
    margin: 1em;
}
```