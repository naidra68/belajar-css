# Outline

Property ini berfungsi membuat garis tepi pada sebuah element, sama seperti `border`, namun `outline tidak mempengaruhi lebar elemen sehingga tidak bisa dianggap sebagai bagian dari box model.

Sama seperti `border`, `outline` memiliki 2 penulisan yaitu longhand notation dan shorthand notation.

## Longhand Notation

Pada penulisan ini terdapat 3 property yang harus di definisikan.

- `outline-color` berfungsi untuk menentukan warna `outline`.
- `outline-style` berfungsi untuk mengatur jenis `outline`.
- outline-width berfungsi untuk mengatur tebal outline.

berikut contoh penerapan-nya

```html
<div class="satu"></div>
```

```css
.satu {
    width: 200px;
    height: 150px;
    background-color: yellow;
    margin: 15px 20px;
    
    outline-color: black;
    outline-style: solid;
    outline-width: 5px;
}
```

Ketika dijalankan, akan terlihat bahwa setiap setiap warna, gaya, dan ketebalan telah diatur scara detail. Berbeda dengan `border` yang bisa diatur beda-beda style disetiap sisi, `outline` tidak bisa seperti itu.

## Shorthand Notation

Menggunakan penulisan ini akan lebih ringkas, sebagai contoh saya akan tambahkan border dan outline.

berikut contoh penerapan-nya

```html
<div class="dua"></div>
```

```css
.dua {
    width: 150px;
    height: 150px;
    background-color: aqua;
    margin: 35px 15px;
    
    outline: 5px solid black;
    border: 5px solid red;
}
```

Jika dijalankan, terlihat bahwa `outline` akan berada diluar element dan `border` ada didalam element.

## Outline Offset

Untuk mengatur jarak antara `outline` dan `border` agar tidak berdempet bisa menggunakan property `outline-offset`.

berikut contoh penerapan-nya

```html
<div class="tiga"></div>
```

```css
.tiga {
    width: 300px;
    height: 150px;
    background-color: limegreen;
    margin: 50px 15px 20px;
    border: 4px solid red;
    outline: 4px solid black;
    outline-offset: 5px;
}
```

<hr>

Outline dibuat sebagai pembantu menandai konten web (accessibility), seperti halnya ketika memasukkan form input akan muncul garis tepi tebal ketika sebuah inputan akan diketikkan,

Sebuah link jika difokuskan akan muncul garis tepi tersebut. Sebagai pembantu untuk User Experience melihat konten tersebut.

