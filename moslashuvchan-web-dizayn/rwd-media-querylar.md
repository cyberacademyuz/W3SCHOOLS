# RWD Media Querylar

### Media so'rovi nima?

Media querie CSS3 da kiritilgan CSS texnikasidir.

U ma'lum bir shart rost bo'lgandagina, CSS xususiyatlari blokini o'z ichiga olgan @media qoidasidan foydalanadi.

{% code title="Agar brauzer oynasi 600px yoki undan kichikroq bo'lsa, background rangi och ko'k rang bo'ladi:" %}
```
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```
{% endcode %}

### Breakpoint qo'shish

Avvalgi mavzularda veb-sahifani qatorlar va ustunlar orqali yaratdik va u maslashuvchan bo'lsada kichik ekranda yaxshi ko'rinmas edi.

Media querielar bunga yordam beradi. Breakpoint qo'shganimizda dizaynning ayrim joylari har bir breakpointda boshqacha ko'rinishga o'tadi.



&#x20;                           Ish stoli                                                                 Telefon\
![](https://www.w3schools.com/css/rwd\_desktop.png)                                      ![](https://www.w3schools.com/css/rwd\_phone.png)\


**768px**da breakpoint qo'shish uchun media queriedan foydalanish:

{% code title="Ekran (brauzer oynasi) 768px dan kichkina bo'lsa, har bir ustunning kengligi 100% bo'lishi kerak:" %}
```
/* For desktop: */
.col-1 {width: 8.33%;}
.col-2 {width: 16.66%;}
.col-3 {width: 25%;}
.col-4 {width: 33.33%;}
.col-5 {width: 41.66%;}
.col-6 {width: 50%;}
.col-7 {width: 58.33%;}
.col-8 {width: 66.66%;}
.col-9 {width: 75%;}
.col-10 {width: 83.33%;}
.col-11 {width: 91.66%;}
.col-12 {width: 100%;}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  [class*="col-"] {
    width: 100%;
  }
}
```
{% endcode %}

### Har doim mobile first uchun dizayn qiling

Mobile First - sahifa dizaynini uy kompyuteri yoki boshqa qurilmalar uchun moslashtirishdan avval mobil qurilamalar uchun moslashtirilgan dizayn tuzishni anglatadi (bu sahifani kichikroq qurilmalarda tezroq ko'rsatishga yordam beradi).

Bu CSS-ga ba'zi o'zgartirishlar kiritishimiz kerakligini anglatadi.

Kenglik **768px** dan _kichkina_ bo'lganda stillarni o'zgartirish o'rniga, 768px dan _katta bo'lganda dizaynni o'zgartirishimiz kerak._ Bu bizning dizaynimizni mobile first qiladi:

```
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
  .col-1 {width: 8.33%;}
  .col-2 {width: 16.66%;}
  .col-3 {width: 25%;}
  .col-4 {width: 33.33%;}
  .col-5 {width: 41.66%;}
  .col-6 {width: 50%;}
  .col-7 {width: 58.33%;}
  .col-8 {width: 66.66%;}
  .col-9 {width: 75%;}
  .col-10 {width: 83.33%;}
  .col-11 {width: 91.66%;}
  .col-12 {width: 100%;}
}
```

### Boshqa bir breakpoint

Xohlaganingizcha breakpoint qo'shishingiz mumkin.

Keeling, planshetlar va mobil telefonlar o'rtasida breakpoint joylashtiramiz.

&#x20;                          Desktop                                                    Planshet                             Telefon\
![](https://www.w3schools.com/css/rwd\_desktop.png)                    ![](https://www.w3schools.com/css/rwd\_tablet.png)                    ![](https://www.w3schools.com/css/rwd\_phone.png)

Buni yana bir media querie (600px da) va 600px dan katta (lekin 768px dan kichik bo'lgan) qurilmalar uchun yangi classlar qoʻshish orqali amalga oshiramiz:

{% code title="E'tibor bering, ikkita class to'plami deyarli bir xil, farq faqat nomda ( col-va col-s-):" %}
```
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}

@media only screen and (min-width: 600px) {
  /* For tablets: */
  .col-s-1 {width: 8.33%;}
  .col-s-2 {width: 16.66%;}
  .col-s-3 {width: 25%;}
  .col-s-4 {width: 33.33%;}
  .col-s-5 {width: 41.66%;}
  .col-s-6 {width: 50%;}
  .col-s-7 {width: 58.33%;}
  .col-s-8 {width: 66.66%;}
  .col-s-9 {width: 75%;}
  .col-s-10 {width: 83.33%;}
  .col-s-11 {width: 91.66%;}
  .col-s-12 {width: 100%;}
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
  .col-1 {width: 8.33%;}
  .col-2 {width: 16.66%;}
  .col-3 {width: 25%;}
  .col-4 {width: 33.33%;}
  .col-5 {width: 41.66%;}
  .col-6 {width: 50%;}
  .col-7 {width: 58.33%;}
  .col-8 {width: 66.66%;}
  .col-9 {width: 75%;}
  .col-10 {width: 83.33%;}
  .col-11 {width: 91.66%;}
  .col-12 {width: 100%;}
}
```
{% endcode %}

Bir xil classlarning ikkita to'plami borligi g'alati tuyulishi mumkin, ammo bu _HTMLda_ har bir breakpointda ustunlar bilan nima sodir bo'lishini belgilash imkoniyatini beradi:

#### HTMLga misol

**PC uchun:**

Birinchi va uchinchi bo'limlarning har biri 3 ta ustundan iborat bo'ladi. O'rta qism 6 ta ustunni o'z ichiga oladi.

**Planshetlar uchun:**

Birinchi bo'lim 3 ta ustunni, ikkinchisi 9 ta ustunni, uchinchi bo'lim esa birinchi ikkita bo'lim ostida ko'rsatiladi va u 12 ta ustunni o'z ichiga oladi:

```
<div class="row">
  <div class="col-3 col-s-3">...</div>
  <div class="col-6 col-s-9">...</div>
  <div class="col-3 col-s-12">...</div>
</div>
```

### Oddiy qurilmalar uchun breakpointlar

Har hil balandlik va kenglikga ega ko'plab ekranlar va qurilmalar mavjud, shu sababli har bir qurilma uchun aniq bir breakpoint yaratish qiyin. Ishni soddalashtirish uchun beshta guruhni mo'ljal qilib olishingiz mumkin:

```
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...}
```

### Orientatsiya: portret / landshaft

Media querielar brauzer oynasining holatiga qarab sahifa layoutini o'zgartirish uchun ham ishlatilishi mumkin.

Brauzer oynasi o'zining balandligidan kattaroq bo'lganida qo'llaniladigan CSS xususiyatlarining to'plamiga ega bo'lishingiz mumkin, ya'ni "Landshaft" yo'nalishida:

{% code title="Orientatsiya landshaft rejimida bo'lsa, ochiq ko'k fon rangidan foydalaning:" %}
```
@media only screen and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}
```
{% endcode %}

### Media querielar bilan elementlarni yashirish

Media querielardan foydalanishning yana bir keng tarqalgan usuli ekran o'lchamlaridagi elementlarni yashirishdir:

<figure><img src="../.gitbook/assets/image (431).png" alt=""><figcaption></figcaption></figure>

```
/* If the screen size is 600px wide or less, hide the element */
@media screen and (max-width: 600px) {
  div.example {
    display: none;
  }
}
```

### Media querielar yordamida shrift o'lchamini o'zgartirish

Bundan tashqari, turli ekran o'lchamlaridagi elementning shrift o'lchamini o'zgartirish uchun media querielardan foydalanishingiz mumkin:

<figure><img src="../.gitbook/assets/image (742).png" alt=""><figcaption></figcaption></figure>

```
/* If screen size is more than 600px wide, set the font-size of <div> to 80px */
@media screen and (min-width: 600px) {
  div.example {
    font-size: 80px;
  }
}

/* If screen size is 600px wide, or less, set the font-size of <div> to 30px */
@media screen and (max-width: 600px) {
  div.example {
    font-size: 30px;
  }
}
```

### CSS @media reference

Barcha media turlari va funksiyalari/iboralari haqida toʻliq maʼlumot olish uchun <mark style="color:green;">CSS maʼlumotnomamizdagi @media qoidasi</mark>ga qarang.
