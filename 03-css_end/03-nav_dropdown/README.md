# Navbar Dropdown

Sekarang saya akan membuat menu navbar horizontal dengan dropdown, jadi navbar ini memiliki child pada submenunya.

berikut contoh penerapan-nya

```html
<nav>
    <ul>
        <li><a href="#" class="active">Home</a></li>
        <li><a href="#">Service</a>
            <ul class="submenu">
                <li><a href="#">Service 1</a></li>
                <li><a href="#">Service 2</a></li>
                <li><a href="#">Service 3</a></li>
            </ul>
        </li>
        <li><a href="#">Project</a>
            <ul class="submenu">
                <li><a href="#">Project 1</a></li>
                <li><a href="#">Project 2</a></li>
            </ul>
        </li>
        <li><a href="#">About</a></li>
    </ul>
</nav>
```

```css
ul {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
}
ul li {
    background-color: #f1f1f1;
    position: relative;
}
li a {
    background-color: #515151;
    display: block;
    padding: 0.5rem 1rem;
    text-decoration: none;
    text-transform: uppercase;
    color: white;
}
li a.active {
    background-color: #44b5b5;
    color: white;
}
li a:hover {
    background-color: #515151;
    color: white;
}
.submenu {
    flex-flow: column;
    position: absolute;
    display: none;
}

nav li:hover > a {
    background-color:  #515151;
    color: white;
}
nav li:hover ul {
    display: block;
    min-width: 150px;
}
```