# Membuat Menu Navigasi Vertikal

Struktur menu navigasi bisa dibuat dari tag apa saja, yang paling sering dipakai adalah dari unordered list tag `<ul>`.

beriktu contoh penerapan-nya

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
nav {
    width: 200px;
}
ul {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    list-style: none;
    padding: 0;
    margin: 0;
}
ul li {
    background-color: #f1f1f1;
}
li a {
    display: block;
    color: #515151;
    padding: 0.5em 1em;
    text-decoration: none;
    border-left: 8px solid #515151;
    text-transform: uppercase;
}
li a.active {
    background-color: #eb3b5a;
    color: white;
}
li a:hover {
    background-color: #2c3e50;
    color: white;
    transition: all 0.3s;
}
```

