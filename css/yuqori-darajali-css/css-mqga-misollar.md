# CSS MQga misollar

### CSS media querielar - ko'proq misollar

Keling, media querielardan foydalanishning yana bir qancha misollarini ko'rib chiqaylik.

Media querielar turli qurilmalarga moslashtirilgan stilllar bilan ta'minlashning mashhur usulidir. Buning oddiy misolini ko'rsatib berish uchun turli qurilmalarning background rangini o'zgartiramiz:

<figure><img src="https://www.w3schools.com/css/mqcap.JPG" alt=""><figcaption></figcaption></figure>

```
/* Set the background color of body to tan */
body {
  background-color: tan;
}

/* On screens that are 992px or less, set the background color to blue */
@media screen and (max-width: 992px) {
  body {
    background-color: blue;
  }
}

/* On screens that are 600px or less, set the background color to olive */
@media screen and (max-width: 600px) {
  body {
    background-color: olive;
  }
}

```

{% hint style="warning" %}
Nima uchun aynan 992px va 600px dan foydalanayotganimizga hayron boʻldingizmi? Ular biz qurilmalar uchun "odatiy to'xtash nuqtalari" deb ataydigan o'lcham hisoblanadi. To'xtash nuqtalari haqida <mark style="color:green;">responsive veb-dizayn qo'llanma</mark>mizda batafsil o'qishingiz mumkin.
{% endhint %}

### Menyular uchun media querielar

Ushbu misolda turli ekran o'lchamlarida dizaynini o'zgartiruvchi moslashuvchan navbar yaratish uchun media querielardan foydalanamiz.

Katta ekranlar:                                                                           Kichik ekranlar:

<figure><img src="../../.gitbook/assets/image (461).png" alt=""><figcaption></figcaption></figure>

```
/* The navbar container */
.topnav {
  overflow: hidden;
  background-color: #333;
}

/* Navbar links */
.topnav a {
  float: left;
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* On screens that are 600px wide or less, make the menu links stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .topnav a {
    float: none;
    width: 100%;
  }
}
```

### Ustunlar uchun media querielar

Media querielardan keng tarqalgan foydalanish usuli moslashuvchan layout yaratishdir. Ushbu misolda turli ekran o'lchamlariga qarab to'rtta, ikkita va to'liq kenglikdagi ustunlar orasida o'zgarib turadigan layout yaratamiz:

<figure><img src="../../.gitbook/assets/image (398).png" alt=""><figcaption></figcaption></figure>

```
/* Create four equal columns that floats next to each other */
.column {
  float: left;
  width: 25%;
}

/* On screens that are 992px wide or less, go from four columns to two columns */
@media screen and (max-width: 992px) {
  .column {
    width: 50%;
  }
}

/* On screens that are 600px wide or less, make the columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column {
    width: 100%;
  }
}

```

{% hint style="warning" %}
**Maslahat:** Ustun layoutlarini yaratishning yanada zamonaviy usuli Flexbox-dan foydalanishdir (quyidagi misolga qarang). Biroq, u **Internet Explorer 10** va undan oldingi versiyalarda qo'llab-quvvatlanmaydi. Agar sizga **IE6-10**da ham ishlashi kerak bo'lsa, floatlardan foydalaning (yuqorida ko'rsatilganidek).

Flexible Box Layout moduli haqida batafsil ma'lumot olish uchun <mark style="color:green;">CSS Flexbox</mark> bo'limimizni o'qing.

Responsive veb-dizayn haqida batafsil ma'lumot olish uchun bizning Responsive veb-dizayn qo'llanmamizni o'qing.
{% endhint %}

```
/* Container for flexboxes */
.row {
  display: flex;
  flex-wrap: wrap;
}

/* Create four equal columns */
.column {
  flex: 25%;
  padding: 20px;
}

/* On screens that are 992px wide or less, go from four columns to two columns */
@media screen and (max-width: 992px) {
  .column {
    flex: 50%;
  }
}

/* On screens that are 600px wide or less, make the columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .row {
    flex-direction: column;
  }
}
```

### Media querielar bilan elementlarni yashirish

Media querielardan foydalanishning yana bir keng tarqalgan usuli ekran o'lchamlaridagi elementlarni yashirishdir:

<figure><img src="../../.gitbook/assets/image (431).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../.gitbook/assets/image (742).png" alt=""><figcaption></figcaption></figure>

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

### Moslashuvchan rasmlar galereyasi

Ushbu misolda moslashuvchan rasmlar galereyasini yaratish uchun flexbox bilan birgalikda media querielardan foydalandik:

<figure><img src="../../.gitbook/assets/image (417).png" alt=""><figcaption></figcaption></figure>

### Moslashuvchan veb-sayt

Ushbu misolda moslashuvchan navbar va moslashuvchan kontentni o'z ichiga olgan moslashuvchan veb-sayt yaratish uchun flexbox bilan birgalikda media querielardan foydalandik.

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

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

### Eng kichik kenglikdan eng katta kenglikka qarab

Minimal kenglik va maksimal kenglikni berish uchun .`(max-width:`` `_`..`_`)` va `(min-width:`` `_`..`_`)` qiymatlaridan ham foydalanishingiz mumkin.

Misol uchun, brauzer kengligi 600 va 900 piksel orasida bo'lsa, `<div>` elementining ko'rinishini o'zgartirish:

```
@media screen and (max-width: 900px) and (min-width: 600px) {
  div.example {
    font-size: 50px;
    padding: 50px;
    border: 8px solid black;
    background: yellow;
  }
}
```

**Qo'shimcha qiymatdan foydalanish:** Quyidagi misolda allaqachon mavjud media querielarimizga vergul orqali qo'shimcha media querie qo'shamiz (bu OR operatori kabi ishlaydi):

```
/* When the width is between 600px and 900px OR above 1100px - change the appearance of <div> */
@media screen and (max-width: 900px) and (min-width: 600px), (min-width: 1100px) {
  div.example {
    font-size: 50px;
    padding: 50px;
    border: 8px solid black;
    background: yellow;
  }
}
```

### CSS @media reference

Barcha media turlari va funksiyalari/iboralari haqida toʻliq maʼlumot olish uchun <mark style="color:green;">CSS maʼlumotnomamizdagi @media qoidasi</mark>ga qarang.

**Maslahat:** Media querielarda break pointlardan foydalanib moslashuvchan veb-dizayn tuzish (turli xil qurilmalar va ekranlarda qanday ko'rsatilishi) haqida batafsil maʼlumot olish uchun <mark style="color:green;">Responsive veb-dizayn</mark> boʻyicha oʻquv qoʻllanmamizni oʻqing.
