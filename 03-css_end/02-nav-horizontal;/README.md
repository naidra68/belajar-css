# Nav Horizontal

Selain navbar vertical, sekarang saya akan mencoba membuat navbar horizontal. Karena saat ini web modern semua pasti menggunakan navbar horizontal. Memanfaatkan Flexbox untuk membuat navbar horizontal lebih mudah dilakukan.

berikut contoh penerapan-nya

```html
<nav>
    <ul>
        <li><a href="#" class="active">Home</a></li>
        <li><a href="#">Service</a></li>
        <li><a href="#">Project</a></li>
        <li><a href="#">About</a></li>
    </ul>
</nav>
```

```css
ul {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
}
ul li {
    background-color: #f1f1f1;
}
li a {
    display: block;
    color: #515151;
    padding: 1em 2em;
    text-decoration: none;
    text-transform: uppercase;
}
li a.active {
    background-color: #eb3b5a;
    border-bottom: 5px solid #515151;
    color: white;
}
li a:hover {
    background-color: #515151;
    color: white;
    transition: background-color 0.3s;
    border-bottom: 5px solid #44b5b5;
}
```