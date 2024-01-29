# SVG Linearlar

### SVG gradientlari

Gradient - bu bir rangdan ikkinchisiga silliq o'tish. Bundan tashqari, bir xil elementga bir nechta rang o'tishlari qo'llanilishi mumkin.

SVG da ikkita asosiy gradient turi mavjud:

* Chiziqli
* Radial

***

### SVG Lineer Gradient - \<linearGradient>

\<linearGradient> elementi chiziqli gradientni aniqlash uchun ishlatiladi.

\<linearGradient> elementi \<defs> tegi ichiga joylashtirilishi kerak. \<defs> tegi ta'riflar uchun qisqa va maxsus elementlarning (masalan, gradientlar) ta'rifini o'z ichiga oladi.

Chiziqli gradientlar gorizontal, vertikal yoki burchakli gradientlar sifatida belgilanishi mumkin:

* Gorizontal gradientlar y1 va y2 teng va x1 va x2 farq qilganda yaratiladi.
* Vertikal gradientlar x1 va x2 teng va y1 va y2 farq qilganda yaratiladi.
* Burchak gradientlari x1 va x2 farq qilganda va y1 va y2 farq qilganda yaratiladi.

***

### 1-misol

Sariqdan qizilgacha gorizontal chiziqli gradientli ellipsni aniqlang:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="150" width="400">\
&#x20; \<defs>\
&#x20;   \<linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">\
&#x20;     \<stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" />\
&#x20;     \<stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" />\
&#x20;   \</linearGradient>\
&#x20; \</defs>\
&#x20; \<ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad1)" />\
\</svg>

Kod tushuntirish:

* \<linearGradient> tegining id atributi gradient uchun noyob nomni belgilaydi
* \<linearGradient> tegining x1, x2, y1,y2 atributlari gradientning boshlanish va tugash holatini belgilaydi.
* Gradient uchun rang diapazoni ikki yoki undan ortiq rangdan iborat bo'lishi mumkin. Har bir rang \<stop> tegi bilan belgilanadi. Ofset atributi gradient rangi qayerda boshlanishi va tugashini aniqlash uchun ishlatiladi
* Fill atributi ellips elementini gradient bilan bog'laydi

***

***

### 2-misol

Sariqdan qizilgacha vertikal chiziqli gradientli ellipsni aniqlang:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="150" width="400">\
&#x20; \<defs>\
&#x20;   \<linearGradient id="grad2" x1="0%" y1="0%" x2="0%" y2="100%">\
&#x20;     \<stop offset="0%" style="stop-color:rgb(255,0,0);stop-opacity:1" />\
&#x20;     \<stop offset="100%" style="stop-color:rgb(255,255,0);stop-opacity:1" />\
&#x20;   \</linearGradient>\
&#x20; \</defs>\
&#x20; \<ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad2)" />\
\</svg>

***

### 3-misol

Sariqdan qizilgacha gorizontal chiziqli gradientli ellipsni aniqlang va ellips ichiga matn qo'shing:

&#x20;SVG Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="150" width="400">\
&#x20; \<defs>\
&#x20;   \<linearGradient id="grad3" x1="0%" y1="0%" x2="100%" y2="0%">\
&#x20;     \<stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" />\
&#x20;     \<stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" />\
&#x20;   \</linearGradient>\
&#x20; \</defs>\
&#x20; \<ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad3)" />\
&#x20; \<text fill="#ffffff" font-size="45" font-family="Verdana" x="150" y="86">\
&#x20; SVG\</text>\
\</svg>

Kod tushuntirish:

* \<matn> elementi matn qo'shish uchun ishlatiladi
