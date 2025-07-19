# :First nth Type and :Last nth Type Selector

Jika sudah paham mengenai `:first-child`,`:last-child`,`:first-of-type`,`last-of-type`. Maka tidak perlu dijelaskan lagi mengenai `:first-nth-type` dan `:last-nth-type`.

Fungsinya sama seperti `:first-of-type` dan `last-of-type`. Cuma ini versi yang agak kompleks-nya.

berikut contoh penerapan-nya

```css
p:nth-of-type(7) {
    color: blue;
}
p:nth-last-of-type(7) {
    color: red;
}
```

Jika dijalankan, maka paragraf no 7 akan berwarna biru dan paragraf 4 akan berwarna merah. Mengapa ini terjadi? karena type akan mengabaikan element bukan paragraf. Jika masih belum paham mengenai type dan child bisa dipelajari pelan-pelan.

