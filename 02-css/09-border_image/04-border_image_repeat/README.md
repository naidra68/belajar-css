# Border Image Repeat

Property ini berfungsi agar tampilkan border gambar menjadi presisi disetiap sisi. Sama seperti style bawaan dari `border`. Karena sebelumnya, saya membuat border gambar-nya tampil dengan efek stretch.

property `border-image-repeat` dapat diisi dengan nilai keyword seperti `stretch`, `repeat`, `round`, `space`.

nilai `stretch` adalah nilai default jika property ini tidak didefinisikan.

berikut contoh penerapan-nya

```html
<div class="box box1">Stretch</div>
<div class="box box2">Repeat</div>
<div class="box box3">Round</div>
<div class="box box4">Space</div>
```

```css
.box {
    width: 200px;
    height: 200px;
    line-height: 200px;
    text-align: center;
    color: white;
    font-size: 1.5em;
    background-color: dimgray;
    margin: 1em;
    float: left;
    border: 33px solid transparent;
    border-image-source: url('../img/border1.png');
    border-image-slice: 33%;
}
.box1 {
    border-image-repeat: stretch;
}
.box2 {
    border-image-repeat: repeat;
}
.box3 {
    border-image-repeat: round;
}
.box4 {
    border-image-repeat: space;
}
```

Ketika dijalankan, terlihat bahwa saya membuat semua nilai dari `border-image-repeat`. Nilai `stretch` adalah nilai default.

- Nilai `repeat` akan mengulang potongan border image-nya, namun di sudut gambar akan terpotong.

- Nilai `round` akan mengulang potongan border-image-nya secara sempurna.

- Nilai `space` sama seperti `round`, akan mengulang potongan border-image-nya secara sempurna dan menambah sedikit space antar gambar potongan-nya.