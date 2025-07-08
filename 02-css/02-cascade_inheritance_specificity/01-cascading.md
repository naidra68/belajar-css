# Cascading

Konsep cascading dari CSS memiliki aturan mengenai style mana yang layak diprioritaskan.

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

Mengapa hal ini bisa terjadi? Karena konsep cascading seperti air terjun, maka akan menimpa satu sama lain. Inilah mengapa saya akan menggunakan comment untuk mematikan sementara fungsi css agar tidak saling menimpa.

Namun, kembali lagi dengan urutan prioritas style pada css. Pada contoh kode diatas, bisa menggunakan internal style dan external style.

Prioritas kedua itu antara internal dan external sama-sama kedudukan-nya. Tergantung mana yang lebih terakhir didefinisikan itulah yang menang.

> Contohnya : Saya buat external style dan dibawah saya buat internal style. Kode tersebut sama, maka yang menang adalah internal style karena konsep cascading tadi.

Bagaimana dengan inline style? Inline style memiliki prioritas tertinggi daripada internal dan external. Harap waspada menggunakan inline style karena dapat menimpa kode external dan internal yang telah dibuat.

Biasanya inline style digunakan sebagai debugging CSS.