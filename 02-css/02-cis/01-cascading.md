# Cascading

Konsep cascading dari CSS memiliki aturan mengenai style mana yang layak diprioritaskan. Pengertian lain, cascade adalah sebuah aturan penurunan style di dalam CSS.

Berikut adalah urutan prioritas style pada CSS mulai dari yang paling kuat:

1. User Style
2. Inline Style
3. Internal Style dan External Style
4. Web browser style


berikut contoh penerapan-nya

```html
<p>Tebak warna paragraf?</p>
```

```css
p {color: red;}
p {color: green;}
p {color: blue;}
```

Jika kode tersebut dijalankan, maka warna dari paragraf akan menjadi biru. 

Mengapa hal ini bisa terjadi? Karena konsep cascading seperti air terjun, maka akan menimpa satu sama lain. Inilah mengapa saya akan menggunakan comment untuk mematikan sementara fungsi css agar tidak saling timpa menimpa.

Kembali ke urutan prioritas dari style css ini. Jika dilihat, User style memiliki prioritas tertinggi karena User style dibuat oleh pengunjung website melalui fitur di web browser. Memang relatif jarang digunakan namun disediakan pada semua web browser.

Untuk mengakses user style pada browser, sebagai contoh saya menggunakan Brave Browser. Maka berikut ini cara-nya :

> **Settings** >> **Content** >> **Font-Size**

Prioritas ketiga/keempat itu antara internal dan external sama-sama kedudukan-nya. Tergantung mana yang lebih terakhir didefinisikan itulah yang menang.

> Contohnya : Saya buat external style dan dibawah saya buat internal style. Kode tersebut sama, maka yang menang adalah internal style karena konsep cascading tadi.

Bagaimana dengan inline style? Inline style memiliki prioritas tertinggi dibandingkan internal dan external, inline style berada di prioritas kedua setelah user style. Harap waspada menggunakan inline style karena dapat menimpa kode external dan internal yang telah dibuat.

Terkadang, sebagai web developer dan programmer untuk debugging code css dapat menggunakan inline style karena sifatnya prioritas teringgi maka dia akan menimpa semuanya agar code jalan secara terpaksa.

## Mengapa Cascading?

Jawabannya sederhana, agar saya tau mana prioritas style pada element akan dikerjakan. Jika belum paham mengenai ini, suatu saat ada style yang timpa menimpa maka saya akan kebingungan kok bisa seperti ini.