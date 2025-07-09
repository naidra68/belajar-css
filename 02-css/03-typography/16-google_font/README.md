# Google Font

Jika saya beranggapan bahwa menggunakan font external dengan cara `@font-face` cukup rumit dan membingungkan, maka saya bisa memakai solusi yang pasti cepat,gratis dan pasti-nya tidak pernah hilang.

Yap, menggunakan Google Font. Google Font menghadirkan pustaka font sebanyak kenangan mantan 😂. Saya buka dulu Google Font dan mencari font yang saya pengen.

Sepertinya saya menemukan font bernama `Poppins`. Jika sudah menemukan.

berikut contoh penerapan-nya

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
```

```css
body {
    font-family: 'Poppins';
}

.satu {
    font-style: italic;
}
.dua {
    font-weight: bold;
}
.tiga {
    font-style: italic;
    font-weight: bold;
}
```

Tag `<link>` taruh pada bagian tag `<head>` karena saya mengakses font dari luar berarti saya harus import menggunakan tag `<link>`. 

Ketika menggunakn Google Font, maka saya harus selalu online ke internet agar font yang saya pakai tetap ada. Jika tidak online maka font tersebut tidak terdeteksi.

Cara agar bisa berjalan tanpa internet maka gunakan font external seperti penjelasan sebelum ini.