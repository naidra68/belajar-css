# ::first-line Selector

selector `::first-line` dipakai untuk mengakses baris pertama dari sebuah element HTML.

berikut contoh penerapan-nya.

```html
<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ratione, culpa! Ratione facere delectus debitis ipsam, odit ullam aspernatur nemo, obcaecati sunt unde provident labore vitae laboriosam iure eveniet eligendi veritatis!</p>

<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorem libero harum quis reiciendis omnis iste alias culpa pariatur modi laboriosam minus, enim est commodi mollitia numquam animi consectetur! Necessitatibus, iusto.</p>
```

```css
p::first-line {
    color: green;
}
```

Jika dijalankan, maka setiap baris pertama akan di style. Hal ini tetap konsisten meskipun jendela web browser diperkecil maupun diperbesar. Tetap baris pertama saja yang akan di style.
