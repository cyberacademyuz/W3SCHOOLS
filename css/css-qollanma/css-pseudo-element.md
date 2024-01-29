# CSS Pseudo-element

### Psevdo-elementlar nima ? <a href="#psevdo-elementlar-nima" id="psevdo-elementlar-nima"></a>

CSSdagi Pseudo-elementlar elementning ma'lum qismlariga stil berish uchun ishlatiladi

Misol uchun:

* Elementning ichidagi birinchi qator yoki birinchi harfga stil berish
* Elementning kontentidan oldin yoki keyin yana nimadur qo'shish

### Sintaksis <a href="#sintaksis" id="sintaksis"></a>

Pseudo-elementlarning sintaksisi:

```
selector::pseudo-element {
  property: value;
}
```

### ::first-line pseudo elementi <a href="#first-line-psevdo-elementi" id="first-line-psevdo-elementi"></a>

`::first-line` pseudo-elementi matnning birinchi qatoriga stil berish uchun ishlatiladi.

Quyidagi misolda barcha `<p>` elementlaridagi matnning birinchi qatoriga stil berilyapti:

```
p::first-line {
  color: #ff0000;
  font-variant: small-caps;
}
```

**Eslatma:** `::first-line` pseudo elementi faqat block darajasidagi elementda ishlaydi.

Quyidagi xususiyatlardan `::first-line` pseudo elementida foydalanish mumkin

* shrift xususiyatlaridan
* Rang xususiyatlaridan
* orqafon xususiyatlaridan
* word-spacing
* letter-spacing
* text-decoration
* vertical-align
* text-transform
* line-height
* clear

{% hint style="warning" %}
**IIkki nuqta belgisiga e'tibor bering** **-** `::first-line` va `:first-line`



Psevdo elementlar CSS3 da pseudo classlardan ajralib turishi uchun W3C tomonidan bittalik ikki nuqta, ikkitalik ikki nuqtaga almashtirilgan



Bittalik ikki nuqta sintaksisi CSS1 va CSS2da pseudo elementlarda ham, pseudo classlarda ham ishlatilgan.



Eski versiyadan foydalanayotgan bo’lsangiz bittalik ikki nuqtadan foydalanish muammo keltirib chiqarmaydi.
{% endhint %}

### ::first-letter Pseudo elementi <a href="#first-letter-psevdo-elementi" id="first-letter-psevdo-elementi"></a>

`::first-letter` pseudo elementi matndagi birinchi harfga maxsus still berish uchun ishlatiladi.

Quyidagi misolda barcha `<p>` elementlarining birinchi harfiga stil berilgan:

```
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}
```

**Eslatma:** `::first-letter` pseudo elementi faqat block elementlar uchun ishlatilishi mumkin.

Quyidagi xususiyatlardan `::first-letter` pseudo elementida foydalanish mumkin

* shrift xususiyatlaridan
* rang xususiyatlaridan
* orqafon xususiyatlaridan
* Margin xususiyatlaridan
* Padding xususiyatlaridan
* Border xususiyatlaridan
* text-decoration
* vertical-align (faqatgina float `none` bo’lganda)
* text-transform
* line-height
* float
* clear

### Pseudo elementlar va HTML classlari <a href="#psevdo-elementlar-va-html-klasslar" id="psevdo-elementlar-va-html-klasslar"></a>

Pseudo elementlarni HTML classlari bilan birga ishlatish mumkin

```
p.intro::first-letter {
  color: #ff0000;
  font-size: 200%;
}
```

Yuqoridagi misolda `class="intro"` li paragrafning birinchi harfi ekranga qizil va katta o'lchamda ko'rinadi.

### Bir nechta pseudo elementlarni bir vaqtda ishlatish <a href="#bir-nechta-psevdo-elementlarni-bir-vaqtda-ishlatish" id="bir-nechta-psevdo-elementlarni-bir-vaqtda-ishlatish"></a>

Bir qancha pseudo elementlarni bir vaqtni o’zida ishlatsa bo’ladi.

Quyidagi misolda xatboshining birinchi harfi xx-large shrift o'lchamida va qizil rangda bo'ladi. Qolgan birinchi qator ko’k rangda va kichkina harflarda bo’ladi. Paragrafning qolgan qismi standart shrift o'lchami va standart rangda qoladi.

```
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}

p::first-line {
  color: #0000ff;
  font-variant: small-caps;
}
```

### CSS - ::before pseudo elementi <a href="#css-before-psevdo-elementi" id="css-before-psevdo-elementi"></a>

`::before` pseudo elementi HTML elementining kontentidan oldin biror kontent qo’shishga yordam beradi.

Quyidagi misolda har bir `<h1>` elementining kontentidan oldin rasm joylashtiriladi.

```
h1::before {
  content: url(smiley.gif);
}
```

### CSS - ::after pseudo elementi <a href="#css-after-psevdo-elementi" id="css-after-psevdo-elementi"></a>

`::after` pseudo elementi HTML elementining kontentidan keyin biror kontent qo’shishga yordam beradi

Quyidagi misolda har bir `<h1>` elementining kontentidan keyin rasm joylashtiriladi.

```
h1::after {
  content: url(smiley.gif);
}
```

### CSS- ::marker pseudo elementi <a href="#css-marker-psevdo-elementi" id="css-marker-psevdo-elementi"></a>

`::marker` pseudo elementi ro'yhatdagi kichik qora rangli belgilarni o'zgartiradi

Quyidagi misolda ro'yhatdagi belgilarga still berilgan:

```
::marker { 
  color: red;
  font-size: 23px;
}
```

### CSS- ::selection pseudo elementi <a href="#css-selection-psevdo-elementi" id="css-selection-psevdo-elementi"></a>

`::selection` pseudo elementi elementning foydalanuvchi tomonidan tanlangan qismini belgilaydi.

Quyidagi CSS xususiyatlaridan `::selection` pseudo elementida foydalanish mumkin: `color`, background, `cursor` va `outline`.

Quyidagi misolda tanlangan matnning rangi qizil va orqafon ranggi sariq bo’ladi.

```
::selection {
  color: red; 
  background: yellow;
}
```

### CSSning barcha Pseudo Elementlari

| Selektor                                                                | Misol           | Misol ta'rifi                                                |
| ----------------------------------------------------------------------- | --------------- | ------------------------------------------------------------ |
| [::after](https://www.w3schools.com/cssref/sel\_after.asp)              | p::after        | Insert something after the content of each \<p> element      |
| [::before](https://www.w3schools.com/cssref/sel\_before.asp)            | p::before       | Insert something before the content of each \<p> element     |
| [::first-letter](https://www.w3schools.com/cssref/sel\_firstletter.asp) | p::first-letter | Selects the first letter of each \<p> element                |
| [::first-line](https://www.w3schools.com/cssref/sel\_firstline.asp)     | p::first-line   | Selects the first line of each \<p> element                  |
| [::marker](https://www.w3schools.com/cssref/sel\_marker.asp)            | ::marker        | Selects the markers of list items                            |
| [::selection](https://www.w3schools.com/cssref/sel\_selection.asp)      | p::selection    | Selects the portion of an element that is selected by a user |
