# Align Content

Property ini digunakan untuk mengatur posisi **child element (flex item)** di dalam fleksible **parent element (flex container)**. Property ini tidak berfungsi jika **parent element (flex container)** tidak memiliki `wrap`.

Selain itu, efeknya baru akan muncul apabila **child element (flex item)** cukup banyak serta diatur pada direction row (sumbu x | horizontal).

Nilai yang dapat di isi kedalam property ini ada 7 yaitu :

- `stretch` (default)
- `flex-start`
- `center`
- `flex-end`
- `space-between`
- `space-around`
- `space-evenly`

berikut contoh penerapan-nya

```html
<div class="container stretch">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
</div>
<div class="container start">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
</div>
<div class="container center">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
</div>
<div class="container end">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
</div>
<div class="container space-between">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
</div>
<div class="container space-around">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
</div>
<div class="container space-evenly">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
    <div class="box">Box 7</div>
    <div class="box">Box 8</div>
    <div class="box">Box 9</div>
</div>
```

```css
.container {
    height: 150px;
    border: 2px solid #FF734F;
    background-color: #09A8C8;
    margin: 1em;
    display: flex;
    flex-flow: row wrap;
}
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.stretch {align-content: stretch;}
.start {align-content: flex-start;}
.center {align-content: center;}
.end {align-content: flex-end;}
.space-between {align-content: space-between;}
.space-around {align-content: space-around;}
.space-evenly {align-content: space-evenly;}
```
Jika dijalankan, untuk isi dari start,center, dan end tidak ada perbedaan ketika menggunakan `justify-content`. Untuk `align-content` perbedaan-nya pada responsive child element-nya.

Saya fokuskan ke bagian isian space. Jika dijalankan pada layar sekecil 300px. Akan terlihat perbedaan bahwa isian space ini akan bekerja jika parent element sudah terlalu kecil lebar-nya.

Untuk melakukan percobaan itu, silahkan pakai **developer tool** atau gunakan extension **Responsive View**.