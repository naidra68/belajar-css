# Text Indent

Property ini berfungsi mengatur identasi pada baris pertama paragraf agar menjorok ke kanan seperti hanya tulisan formal pada surat resmi atau paragraf pertama pada bab.

Property `text-indent` memiliki isi beragam dalam satuan length seperti `px`,`em`,`rem`, dan `rem`.

berikut contoh penerapan-nya

```html
<p class="satu">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sint vero, voluptas libero perferendis non quisquam quo tempora temporibus est recusandae laborum exercitationem blanditiis deleniti ipsum rerum unde quod ex similique?</p>
<p class="dua">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur corporis laudantium nulla, deleniti repudiandae, cupiditate, velit ab rem fuga sapiente ipsum aperiam ipsam facilis aliquam? Eaque dolores tempora expedita illo.</p>
<p class="tiga">Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel sed architecto enim. Asperiores, vel. Temporibus beatae accusantium obcaecati ipsa. Dolore illo rem minima esse corporis ea libero adipisci alias facere.</p>
<p class="empat">Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum nisi aliquid, tempore ea culpa dolore placeat rerum fugiat debitis est doloremque atque quod quia aliquam hic iste? Sit, officiis explicabo!</p>
<p class="lima">Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum nisi aliquid, tempore ea culpa dolore placeat rerum fugiat debitis est doloremque atque quod quia aliquam hic iste? Sit, officiis explicabo!</p>
```

```css
.satu {text-indent: 40px;}
.dua {text-indent: 1em;}
.tiga {text-indent: 1.5rem;}
.empat {text-indent: 50%;}
.lima {
    text-indent: -100rem;
    background-color: magenta;
}
```

Semua satuan length telah dipakai dalam penulisan `text-indent`. Pembuatan `text-indent` dengan nilai negatif digunakan untuk menyembunyikan paragraf.