# Align Self

Property ini berfungsi untuk mengatur posisi **child element (flex item)** secara satu persatu. Property ini akan menimpa pengaturan `align-items` jika terdapat property itu pada **parent element (flex container)**. Nilai yang dapat diisi juga sama seperti `align-items` yaitu :

- `stretch`
- `flex-start`
- `center`
- `flex-end`
- `baseline`

berikut contoh penerapan-nya

```html
<h1>Row</h1>
<div class="container row">
    <div class="box start">Box 1</div>
    <div class="box center">Box 2</div>
    <div class="box end">Box 3</div>
</div>
<div class="container row">
    <div class="box end">Box 1</div>
    <div class="box stretch">Box 2</div>
    <div class="box center">Box 3</div>
</div>
<div class="container row">
    <div class="box baseline fs-18">Box 1</div>
    <div class="box baseline fs-22">Box 2</div>
    <div class="box baseline fs-26">Box 3</div>
</div>
<h1>Column</h1>
<div class="container column">
    <div class="box start">Box 1</div>
    <div class="box center">Box 2</div>
    <div class="box end">Box 3</div>
</div>
<div class="container column">
    <div class="box end">Box 1</div>
    <div class="box stretch">Box 2</div>
    <div class="box center">Box 3</div>
</div>
<div class="container column">
    <div class="box baseline fs-18">Box 1</div>
    <div class="box baseline fs-22">Box 2</div>
    <div class="box baseline fs-26">Box 3</div>
</div>
```

```css
.container {
    height: 150px;
    border: 2px solid #FF734F;
    background-color: #09A8C8;
    margin: 1em;
    display: flex;
    align-items: start;
}
.row {flex-direction: row;}
.column {flex-direction: column;}
.box {
    margin: 0.2em;
    padding: 0.2em;
    text-align: center;
    background-color: #F9C75C;
}
.stretch {align-self: stretch;}
.start {align-self: flex-start;}
.center {align-self: center;}
.end {align-self: flex-end;}
.baseline {align-self: baseline;}

.fs-18 {font-size: 18px;}
.fs-22 {font-size: 22px;}
.fs-26 {font-size: 26px;}
```
Jika dijalankan, terlihat bahwa child element yang memiliki `align-self` akan memiliki style berbeda daripada child element lain. Fungsi ini cocok digunakan jika ingin memberikan style pada element yang lebih spesifik.