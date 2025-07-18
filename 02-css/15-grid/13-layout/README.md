# Membuat layout sederhana dengan Grid

Setelah mempelajari mengenai semua property tentang Grid, saatnya saya menguji kemampuan saya membuat layout sederhana menggunakan Grid.

Saya akan mengambil contoh layout yang pernah saya buat dengan flexbox. Jika menggunakan contoh itu, membuat layout seperti itu terasa sangat mudah jika menggunakan grid daripada flexbox.

berikut contoh penerapan-nya

```html
<div class="container">
    <header class="header">Header</header>
    <main class="main">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nisi consequatur nam illum porro in reiciendis quos ab, at quasi necessitatibus error assumenda fugiat vel minima, labore obcaecati, recusandae cumque temporibus!
    </main>
    <aside class="sidebar1">Sidebar 1</aside>
    <aside class="sidebar2">Sidebar 2</aside>
    <footer class="footer">Footer</footer>
</div>
```

```css
.container {
    width: 100vw;
    height: 100vh;
    display: grid;
    color: white;
    text-align: center;
    grid-template-columns: 1fr 1.5fr 1.5fr fr;
    grid-template-areas: 
    " header header header header "
    " main main main main "
    " sidebar1 sidebar1 sidebar1 sidebar1 "
    " sidebar2 sidebar2 sidebar2 sidebar2 "
    " footer footer footer footer "
    ;
}
.container > * {
    padding: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2rem;
}
.header {background-color: #04bcc5; grid-area: header;}
.main {background-color: #666666; grid-area: main;}
.sidebar1 {background-color: #cf781e; grid-area: sidebar1;}
.sidebar2 {background-color: #eb596e; grid-area: sidebar2;}
.footer {background-color: #252a34; grid-area: footer;}

@media screen and (min-width: 600px) {
    .container {
        grid-template-areas: 
        " header header header header "
        " main main main main "
        " sidebar1 sidebar1 sidebar2 sidebar2 "
        " footer footer footer footer "
        ;
    }
}

@media screen and (min-width: 900px) {
    .container {
        grid-template-areas: 
        " header header header header "
        " sidebar1 main main sidebar2 "
        " footer footer footer footer "
        ;
    }
}
```

Jika dijalankan, tampilan akan sama persis seperti yang telah saya buat waktu menggunakan flexbox. Perhatikan disini, untuk membuat responsive layout-nya, saya hanya tinggal mengatur template grid area tanpa perlu menambahkan property css lain.

Hal mudah seperti inilah, mengapa para developer dan programmer menggunakan grid untuk membuat layout website mereka. Selain itu, untuk mengatur content yang berada di dalam layout biasanya dikombinasikan dengan flexbox karena lebih mudah untuk dikontrol.