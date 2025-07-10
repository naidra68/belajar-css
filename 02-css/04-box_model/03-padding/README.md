# Padding

Setelah memahami property untuk content, sekarang saat-nya masuk ke `padding`. Lapisan kedua dari Box Model ini berfungsi agar konten tidak menempel langsung dengan garis tepi `border`.

Penulisan `padding` memliki 2 cara yaitu dengan langsung menulis shorthand notation untuk segala arah atau menulis property masing-masing arah `padding` nya,

Property `padding` mendukung semua satuan nilai mulai dari `px`, `%`, `em`, dan `rem`. Berikut penulisan `padding` dari berbagai arah.

- padding-top
- padding-bottom
- padding-left
- padding-right

## All Property

Sebelum masuk ke penulisan shorthand notation, saya akan mencoba menulis `padding` dari berbagai arah. Untuk memperjelas penggunaan `padding`, maka saya akan tampilkan konten dengan `border`.

berikut contoh penerapan-nya

```html
<p class="satu">Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci, suscipit commodi, eveniet natus aut dolore ullam debitis numquam aliquam nemo quam! Dolorem reiciendis nesciunt porro magnam, ipsa cumque voluptatem unde!</p>
```

```css
.satu {
    border: 1px solid black;
    padding-left: 20px;
    padding-right: 20px;
    padding-top: 30px;
    padding-bottom: 30px;
}
```

Apabila dijalankan, akan tampil bahwa garis tepi dan `padding` akan terlihat menjauh. Property ini akan menganut dari element tersebut. Jika element memiliki `background-color`, maka padding akan menyesuaikan `background-color` nya sesuai element.

berikut contoh penerapan-nya

```html
<p class="dua">Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia ullam excepturi, dolores suscipit libero in maiores cumque iusto perferendis autem nobis provident animi reiciendis tempore dolorum laudantium. Velit, itaque omnis.</p>
```

```css
.dua {
    border: 1px solid black;
    padding-left: 50px;
    padding-right: 0px;
    padding-top: 30px;
    background-color: red;
}
```


## Shorthand Notation

Jika penulisan menggunakan shorthand notation maka terlihat lebih ringkas, namun perlu dipahami secara teliti bahwa penulisan ini memiliki 4 nilai. 

4 nilai ini merujuk pada penulisan satu-persatu property `padding` tersebut.

perhatikan table berikut agar paham penulisan `padding`.


| Syntax                | Nilai Property | Deskripsi     |
| :---                  | :---:          | :---:          |
| padding: 20px;        | 1              | Semua nilai akan tampil sama. |
| padding: 20px 15px;   | 2              | Nilai pertama untuk top,bottom dan nilai kedua untuk left,right.  |
| padding: 20px 15px 20px;   | 3              | Nilai pertama untuk top dan nilai kedua, ketiga untuk left,right, dan nilai keempat untuk bottom.  |
| padding: 20px 15px 20px 10px;   | 4              | Nilai pertama untuk top, nilai kedua untuk right, nilai ketiga untuk bottom, dan nilai keempat untuk left.  |


Untuk menghafal urutan ini, saya biassanya menggunakan arah jarum jam atau bisa juga dengan kata TRouBLe.

berikut contoh penerapan-nya

```html
<p class="nilai1 sn">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam impedit neque, magni delectus voluptate eaque aspernatur asperiores tempora recusandae obcaecati soluta, iure ducimus fuga quisquam ullam et magnam nesciunt! Ipsum.</p>
<p class="nilai2 sn">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam impedit neque, magni delectus voluptate eaque aspernatur asperiores tempora recusandae obcaecati soluta, iure ducimus fuga quisquam ullam et magnam nesciunt! Ipsum.</p>
<p class="nilai3 sn">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam impedit neque, magni delectus voluptate eaque aspernatur asperiores tempora recusandae obcaecati soluta, iure ducimus fuga quisquam ullam et magnam nesciunt! Ipsum.</p>
<p class="nilai4 sn">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam impedit neque, magni delectus voluptate eaque aspernatur asperiores tempora recusandae obcaecati soluta, iure ducimus fuga quisquam ullam et magnam nesciunt! Ipsum.</p>
```

```css
.sn {
    width: 400px;
    border: 1px solid red;
    background-color: cyan;
}

.nilai1 {padding: 20px;}
.nilai2 {padding: 15px 20px;}
.nilai3 {padding: 5px 30px 10px;}
.nilai4 {padding: 5px 10px 15px 20px;}
```

Ketika dijalankan, terlihat bahwa lebar setiap element akan berbeda ketika lebar element di definisikan. Hal ini dapat terjadi karena lebar konten akan ditambah dengan lebar dari `padding` tersebut.

