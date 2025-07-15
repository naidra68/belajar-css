# Multiple Animation

Ketika dirasa efek animasi masih kurang, CSS dapat mengizinkan saya untuk menambah efek animasi lanjutan ke dalam 1 penulisan property animation.

Saya sudah pernah mencoba-nya waktu membuat animation. Namun sekarang saya akan coba menambahkan 3 efek animasi.

berikut contoh penerapan-nya

```html
<div class="container">
    <div class="box box1"></div>
</div>
```

```css
.container {
    background-color: dimgray;
    width: 80%;
    height: 400px;
    margin: 1em auto;
}

.box {
    width: 100px;
    height: 100px;
    text-align: center;
    color: white;
    background-color: red;
}
.box {
    animation: warna 3s ease-in-out infinite,
                ukuran 5s linear infinite,
                bentuk 6s ease infinite;
}

@keyframes warna {
    0% {background-color: #e74c3c;}
    25% {background-color: #e67e22;}
    50% {background-color: #f1c40f;}
    75% {background-color: #2ecc71;}
    100% {background-color: #3498db;}
}
@keyframes ukuran {
    0%, 100% {
        width: 100px;
        height: 100px;
    }
    50% {
        width: 400px;
        height: 400px;
    }
}
@keyframes bentuk {
    0%, 100% {
        border-radius: 0%;
    }
    50% {
        border-radius: 50%;
    }
}

```

Jika dijalankan, terlihat bahwa saya menambahkan 3 animasi sekaligus dimulai dari bentuk element, ukuran element, dan warna element.

