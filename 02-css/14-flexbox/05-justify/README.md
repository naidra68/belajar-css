# Justify Content

Property ini digunakan untuk mengatur posisi **child element (flex item)** pada main axis atau sumbu utama dari flex container. Hasil dari property ini bisa berbeda tergantung sumbu yang dipakai.

Nilai dari porperty `justify-content` ada 6 yaitu :

- flex-start (default)
- center
- flex-end
- space-between
- space-around
- space-evenly

Saya akan bagi menjadi 2 property direction-nya yaitu `row` dan `column`. Karena penggunaan `justify-content` ini akan mempengaruhi sumbu pada main axis.

## 1. Row

berikut contoh penerapan-nya.

```html
<div class="container start">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container center">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container end">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container space-between">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container space-around">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container space-evenly">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
```

```css
/* Row */
.container {
    height: 150px;
    border: 2px solid #FF734F;
    background-color: #09A8C8;
    margin: 1em;
    display: flex;
    flex-direction: row;
}
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}

.start {
    justify-content: flex-start;
}
.center {
    justify-content: center;
}
.end {
    justify-content: flex-end;
}
.space-between {
    justify-content: space-between;
}
.space-around {
    justify-content: space-around;
}
.space-evenly {
    justify-content: space-evenly;
}
```

Jika dijalankan, terlihat bahwa setiap box element akan memiliki posisi yang berbeda-beda. Berikut ini adalah penjelasan satu persatu dari isi `justify-content`.

- **Flex-Start** digunakan untuk mengatur posisi child element berada di awal atau berada disebelah kiri.
- **Center** digunakan untuk mengatur posisi child element berada di tengah-tengah parent element.
- **Flex-End** digunakan untuk mengatur posisi child element berada di akhir atau berada disebelah kiri.
- **Space-Between** digunakan untuk mengatur posisi child element berada di bagian awal,tengah, dan akhir pada masing-masing child-nya.
- **Space-Around** digunakan untuk membagi spasi kosong sama besar di sisi kiri dan kanan child element.
- **Space-Evenly** digunakan untuk membagi spasi saam besar pada setiap child element.

## 2. Column

berikut contoh penerapan-nya

```html
<div class="container start">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container center">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container end">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container space-between">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container space-around">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
<div class="container space-evenly">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
```

```css
/* Column */
.container {
    height: 150px;
    border: 2px solid #FF734F;
    background-color: #09A8C8;
    margin: 1em;
    display: flex;
    flex-direction: column;
}
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}

.start {
    justify-content: flex-start;
}
.center {
    justify-content: center;
}
.end {
    justify-content: flex-end;
}
.space-between {
    justify-content: space-between;
}
.space-around {
    justify-content: space-around;
}
.space-evenly {
    justify-content: space-evenly;
}
```

Jika dijalankan, terlihat bahwa posisi dari child element akan berada di sumbu Y (vertical) yaitu kebawah. Jarak spasi antar child element pada contoh diatas memang dirasa kurang terlihat karena saya atur tinggi parent element-nya hanya 150px. Silahkan coba atur tinggi parent element-nya.