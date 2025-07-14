# Transition

Transition adalah perubah style dari sebeuah element HTML secara bertahap. Sebenarnya efek transisi sudah ada jika saya melihat kembali fungsi dari `:hover` itu juga bisa dikatakan sebagai transition.

Namun dengan menggunakan transition ini, efek dari transisi akan lebih halus dan tidak melompat seperti `:hover` langsung.


## Link Tree

1. [01-transition_property](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/01-transition/01-transition_property)
2. [02-transition_duration](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/01-transition/02-transition_duration)
3. [03-transition_timing_function](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/01-transition/03-transition_timing_function)
4. [04-transition_delay](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/01-transition/04-transition_delay)
5. [05-transition](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/01-transition/05-transition)
6. [06-multiple_transition](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/01-transition/06-multiple_transition)

# Animation

Animation adalah animasi css yang dapat digunakan kedalam element html, secara teknis `animation` hampir mirip dengan `transition`. Perbedaan hanya pada pengaturan efek nya saja.

Jika transisi mengatur efek awal dan akhir saja, sedangkan animation akan mengatur nya secara bertahap. Jadi efeknya bisa dilihat bertahap.

Sebelum membuat animation pada CSS, saya harus mengenal Keyframe.

## Keyframe

Keyframes adalah sebuah efek untuk mengatur waktu perubahan animasi yang akan terjadi.

Jika pada transition hanya ada awal dan akhir, berbeda dengan animation keyframe ini. Dengan keyframe maka dapat ditentukan berdasarkan persentase animation.

berikut contoh penerapan-nya

```css
@keyframes lebar {
    0% { width: 300px; }
    50% { width: 100px; }
    100% { width: 1000px; }
}
```

Nilai percentase tidak hanya 3 saja seperti contoh diatas. Jika saya ingin membuatnya berubah-ubah setiap 10% maka itu bisa dilakukan.

berikut contoh penerapan-nya

```css
@keyframes warna {
    10% {background-color: red;}
    20% {background-color: green;}
    30% {background-color: blue;}
    40% {background-color: cyan;}
    50% {background-color: magenta;}
    60% {background-color: yellow;}
    70% {background-color: black;}
    80% {background-color: purple;}
    90% {background-color: tomato;}
    100% {background-color: lime;}
}
```

Jika sudah mengerti mengenai keyframe ini, maka selanjutnya baru saya buat animation-nya dengan property yang telah disediakan oleh CSS.

## Link Tree

1. [01-animation_name](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/01-animation_name)
2. [02-animation_duration](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/02-animation_duration)
3. [03-animation_timing_function](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/03-animation_timing_function)
4. [04-animation_delay](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/04-animation_delay)
5. [05-animation_iteration_count](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/05-animation_iteration_count)
6. [06-animation_direction](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/06-animation_direction)
7. [07-animation_fill_mode](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/07-animation_fill_mode)
8. [08-animation_play_state](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/08-animation_play_state)
9. [09-animation](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/09-animation)
10. [10-multiple_animation](https://github.com/naidra68/belajar-css/tree/main/02-css/12-transition_animation/02-animation/10-multiple_animation)