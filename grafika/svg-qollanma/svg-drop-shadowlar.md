# SVG Drop Shadowlar

### \<defs> va \<filtr>

Barcha SVG filtrlari \<defs> elementida aniqlanadi. \<defs> elementi ta'riflar uchun qisqa va maxsus elementlarning (masalan, filtrlar) ta'rifini o'z ichiga oladi.

\<filtr> elementi SVG filtrini aniqlash uchun ishlatiladi. \<filtr> elementi filtrni identifikatsiya qiluvchi id atributiga ega. Keyin grafik foydalanish uchun filtrga ishora qiladi.

***

### SVG \<feOffset>

### 1-misol

\<feOffset> elementi soya effektlarini yaratish uchun ishlatiladi. G'oya SVG grafikasini (tasvir yoki element) olish va uni xy tekisligida bir oz harakatlantirishdir.

Birinchi misol to'rtburchakni ofset qiladi (\<feOffset> bilan), so'ngra asl nusxani ofset tasvirining tepasida aralashtiriladi (\<feBlend> bilan):

![feoffset](https://www.w3schools.com/graphics/svg\_feoffset.gif)

Mana SVG kodi:

#### Misol

\<svg height="120" width="120">\
&#x20; \<defs>\
&#x20;   \<filter id="f1" x="0" y="0" width="200%" height="200%">\
&#x20;     \<feOffset result="offOut" in="SourceGraphic" dx="20" dy="20" />\
&#x20;     \<feBlend in="SourceGraphic" in2="offOut" mode="normal" />\
&#x20;   \</filter>\
&#x20; \</defs>\
&#x20; \<rect width="90" height="90" stroke="green" stroke-width="3"\
&#x20; fill="yellow" filter="url(#f1)" />\
\</svg>

Kod tushuntirish:

* \<filtr> elementining id atributi filtr uchun noyob nomni belgilaydi
* \<rect> elementining filtr atributi elementni "f1" filtriga bog'laydi

***

***

### 2-misol

Endi ofset tasvirni xiralashtirish mumkin (\<feGaussianBlur> bilan):

![feoffset2](https://www.w3schools.com/graphics/svg\_feoffset2.jpg)

Mana SVG kodi:

#### Misol

\<svg height="140" width="140">\
&#x20; \<defs>\
&#x20;   \<filter id="f2" x="0" y="0" width="200%" height="200%">\
&#x20;     \<feOffset result="offOut" in="SourceGraphic" dx="20" dy="20" />\
&#x20;     \<feGaussianBlur result="blurOut" in="offOut" stdDeviation="10" />\
&#x20;     \<feBlend in="SourceGraphic" in2="blurOut" mode="normal" />\
&#x20;   \</filter>\
&#x20; \</defs>\
&#x20; \<rect width="90" height="90" stroke="green" stroke-width="3"\
&#x20; fill="yellow" filter="url(#f2)" />\
\</svg>

Kod tushuntirish:

* \<feGaussianBlur> elementining stdDeviation atributi loyqalik miqdorini belgilaydi.

***

### 3-misol

Endi soyani qora rangga aylantiring:

![feoffset3](https://www.w3schools.com/graphics/svg\_feoffset3.jpg)

Mana SVG kodi:

#### Misol

\<svg height="140" width="140">\
&#x20; \<defs>\
&#x20;   \<filter id="f3" x="0" y="0" width="200%" height="200%">\
&#x20;     \<feOffset result="offOut" in="SourceAlpha" dx="20" dy="20" />\
&#x20;     \<feGaussianBlur result="blurOut" in="offOut" stdDeviation="10" />\
&#x20;     \<feBlend in="SourceGraphic" in2="blurOut" mode="normal" />\
&#x20;   \</filter>\
&#x20; \</defs>\
&#x20; \<rect width="90" height="90" stroke="green" stroke-width="3"\
&#x20; fill="yellow" filter="url(#f3)" />\
\</svg>

Kod tushuntirish:

* \<feOffset> elementining in atributi butun RGBA pikseli o'rniga xiralashtirish uchun Alfa kanalidan foydalanadigan "SourceAlpha" ga o'zgartiriladi.

***

### 4-misol

Endi soyani rang sifatida ko'rib chiqing:

![feoffset4](https://www.w3schools.com/graphics/svg\_feoffset4.jpg)

Mana SVG kodi:

#### Misol

\<svg height="140" width="140">\
&#x20; \<defs>\
&#x20;   \<filter id="f4" x="0" y="0" width="200%" height="200%">\
&#x20;     \<feOffset result="offOut" in="SourceGraphic" dx="20" dy="20" />\
&#x20;     \<feColorMatrix result="matrixOut" in="offOut" type="matrix"\
&#x20;     values="0.2 0 0 0 0 0 0.2 0 0 0 0 0 0.2 0 0 0 0 0 1 0" />\
&#x20;     \<feGaussianBlur result="blurOut" in="matrixOut" stdDeviation="10" />\
&#x20;     \<feBlend in="SourceGraphic" in2="blurOut" mode="normal" />\
&#x20;   \</filter>\
&#x20; \</defs>\
&#x20; \<rect width="90" height="90" stroke="green" stroke-width="3"\
&#x20; fill="yellow" filter="url(#f4)" />\
\</svg>

Kod tushuntirish:

* \<feColorMatrix> filtri ofset tasviridagi ranglarni qora rangga yaqinlashtirish uchun ishlatiladi. Matritsadagi "0,2" ning uchta qiymati qizil, yashil va ko'k kanallarga ko'paytiriladi. Ularning qiymatlarini kamaytirish ranglarni qora rangga yaqinlashtiradi (qora 0 ga teng)
