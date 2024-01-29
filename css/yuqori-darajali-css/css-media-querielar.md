# CSS Media querielar

### CSS2da kiritilgan media turlar

CSS2da kiritilgan `@media` qoidasi har xil media turlari uchun turli stillar berish imkonini yaratdi.

**Masalan**: Kompyuter ekranlari uchun, printerlar uchun, portativ qurilmalar uchun, televizor shaklidagi qurilmalar uchun alohida stillar berish mumkin.

Afsuski, bu media turlari boshqa print media vositalariga qaraganda boshqa qurilmalar tomonidan ko'pam qo'llab-quvvatlanmagan.

### CSS3da kiritilgan media querielar

CSS3-dagi media querielar CSS2 media turlari g'oyasini kengaytirdi: qurilma turini aniqlash o'rniga, qurilmaning imkoniyatlariga qaraladi.

Media querielar ko'p narsalarni tekshirish uchun ishlatilishi mumkin, masalan:

* viewportning kengligi va balandligi
* qurilmaning kengligi va balandligi
* orientatsiya (planshet/telefon landscape rejimida yoki portret rejimidami ?)
* rezolyutsiya

Media querielardan foydalanish uy kompyuterlari, noutbuklar, planshetlar va mobil telefonlarga (masalan, iPhone va Android telefonlari) moslashtirilgan css berishning mashhur usuli hisoblanadi.

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar qoidani to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi `@media`.

| Xususiyat | Chrome | Firefox |     |     |     |
| --------- | ------ | ------- | --- | --- | --- |
| @media    | 21.0   | 9.0     | 3.5 | 4.0 | 9.0 |

### Media querielar sintaksisi

Media querielar media turidan iborat bo'lib, bir yoki bir nechta ifodalarni o'z ichiga olishi mumkin, ular true yoki false deb hisoblanadi.

```
@media not|only mediatype and (expressions) {
  CSS-Code;
}
```

Agar ko'rsatilgan media turi hujjat ko'rsatilayotgan qurilma turiga mos kelsa va media queriedagi barcha ifodalar to'g'ri bo'lsa, querie natijasi true bo'ladi. Media querie true bo'lsa, css qoidalariga rioya qilgan holda mos keladigan css kodlari qo'llaniladi.

Agar **only** yoki **not** operatorlaridan foydalanmasangiz, media turidan foydalanish ixtiyoriy va `all`dan foydalaniladi.

Shuningdek, turli xil medialar uchun xar xil stillarga ega bo'lishingiz mumkin:

```
<link rel="stylesheet" media="mediatype and|not|only (expressions)" href="print.css">
```

### CSS3 media turlari

| Qiymat | Ta'rif                                                |
| ------ | ----------------------------------------------------- |
| all    | Used for all media type devices                       |
| print  | Used for printers                                     |
| screen | Used for computer screens, tablets, smart-phones etc. |
| speech | Used for screenreaders that "reads" the page out loud |

### Media so'rovlariga oddiy misollar

Media so'rovlaridan foydalanishning bir usuli - uslublar jadvalingiz ichida muqobil CSS bo'limiga ega bo'lishdir.

Quyidagi misol, agar ko'rish oynasi kengligi 480 piksel yoki undan ko'p bo'lsa, fon rangi och yashil rangga o'zgartiriladi (agar ko'rish maydoni 480 pikseldan kam bo'lsa, fon rangi pushti bo'ladi):

```
@media screen and (min-width: 480px) {
  body {
    background-color: lightgreen;
  }
}
```

Quyidagi misol, agar ko'rish oynasi 480 piksel kengligida yoki kengroq bo'lsa, sahifaning chap tomoniga suzib yuradigan menyuni ko'rsatadi (agar ko'rish oynasi 480 pikseldan kam bo'lsa, menyu kontentning tepasida bo'ladi):

```
@media screen and (min-width: 480px) {
  #leftsidebar {width: 200px; float: left;}
  #main {margin-left: 216px;}
}
```

{% hint style="warning" %}
### Ko'proq Media so'roviga misollar

Media so'rovlari bo'yicha ko'proq misollar uchun keyingi sahifaga o'ting: [CSS MQ Examples](https://www-w3schools-com.translate.goog/css/css3\_mediaqueries\_ex.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) .
{% endhint %}

### CSS @media havolasi

Barcha media turlari va funksiyalari/iboralari haqida toʻliq maʼlumot olish uchun CSS maʼlumotnomamizdagi @media qoidasiga qarang .
