# Animation

Property animation sangat banyak dan tidak mungkin saya hafalkan, menggunakan property animation satu persatu tidak ada masalah jika ingin membuat animation secara pasti dan dapat terlihat jelas.

Selain menggunakan property satu persatu, saat-nya saya menggunakan penulisan animation shorthand notation agar lebih ringkas dan mudah dilihat, yang terpenting adalah paham urutan isi dari property ini.

> animation : `name` `duration` `timing-function` `delay` `iteration-count` `direction` `fill-mode` `play-state`

Biasanya sih, developers dan programmer tidak menulis dan menggunakan semua property itu. Terkadang yang dipakai hanya-lah `name`,`duration`,`timing-function`, dan `iteration-count`.

<hr>

Setelah mengetahui mengenai CSS Animation, maka saya akan mencoba membuat element yang memiliki animation sederhana. Dengan pemahaman mengenai animation dan property CSS lain-nya, maka saya akan mencoba membuat-nya.


## 1. Animation Link

berikut contoh code-nya

```html
<div class="container">
   <a class="link-animation" href="#">Klik Saya</a>
</div>
```

```css
.container {
    background-color: dimgray;
    width: 80%;
    height: 400px;
    margin: 1em auto;
    color: white;
    padding: 1.5em;
}
.link-animation {
    display: inline-block;
    text-decoration: none;
    color: white;
    border: 2px solid black;
    padding: 1em;
    transform: translate(240px, 160px);
}

.link-animation:hover {
    animation: button 5s ease-in-out infinite;
}

@keyframes button {
    0% {
        background-image: linear-gradient(red,orange);
    }
    25% {
        background-image: linear-gradient(yellow,lime);
    }
    50% {
        background-image: linear-gradient(green,cyan);
    }
    75% {
        background-image: linear-gradient(blue,pink);
    }
    100% {
        background-image: linear-gradient(magenta,purple);
    }
}
```

## 2. Flip Text

berikut contoh code-nya

```html
<div class="container">
    <div class="satu">
    Hallo
        <div id="ganti">
            <div><div>Dunia</div></div>
            <div><div>Ibu</div></div>
            <div><div>Sepuh</div></div>
        </div>
    </div>
</div>
```

```css
.satu {
    font-size: 2em;
    text-align: center;
}

#ganti {
    height: 50px;
    overflow: hidden;
}

#ganti > div > div {
    padding: 4px 12px;
    display: inline-block;
    height: 45px;
    margin-bottom: 45px;
}

#ganti div:first-child {
    animation: tampil 5s linear infinite;
}

#ganti div div{
    background-color: #42c58a;
}
#ganti div:first-child div{
    background-color: #4ec7f3;
}
#ganti div:last-child div{
    background-color: #DC143C;
}

@keyframes tampil {
    0% {margin-top:-270px;}
    5% {margin-top:-180px;}
    33% {margin-top:-180px;}
    38% {margin-top:-90px;}
    66% {margin-top:-90px;}
    71% {margin-top:0px;}
    99.99% {margin-top:0px;}
    100% {margin-top:-270px;}
  }
```

## 3. Text Shadow Dance

berikut contoh code-nya

```html
<div class="container">
    <h1 class="shadow-dance">Text Bergoyang</h1>
</div>
```

```css
.shadow-dance {
    text-shadow: 5px 5px 0 red,
                    10px 10px 0 blue;
    animation: shadow_dance 2s infinite;
}

@keyframes shadow_dance {
    0%, 100% {
        text-shadow: 5px 5px 0 red,
                        10px 10px 0 blue;
    }
    50% {
        text-shadow: -5px -5px 0 red,
                        -10px -10px 0 blue;
    }
}
```

## 4. Loading Circle Square

berikut contoh code-nya

```html
<div class="container">
    <div class="wrapper">
        <div class="loading"></div>
    </div>
</div>
```

```css
.wrapper {
    transform: translate(50px, 100px);
}

.loading {
    width: 100px;
    height: 100px;
    border: 15px solid transparent;
    border-top: 15px solid #3498db;
    border-right: 15px solid #e74c3c;
    border-left: 15px solid #2ecc71;
    border-bottom: 15px solid #f39c12;
    border-radius: 50%;
    animation: rotate 2s linear infinite,
                morph 2s ease-in-out infinite;
}

@keyframes rotate {
    0% {transform: rotate(0deg);}
    100% {transform: rotate(360deg);}
}
@keyframes morph {
    0%, 100% {
        border-radius: 50%;
        width: 100px;
        height: 100px;
    }
    50% {
        border-radius: 10%;
        width: 150px;
        height: 150px;
    }
}
```

## 5. Spin 3D

berikut contoh code-nya

```html
<div class="container">
    <div class="fs">
        <p>MALAM</p>
    </div>
</div>
```

```css
.fs {
    font-size: 6em;
    text-align: center;
    font-family: sans-serif;
}
.fs > p {
    font-weight: bold;
    text-transform: uppercase;
    text-shadow: 
    1px 1px 0px#e63946,
    2px 2px 0px #f77f00,
    3px 3px 0px #fcbf49,
    4px 4px 0px #a8dadc,
    5px 5px 0px #457b9d;
    transform: rotate(0deg);
    animation: spin 4s linear infinite;
}

@keyframes spin {
    0% {
        transform: rotateY(0deg);
    }
    100% {
        transform: rotateY(360deg);
    }
}
```