# Normal Document Flow

Normal Document Flow adalah sebuah istilah dalam penyebutan mengenai proses document HTML ketika ditampilkan oleh web browser secara normal. Bisa dipahami sebagai default style bawaan web browser.

Setiap baris akan diproses, block element akan ditampilkan di bari tersendiri sedangkan inline ement akan diproses berdampingan. Sesuai dengan element html yang ada.

Dengan menanfaatkan doucment flow ini, saya bisa merancang layout halaman web sederhana.

berikut contoh penerapan-nya

```html
<div class="content">
    <h1>Header 1</h1>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vel aspernatur nesciunt quod magnam distinctio dolores sapiente ipsa non corrupti, laudantium inventore officiis nisi quae temporibus maxime voluptate reprehenderit dolore pariatur.</p>
    <div class="gallery">
        <img src="../img/fruit1.png"><img src="../img/fruit2.png">
        <img src="../img/fruit3.png"><img src="../img/fruit4.png">
    </div>
    <h2>Header 2</h2>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vitae asperiores eum magni mollitia nihil ullam sapiente, deserunt nemo numquam quis. Natus sunt voluptatibus cupiditate facilis necessitatibus praesentium sed placeat maxime.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo voluptas iure, tenetur nisi ipsum illo a aliquam ea cum fuga dignissimos aperiam provident perferendis commodi voluptatum alias! Ea, maiores rerum?</p>
</div>
```

```css
body {
    background-image: url('../../05-background/02-background_image/wallpaper.png');
    width: 960px;
    margin: 0 auto;
    font-family: sans-serif;
    background-size: cover;
}

h1,h2 {
    background-color: rgb(169, 167, 167);
    padding: 10px;
    margin: 0;
    text-align: center;
}
.content {
    background-color: rgb(231, 232, 226);
}
p {
    padding: 10px;
}
.gallery {
    background-color: rgb(231, 232, 226);
    width: 880px;
    margin: 10px auto;
}
img {
    border: 10px solid white;
    margin: 10px;
}
```

Dengan CSS, saya bisa membuat normal document flow ini menjadi lebih rapi sesuai tampilan keinginan saya. Setiap penulisan CSS dimulai dari atas ke bawah.

Ada 1 hal aneh ketika web browser memproses tag `<img>` yang berada didalam container semacam `<div>`. Setiap spasi dan enter pada masing-masing tag `<img>` akan memakai tempat beberapa pixel. Hal tersebut cukup menanggu karena struktur yang telah dibuat tidak seimbang.

Solusi paling tepat (sebelum adanya flexbox dan grid) adalah menggunakan property `float: left` pada seluruh tag `<img>` tersebut.