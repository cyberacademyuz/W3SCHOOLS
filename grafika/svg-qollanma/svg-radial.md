# SVG Radial

### SVG Radial Gradient - \<radialGradient>

Radial gradientni aniqlash uchun \<radialGradient> elementidan foydalaniladi.

\<radialGradient> elementi \<defs> tegi ichiga joylashtirilishi kerak. \<defs> tegi ta'riflar uchun qisqa va maxsus elementlarning (masalan, gradientlar) ta'rifini o'z ichiga oladi.

***

### 1-misol

Oqdan ko'kgacha radial gradientli ellipsni aniqlang:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="150" width="500">\
&#x20; \<defs>\
&#x20;   \<radialGradient id="grad1" cx="50%" cy="50%" r="50%" fx="50%" fy="50%">\
&#x20;     \<stop offset="0%" style="stop-color:rgb(255,255,255);\
&#x20;     stop-opacity:0" />\
&#x20;     \<stop offset="100%" style="stop-color:rgb(0,0,255);stop-opacity:1" />\
&#x20;   \</radialGradient>\
&#x20; \</defs>\
&#x20; \<ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad1)" />\
\</svg>

Kod tushuntirish:

* \<radialGradient> tegining id atributi gradient uchun noyob nomni belgilaydi
* cx, cy va r atributlari eng tashqi doirani, fx va fy esa eng ichki doirani belgilaydi.
* Gradient uchun rang diapazoni ikki yoki undan ortiq rangdan iborat bo'lishi mumkin. Har bir rang \<stop> tegi bilan belgilanadi. Ofset atributi gradient rangi qayerda boshlanishi va tugashini aniqlash uchun ishlatiladi
* Fill atributi ellips elementini gradient bilan bog'laydi

***

***

### 2-misol

Oqdan ko'kgacha radial gradientli boshqa ellipsni aniqlang:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="150" width="500">\
&#x20; \<defs>\
&#x20;   \<radialGradient id="grad2" cx="20%" cy="30%" r="30%" fx="50%" fy="50%">\
&#x20;     \<stop offset="0%" style="stop-color:rgb(255,255,255);\
&#x20;     stop-opacity:0" />\
&#x20;     \<stop offset="100%" style="stop-color:rgb(0,0,255);stop-opacity:1" />\
&#x20;   \</radialGradient>\
&#x20; \</defs>\
&#x20; \<ellipse cx="200" cy="70" rx="85" ry="55" fill="url(#grad2)" />\
\</svg>
