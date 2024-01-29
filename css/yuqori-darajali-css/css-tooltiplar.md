---
description: CSS orqali tooltiplar yarating
---

# CSS Tooltiplar

### Demo: Tooltipga misollar <a href="#demo-tooltip-misollar" id="demo-tooltip-misollar"></a>

Ko'pincha foydalanuvchi sichqoncha ko'rsatgichini element ustida olib borganida biror narsa haqida qo'shimcha ma'lumot ko'rsatish uchun tooltip ishlatiladi:

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

### Sodda tooltip <a href="#sodda-tooltip" id="sodda-tooltip"></a>

Foydalanuvchi sichqonchani element ustida olib borganida paydo bo'ladigan tooltip yaratish:

```
<style>
/* Tooltip container */
.tooltip {
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted black; /* If you want dots under the hoverable text */
}

/* Tooltip text */
.tooltip .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  text-align: center;
  padding: 5px 0;
  border-radius: 6px;
 
  /* Position the tooltip text - see examples below! */
  position: absolute;
  z-index: 1;
}

/* Show the tooltip text when you mouse over the tooltip container */
.tooltip:hover .tooltiptext {
  visibility: visible;
}
</style>

<div class="tooltip">Hover over me
  <span class="tooltiptext">Tooltip text</span>
</div> 
```

#### Misolni tushuntirish: <a href="#misolni-tushuntirsak" id="misolni-tushuntirsak"></a>

**HTML**: Konteyner elementidan foydalaning (masalan, `<div>`) va unga "tooltip" klassini qo'shing. Foydalanuvchi sichqonchani ushbu `<div>` elementining ustiga olib borganida, u tooltip matnini ko'rsatadi.

Ko'rsatiladigan matnni `class="tooltiptext"` orqali inline element ichiga (masalan, `<span>`) joylashtiriladi.

**CSS**: tooltip classi tooltip matnini (`position: absolute`) joylashtirish uchun zarur bo'lgan `position:relative` dan foydalanadi. **Eslatma**: tooltip ni qanday joylashtirish haqida quyidagi misollarga qarang.

`tooltiptext` classi tooltip matnini saqlaydi. U standart holatda yashirin bo'ladi, sichqonchani kursori element ustiga olib borilganida ko'rinadi. Biz unga ba'zi oddiy stillarni ham qo'shdik: width 120px, background rangi qora, matn rangi oq, matnni o'rtaga joylashtirish va tepa pastga 5px padding.

CSSning `border-radius` xususiyati tooltip matniga yumaloq burchaklar qo'shish uchun ishlatiladi.

`:hover` selektori foydalanuvchi sichqonchani `class="tooltip"` li `<div>` elementi ustiga olib borganida, tooltip matnini ko'rsatish uchun ishlatiladi.

### Tooltiplar joylashuvi <a href="#pozitsiyalangan-tooltiplar" id="pozitsiyalangan-tooltiplar"></a>

Ushbu misolda tooltip hover qilinadigan matnning (`<div>`) o'ng tomoniga (`left:105%`) joylashtirilgan. Shuni ham yodda tutingki, `top:-5px` uni konteyner elementining o'rtasiga joylashtirish uchun ishlatiladi. Biz 5 raqamidan foydalanamiz, chunki tooltipning tepa va pastki qismida 5px padding bor. Agar uning paddingini ko'paytirsangiz, o'rtada qolishini ta'minlash uchun `top` xususiyatining qiymatini ham ko'paytiring. Xuddi shu narsa tooltipni chap tomonga joylashtirilishni istaganingizda ham amal qiladi.

#### O'ng tomondagi tooltip <a href="#ong-tomondagi-tooltip" id="ong-tomondagi-tooltip"></a>

```
.tooltip .tooltiptext {
  top: -5px;
  left: 105%;
}
```

<figure><img src="../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

#### Chap tomondagi tooltip <a href="#chap-tomondagi-tooltip" id="chap-tomondagi-tooltip"></a>

```
 .tooltip .tooltiptext {
  top: -5px;
  right: 105%;
}
```

<figure><img src="../../.gitbook/assets/image (656).png" alt=""><figcaption></figcaption></figure>

Tooltip tepada yoki pastda ko'rinishini istasangiz, quyidagi misollarni ko'rib chiqing. `margin-left` xususiyatiga -60px berganimizga e'tibor qiling. Bu hover qilinadigan matn tepasidagi yoki pastidagi tooltip matnini ortada ko'rinishi uchun qilingan. U tooltip kengligining yarmiga ega (120/2 = 60).

#### Tepada joylashgan tooltip <a href="#yuqorida-joylashgan-tooltip" id="yuqorida-joylashgan-tooltip"></a>

```
.tooltip .tooltiptext {
  width: 120px;
  bottom: 100%;
  left: 50%;
  margin-left: -60px; /* Use half of the width (120/2 = 60), to center the tooltip */
}
```

<figure><img src="../../.gitbook/assets/image (239).png" alt=""><figcaption></figcaption></figure>

#### Pastda joylashgan tooltip <a href="#pastda-joylashgan-tooltip" id="pastda-joylashgan-tooltip"></a>

```
.tooltip .tooltiptext {
  width: 120px;
  top: 100%;
  left: 50%;
  margin-left: -60px; /* Use half of the width (120/2 = 60), to center the tooltip */
}
```

<figure><img src="../../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure>

### Tooltip uchlari <a href="#tooltip-uchlari" id="tooltip-uchlari"></a>

Tooltipning ma'lum bir tomonida paydo bo'ladigan burchakni yaratish uchun, classda `::after` pseudo-elementi orqali `content` xususiyatidan foydalanib "bo'sh" kontent yarating. Bu tooltipni pufakchaga o'xshagan qiladi.

Ushbu misolda, tooltipning pastki qismiga burchak qo'shish ko'rsatilgan:

### Pastga qaragan burchak <a href="#pastki-uch" id="pastki-uch"></a>

```
.tooltip .tooltiptext::after {
  content: " ";
  position: absolute;
  top: 100%; /* At the bottom of the tooltip */
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: black transparent transparent transparent;
}
```

<figure><img src="../../.gitbook/assets/image (353).png" alt=""><figcaption></figcaption></figure>

#### Misolni tushuntirish: <a href="#misolni-tushuntirsak-2" id="misolni-tushuntirsak-2"></a>

Burchakni tooltipning pastki qismiga joylashtirish uchun `top:100%`dan foydalandik, shunda u tooltipning pastki qismida joylashadi. `left:50%` esa burchakni o'rtaga joylashtiradi.

**Eslatma:** `border-width` xususiyati burchak o'lchamini belgilaydi. Agar uni o'zgartiradigan bo'lsangiz unda `left` qiymatini ham o'zgaritirishingiz kerak. Shunda burchak o'rtada joylashadi.

`border-color` kontentni burchakga aylantirish uchun ishlatiladi. Biz tepa borderni qora, qolganini esa shaffof qildik. Agar hamma burchaklarga qora rang bersak, unda qop qora to'rtburchak hosil bo'ladi.

Quyidagi misolda tooltipning tepasiga burchak qo'shganmiz. Endi bu safar tepa borderni qora qilmasdan pastiki qismini qora qildik:

### Tepaga qaragan burchak <a href="#tepadagi-uch" id="tepadagi-uch"></a>

```
.tooltip .tooltiptext::after {
  content: " ";
  position: absolute;
  bottom: 100%;  /* At the top of the tooltip */
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: transparent transparent black transparent;
}
```

<figure><img src="../../.gitbook/assets/image (654).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda burchakni chap tomonga joylashtirishni qanday qilish ko'rsatilgan:

#### Chap tomonga qaragan burchak <a href="#chap-tomondagi-uch" id="chap-tomondagi-uch"></a>

```
 .tooltip .tooltiptext::after {
  content: " ";
  position: absolute;
  top: 50%;
  right: 100%; /* To the left of the tooltip */
  margin-top: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: transparent black transparent transparent;
}
```

<figure><img src="../../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda burchakni o'ng tomonga joylashtirishni qanday qilish ko'rsatilgan:

```
 .tooltip .tooltiptext::after {
  content: " ";
  position: absolute;
  top: 50%;
  left: 100%; /* To the right of the tooltip */
  margin-top: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: transparent transparent transparent black;
}
```

<figure><img src="../../.gitbook/assets/image (268).png" alt=""><figcaption></figcaption></figure>

### Fade In animatsiyasi (tooltip larda) <a href="#fade-in-animatsiyasi-tooltip-larda" id="fade-in-animatsiyasi-tooltip-larda"></a>

Agar tooltipni sekinlik bilan paydo bo'lishini xohlasangiz, unda `transition` va `opacity` xususiyatlaridan foydalanib, sodda animatsiya yasashingiz mumkin:

```
.tooltip .tooltiptext {
  opacity: 0;
  transition: opacity 1s;
}

.tooltip:hover .tooltiptext {
  opacity: 1;
}
```
