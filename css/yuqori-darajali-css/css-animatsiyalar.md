# CSS Animatsiyalar

### CSS Animatsiyalari <a href="#css-animatsiyalari" id="css-animatsiyalari"></a>

CSS HTML elementlarini Javascript yoki Flashdan foydalanmay animatsiyalashtirish imkonini beradi.

&#x20;                                       ![](<../../.gitbook/assets/image (244).png>)

Ushbu bo'limda CSSning quyidagi xususiyatlari haqida o'rganasiz:

* `@keyframes`
* `animation-name`
* `animation-duration`
* `animation-delay`
* `animation-iteration-count`
* `animation-direction`
* `animation-timing-function`
* `animation-fill-mode`
* `animation`

### Brauzerning qo'llab quvvatlashi <a href="#brauzer-qollab-quvvatlashi" id="brauzer-qollab-quvvatlashi"></a>

Jadvaldagi raqamlar xususiyatni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Xususiyat                 | Chrome | Edge | Firefox | Safari | Opera |
| ------------------------- | ------ | ---- | ------- | ------ | ----- |
| @keyframes                | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |
| animation-name            | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |
| animation-duration        | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |
| animation-delay           | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |
| animation-iteration-count | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |
| animation-direction       | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |
| animation-timing-function | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |
| animation-fill-mode       | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |
| animation                 | 43.0   | 10.0 | 16.0    | 9.0    | 30.0  |

### CSS Animatsiyalari nima ? <a href="#css-animatsiyalari-ozi-nima" id="css-animatsiyalari-ozi-nima"></a>

Animatsiya elementni bir stildan boshqasiga asta-sekinlik bilan o'zgartirish imkonini beradi.

Istalgancha xususiyatlarini o'zingiz xohlagandek o'zgartirishingiz mumkin.

CSS animatsiyasidan foydalanish uchun avval ba'zi animatsiya keyframelarini belgilashingiz kerak.

Keyframelar ma'lum bir vaqtlarda elementni qanday stillarga ega bo'lishini o'zida saqlaydi.

### @keyframes qoidasi <a href="#keyframes-qoidasi" id="keyframes-qoidasi"></a>

`@keyframes` qoidasi ichida CSS stillarini berganingizda, animatsiya ma'lum bir vaqt oralig'ida elementning stillarini asta-sekinlik bilan yangi stillarga o'zgaradi.

Animatsiyani ishga tushirish uchun uni elementga bog'lashingiz kerak.

Quyidagi misolda "example" animatsiyasi `<div>` elementiga bog'lanadi. Animatsiya 4 soniya davom etadi va u `<div>` elementining background rangini asta-sekin "qizil"dan "sariq"ga o'zgartiradi:

```
 /* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
} 
```

**Eslatma**: `animation-duration` xususiyati animatsiyani qancha vaqtda bajarilishi kerakligini belgilaydi. `animation-duration` xususiyati berilmagan bo'lsa, hech qanday animatsiya sodir bo'lmaydi, chunki uning standart qiymat 0s (0 soniya).

Yuqoridagi misolda still qachon o'zgarishini "**from**" va "**to**" kalit so'zlari (bu 0% (boshlash) va 100% (tugash)) orqali belgiladik.

Bundan tashqari, foizlardan foydalanish mumkin. Foizdan foydalanib, istalgancha still o'zgarishlarini qo'shishingiz mumkin.

Ushbu misoldagi animatsiya 25% bo'lganida \<div> elementining orqafonidagi qizil rangni sariq rangga, 50% bo'lganida ko'k rangga, 100% bolganida esa yashil rangga o'zgartiradi.&#x20;

```
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```

Ushbu misoldagi animatsiya 25%, 50% va 100% bo'lganida `<div>` elementining orqafon rangini va joylashuvini o'zgartiradi:

```
/* The animation code */
@keyframes example {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
} 
```

### Animatsiyani kechiktirish <a href="#animatsiyani-kechiktirish" id="animatsiyani-kechiktirish"></a>

`animation-delay` xususiyati animatsiya boshlanishini kechikishni belgilaydi.

Quyidagi misolda animatsiyani boshlashdan avval 2 soniya kutiladi:

<pre><code><strong>div {
</strong>  width: 100px;
<strong>  height: 100px;
</strong>  position: relative;
<strong>  background-color: red;
</strong>  animation-name: example;
<strong>  animation-duration: 4s;
</strong>  animation-delay: 2s;
<strong>}
</strong></code></pre>

Manfiy qiymatlarga ham ruxsat beriladi. Agar manfiy qiymatlardan foydalansangiz, animatsiya allaqachon N soniya vaqt o'tgandek boshlanadi.

Quyidagi misolda animatsiya allaqachon 2 soniya vaqt harakatlangandek boshlanadi:

<pre><code><strong>div {
</strong>  width: 100px;
<strong>  height: 100px;
</strong>  position: relative;
<strong>  background-color: red;
</strong>  animation-name: example;
<strong>  animation-duration: 4s;
</strong>  animation-delay: -2s;
<strong>}
</strong></code></pre>

### Animatsiya necha marta ishlashi kerakligini belgilash <a href="#animatsiya-necha-marta-ishlashi-kerakligini-belgilash" id="animatsiya-necha-marta-ishlashi-kerakligini-belgilash"></a>

`animation-iteration-count` xususiyati animatsiya necha marta ishga tushishi kerakligini belgilaydi.

Quyidagi misolda animatsiya 3 marta ishlab to'xtaydi:

<pre><code><strong>div {
</strong>  width: 100px;
<strong>  height: 100px;
</strong>  position: relative;
<strong>  background-color: red;
</strong>  animation-name: example;
<strong>  animation-duration: 4s;
</strong>  animation-iteration-count: 3;
<strong>}
</strong></code></pre>

Quyidagi misolda animatsiya to'xtamasdan davom etishi uchun "infinite" qiymatidan foydalanilgan:

<pre><code>div {
  width: 100px;
<strong>  height: 100px;
</strong>  position: relative;
<strong>  background-color: red;
</strong>  animation-name: example;
<strong>  animation-duration: 4s;
</strong>  animation-iteration-count: infinite;
<strong>}
</strong></code></pre>

### Animatsiyani teskari yo'nalishda yoki alternate shaklda harakatlantirish <a href="#animatsiyani-teskari-yonalishda-yoki-alternativ-sikllarda-ishga-tushirish" id="animatsiyani-teskari-yonalishda-yoki-alternativ-sikllarda-ishga-tushirish"></a>

`animation-direction` xususiyati animatsiyani oldinga, orqaga yoki alternate shaklda harakatlantirish kerakligini belgilaydi.

`animation-direction` xususiyati quyidagi qiymatlarni o'z ichiga oladi:

* `normal` - Animatsiya odatdagidek harakatlanadi (oldinga). Standart
* `reverse` - Animatsiya teskari yo'nalishda harakatlanadi (orqaga)
* `alternate` - Animatsiya avval oldinga, keyin esa orqaga harakatlanadi
* `alternate-reverse` - Animatsiya avval orqaga, keyin oldinga qarab harakatlanadi

Quyidagi misolda animatsiya teskari yo'nalishda (orqaga) harakatlantiriladi:

```
 div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-direction: reverse;
}
```

Quyidagi misolda animatsiya avval oldinga, keyin esa orqaga harakatlanishi uchun "alternate" qiymatidan foydalaniladi:

```
 div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate;
}
```

Quyidagi misolda animatsiyani avval orqaga, keyin oldinga yo‘naltirish uchun “alternate-reverse” qiymatidan foydalaniladi:

```
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate-reverse;
}
```

### Animatsiyaning curve tezligini belgilash <a href="#animatsiya-tezligi-curve-chizigini-belgilash" id="animatsiya-tezligi-curve-chizigini-belgilash"></a>

`animation-timing-function` xususiyati animatsiyaning curve tezligini belgilaydi.

`animation-timing-function` xususiyati quyidagi qiymatlarga ega bo'lishi mumkin:

* `ease` - sekin boshlanib, keyin tezlashadi va ohirida sekin to'xtaydigan animatsiyani belglaydi (bu standart)
* `linear` - boshidan oxirigacha bir xil tezlikdagi animatsiyani belglaydi
* `ease-in` - sekin boshlanadigan animatsiyani belglaydi
* `ease-out` - sekin tugaydigan animatsiyani belglaydi
* `ease-in-out` - sekin boshlanib va sekin tugaydigan animatsiyani belglaydi
* `cubic-bezier(n,n,n,n)` - cubic-bezier funksiyasi o'zingiz istagan qiymatlarni berish imkonini beradi

Quyidagi misolda foydalanish mumkin bo'lgan har xil curve tezliklari  ko'rsatilgan:

```
#div1 {animation-timing-function: linear;}
#div2 {animation-timing-function: ease;}
#div3 {animation-timing-function: ease-in;}
#div4 {animation-timing-function: ease-out;}
#div5 {animation-timing-function: ease-in-out;}
```

### Animatsiya uchun fill-modeni belgilash <a href="#animatsiya-uchun-toldirish-rejimini-belgilash" id="animatsiya-uchun-toldirish-rejimini-belgilash"></a>

CSS animatsiyalari elementga birinchi keyframe bajarilishidan avval yoki oxirgi keyframe bajarilishidan keyin taʼsir qilmaydi. Animatsiyaning `fill-mode` xususiyati bu narsani bekor qiladi.

`animation-fill-mode` xususiyati animatsiya bajarilmayotganda (boshlanishidan oldin, tugagandan keyin yoki ikkalasida ham) elementga still beradi.

`animation-fill-mode` xususiyati quyidagi qiymatlarga ega bo'lishi mumkin:

* `none` - Standart qiymat. Animatsiya bajarilgunga qadar yoki bajarilgandan keyin elementga hech qanday still bermaydi
* `forwards` - Element oxirgi keyframe tomonidan berilgan stillarni saqlab qoladi (`animation-direction` va `animation-iteration-count` ga bog'liq)
* `backwards` - Element birinchi keyframe tomonidan berilgan stillarni oladi(`animation-direction`ga bog'liq) va buni `animation-delay` paytida saqlab qoladi.
* `both` - Animatsiya ikkala yo'nalishda ham animatsiya xususiyatlarini kengaytirib, oldinga va orqaga harakat qilish qoidalariga amal qiladi.

Quyidagi misolda `<div>` elementiga animatsiya tugashi bilan oxirgi keyframe stillarini saqlab qolish imkoni beriladi:

```
 div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-fill-mode: forwards;
}
```

Quyidagi misolda `<div>` elementiga animatsiya boshlanishidan oldin (animatsiya kechikish paytida) birinchi keyframe tomonidan berilgan still qiymatlarini olish imkoni beriladi:

```
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: backwards;
}
```

Quyidagi misolda `<div>` elementiga animatsiya boshlanishidan oldin birinchi keyframe tomonidan berilgan still qiymatlarini olish va animatsiya tugashi bilan oxirgi keyframe tomonidan berilgan still qiymatlarini saqlab qolish imkoni beriladi:

```
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: both;
}
```

### animation qisqartma xususiyati <a href="#animatsiya-qisqartma-xususiyati" id="animatsiya-qisqartma-xususiyati"></a>

Quyidagi misolda oltita animatsiya xususiyatidan foydalaniladi:

```
div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```

Yuqoridagi kabi animatsiya effektini `animation` xususiyati orqali amalga oshirish mumkin:

```
div {
  animation: example 5s linear 2s infinite alternate;
}
```

### CSSning animatsiya xususiyatlari <a href="#css-animatsiya-xususiyatlari" id="css-animatsiya-xususiyatlari"></a>

Quyidagi jadvalda `@keyframes` qoidasi va CSSning barcha  animatsiya xususiyatlari keltirilgan:

| Xususiyat                                                                                             | Ta'rif                                                                                                                    |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| [@keyframes](https://www.w3schools.com/cssref/css3\_pr\_animation-keyframes.asp)                      | Animatsiya kodini belgilaydi                                                                                              |
| [animation](https://www.w3schools.com/cssref/css3\_pr\_animation.asp)                                 | Barcha animatsiya xususiyatlarini o'rnatish uchun qisqartma xususiyati                                                    |
| [animation-delay](https://www.w3schools.com/cssref/css3\_pr\_animation-delay.asp)                     | Animatsiya boshlanishidan oldingi kechikishni belgilaydi                                                                  |
| [animation-direction](https://www.w3schools.com/cssref/css3\_pr\_animation-direction.asp)             | Animatsiya oldinga, orqaga yoki alternativ sikllarda ijro etilishi kerakligini belgilaydi                                 |
| [animation-duration](https://www.w3schools.com/cssref/css3\_pr\_animation-duration.asp)               | Animatsiya bir siklni bajarish uchun qancha vaqt ketishi kerakligini belgilaydi                                           |
| [animation-fill-mode](https://www.w3schools.com/cssref/css3\_pr\_animation-fill-mode.asp)             | Animatsiya ishlamayotganda element uchun uslubni belgilaydi (u boshlanishidan oldin, tugaganidan keyin yoki ikkalasi ham) |
| [animation-iteration-count](https://www.w3schools.com/cssref/css3\_pr\_animation-iteration-count.asp) | Animatsiya necha marta ijro etilishi kerakligini belgilaydi                                                               |
| [animation-name](https://www.w3schools.com/cssref/css3\_pr\_animation-name.asp)                       | @keyframes animatsiyasi nomini belgilaydi                                                                                 |
| [animation-play-state](https://www.w3schools.com/cssref/css3\_pr\_animation-play-state.asp)           | Animatsiya ishlayotgan yoki to'xtatilganligini belgilaydi                                                                 |
| [animation-timing-function](https://www.w3schools.com/cssref/css3\_pr\_animation-timing-function.asp) | Animatsiya tezligini curve chizig'ini belgilaydi                                                                          |
