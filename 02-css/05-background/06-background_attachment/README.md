# Background Attachment

Property `background-attachment` merupakan property yang unik pada CSS. Property ini dipakai untuk mengatur gambar melekat pada halaman atau ke tampilan jendela web browser (viewport).

Nilai yang dapat di isi adalah `scroll` (default), `fixed`, dan `local`.

Jadi begini, ketika saya mendefinisikan gambar pada sebuah element menggunakan `background-image`, maka gambar tersebut akan melekat atau menempel pada halaman. Ketika di scroll pun akan tetap menempel kepada element tersebut.

Maka dari itu, jika saya tidak definisikan `background-attachment`, secara otomatis web browser akan mengisi-nya dengan isi `scroll`.

berikut contoh penerapan-nya

```html
<div class="box satu"></div>
```

```css
.box {
    width: 500px;
    height: 1000px;
    border: 3px solid purple;
    margin: 10px;
    background-image: url('../img/strawberry.png');
    background-repeat: no-repeat;
    background-position: 200px 200px;
}
.satu {background-attachment: scroll;}
```

Ketika dijalankan, terlihat bahwa gambar tetap di tempatnya saat saya scroll halaman ke bawah.

Apabila ingin gambar tampak melayang pada element web browser ketika saya scroll, maka nilai selanjutnya lah yang bisa melakukan hal tersebut yakni `fixed`.

berikut contoh penerapan-nya

```html
<div class="box dua"></div>
```

```css
.dua {background-attachment: fixed;}
```

Jika dijalankan, terlihat bahwa gambar akan tampak melayang pada web browser ketika di scroll kebawah. Efek ini sangat menarik untuk membuat sebuah background gambar secara preview.

Terakhir, `local`. Nilai ini cukup rumit dipahami karena hampir mirip dengan `scroll`, yang menjadikan pembeda adalah `local` akan terlihat berbeda jika background gambar tersebut digabung dengan isi konten berupa tulisan.

barikut contoh penerapan-nya

```html
<div class="box1 tiga">
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempora velit odio ea id exercitationem repellat magni, sunt iste veritatis eveniet ducimus veniam. Sequi vel totam accusantium velit illo, non doloremque?</p>

    <p>Ipsum odio, repellat esse vero nemo sunt a hic recusandae ad eum sit, quis molestiae eaque voluptates voluptatum iure quod iste! Facere modi animi expedita accusamus illo voluptas soluta eveniet.</p>

    <p>Error, laudantium suscipit? Corporis consequuntur, a tenetur ipsum optio sunt mollitia alias minus accusamus quas molestias eveniet quia assumenda ullam, esse sapiente exercitationem possimus, atque maiores fugiat aut placeat libero?</p>

    <p>Inventore asperiores quod cumque voluptate consequatur ad sapiente cum? Necessitatibus nisi ut voluptatem repudiandae quis eos dolore dignissimos quidem veniam consequatur dolor, deserunt, vel soluta harum in voluptates ea officiis.</p>

    <p>Facilis cumque vel blanditiis voluptas, cupiditate illum rerum corporis fugiat. Nobis aut, nihil, facere blanditiis iure error eos doloremque expedita excepturi praesentium assumenda laboriosam eius nesciunt voluptate? Dolores, libero ex.</p>

    <p>Ad repellat qui doloribus at fugit dolor, quasi tempora? Nesciunt iste impedit necessitatibus, officiis veniam asperiores suscipit eveniet, expedita quas reiciendis distinctio tempora ea quo hic cupiditate facere. Aperiam, corrupti!</p>

    <p>Quia mollitia dicta rerum, consequuntur, numquam ducimus pariatur quo nesciunt nostrum nemo quis id laborum molestiae quae sint ipsum enim, voluptate eligendi excepturi est eum? Nulla autem at amet quod!</p>
        
    <p>Natus molestiae dicta quia ducimus, aliquid incidunt aut provident expedita neque modi reprehenderit, est et magni. Sequi maxime vitae, est nostrum possimus doloribus. Vitae sapiente ipsa eum, beatae atque adipisci!</p>
</div>
```

```css
.box1 {
    width: 400px;
    height: 400px;
    padding: 0.5em;
    margin: 10px;
    overflow: scroll;
    color: white;
    background-image: url('../img/strawberry100x100.png');
}

.tiga {background-attachment: local;}
```

Jika dijalankan, terlihat ada scroll pada element tersebut, itu karena saya tambahkan `overflow: scroll` karena agar lebih jelas aja mengenai si `local` ini.

Ketika saya scroll, maka gambar akan menempel pada element dan saat di repeat, maka gambar akan tampil berulang kali sampai tinggi element tersebut.

<hr>

Dengan property ini, saya bisa gambar background yang menarik untuk dilihat.

berikut contoh penerapan-nya

```html
<div class="box2 pertama">
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorum quae incidunt, ad nemo fugiat itaque eaque, illo pariatur eius reiciendis odio consequuntur quis in praesentium? Eum in deserunt at cupiditate?</p>
    <p>Consectetur quas consequuntur nesciunt quisquam autem adipisci mollitia repellendus neque fugit illum, tempore commodi vitae asperiores alias doloribus, numquam voluptatibus soluta ducimus! Amet, totam quasi. Molestias labore quibusdam soluta distinctio.</p>
    <p>Delectus libero voluptatum, amet ullam quos iure blanditiis animi beatae corrupti accusantium. Odit dolores voluptate excepturi illo reprehenderit eveniet suscipit, mollitia pariatur est, vel adipisci esse veniam explicabo quae aut!</p>
</div>
<div class="box2 kedua">
    <span>Strawberry</span>
</div>
<div class="box2 ketiga">
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorum quae incidunt, ad nemo fugiat itaque eaque, illo pariatur eius reiciendis odio consequuntur quis in praesentium? Eum in deserunt at cupiditate?</p>
    <p>Consectetur quas consequuntur nesciunt quisquam autem adipisci mollitia repellendus neque fugit illum, tempore commodi vitae asperiores alias doloribus, numquam voluptatibus soluta ducimus! Amet, totam quasi. Molestias labore quibusdam soluta distinctio.</p>
    <p>Delectus libero voluptatum, amet ullam quos iure blanditiis animi beatae corrupti accusantium. Odit dolores voluptate excepturi illo reprehenderit eveniet suscipit, mollitia pariatur est, vel adipisci esse veniam explicabo quae aut!</p>
</div>
```

```css
.box2 {
    width: 100%;
    height: auto;
    text-align: center;
}
.pertama {
    padding: 1em;
    background-color: aqua;
}
.kedua {
    height: 300px;
    background-image: url('../img/strawberry.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-attachment: fixed;
}
span {
    line-height: 300px;
    color: white;
    font-size: 1.5em;
    background-color: red;
    padding: 0.5rem;
    border: 2px solid black;
}
.ketiga {
    padding: 1em;
    background-color: yellow;
}
```

Cukup menarik, bukan? Saya bisa membuat hal seperti ini saat belajar mengenai CSS. Saya perlu mengulik lagi mengenai css lebih dalam.