# BS5 Rasmlar

### Tasvir shakllari

Dumaloq burchakli:                                                           Aylana

![Parij](https://www.w3schools.com/bootstrap5/paris.jpg)![NYC](https://www.w3schools.com/bootstrap5/newyork.jpg)![San-Fran](https://www.w3schools.com/bootstrap5/sanfran.jpg)Thumbnail

***

### Dumaloq burchakli

`.rounded` classi rasmga yumaloq burchaklar qo'shadi:

```
<img src="cinqueterre.jpg" class="rounded" alt="Cinque Terre">
```

### Doira

`.rounded-circle` classi rasmni doira shakliga keltiradi:

```
<img src="cinqueterre.jpg" class="rounded-circle" alt="Cinque Terre">
```

### Eskiz

`.img-thumbnail` classi rasmni eskiz shakliga (chegaralangan) keltiradi:

```
<img src="cinqueterre.jpg" class="img-thumbnail" alt="Cinque Terre">
```

### Rasmlarni surish

Rasmni `.float-start` classi bilan chapga yoki `.float-end` bilan o‘ngga surib qo‘ying:

![](https://www.w3schools.com/bootstrap5/paris.jpg) ![](https://www.w3schools.com/bootstrap5/paris.jpg)

```
<img src="paris.jpg" class="float-start">
<img src="paris.jpg" class="float-end">
```

### Markazlashtirilgan rasm

Rasmga `.mx-auto` (margin:auto) va `.d-block` (displey:block) classlarini qo‘shish orqali rasmni markazga joylang:

![](https://www.w3schools.com/bootstrap5/paris.jpg)

```
<img src="paris.jpg" class="mx-auto d-block">
```

### Moslashuvchan rasmlar

Rasmlar o'lchami har xil bo'ladi. Ekranlar ham shunday. Moslashuvchan tasvirlar avtomatik tarzda ekran o'lchamiga moslashadi.

`<img>`  tegiga `.img-fluid` classini qo'shish orqali moslashuvchan rasmlar yarating. Keyin rasm ota elementga yaxshi moslashadi.

`.img-fluid` classi rasmga `max-width: 100%;` va `height: auto;` qo'llaydi::

```
<img class="img-fluid" src="ny.jpg" alt="New York">
```
