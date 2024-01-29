# SVG Blur effektlari

### \<defs> va \<filtr>

Barcha internet SVG filtrlari \<defs> elementida belgilangan. \<defs> elementi ta'riflar uchun qisqa va maxsus elementlarning (masalan, filtrlar) ta'rifini o'z ichiga oladi.

\<filtr> elementi SVG filtrini aniqlash uchun ishlatiladi. \<filtr> elementi filtrni identifikatsiya qiluvchi id atributiga ega. Keyin grafik foydalanish uchun filtrga ishora qiladi.

***

### SVG \<feGaussianBlur>

### 1-misol

Xiralashtirish effektlarini yaratish uchun \<feGaussianBlur> elementidan foydalaniladi:

![fegaussian loyqalik](https://www.w3schools.com/graphics/svg\_fegaussianblur.jpg)

Mana SVG kodi:

#### Misol

\<svg height="110" width="110">\
&#x20; \<defs>\
&#x20;   \<filter id="f1" x="0" y="0">\
&#x20;     \<feGaussianBlur in="SourceGraphic" stdDeviation="15" />\
&#x20;   \</filter>\
&#x20; \</defs>\
&#x20; \<rect width="90" height="90" stroke="green" stroke-width="3"\
&#x20; fill="yellow" filter="url(#f1)" />\
\</svg>

Kod tushuntirish:

* \<filtr> elementining id atributi filtr uchun noyob nomni belgilaydi
* Loyqalik effekti \<feGaussianBlur> elementi bilan aniqlanadi
* in="SourceGraphic" qismi effekt butun element uchun yaratilganligini belgilaydi
* stdDeviation atributi xiralik miqdorini belgilaydi
* \<rect> elementining filtr atributi elementni "f1" filtriga bog'laydi
