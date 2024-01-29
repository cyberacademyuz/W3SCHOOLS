# SVG Path

### SVG yo'li - \<yo'l>

\<path> elementi yo'lni aniqlash uchun ishlatiladi.

Yo'l ma'lumotlari uchun quyidagi buyruqlar mavjud:

* M = harakat qilish
* L = lineto
* H = gorizontal chiziq
* V = vertikal chiziq
* C = egri chiziq
* S = silliq egri chiziq
* Q = kvadratik Bezier egri chizig'i
* T = silliq kvadratik Bezier egri chizig'i
* A = elliptik yoy
* Z = yaqin yo'l

Eslatma: Yuqoridagi barcha buyruqlar pastki harflar bilan ham ifodalanishi mumkin. Katta harflar mutlaq joylashtirilgan, kichik harflar nisbatan joylangan degan ma'noni anglatadi.

***

### 1-misol

Quyidagi misol 150,0 pozitsiyasidan boshlanadigan yo'lni 75,200 pozitsiyasiga, so'ngra u yerdan 225,200 gacha bo'lgan chiziqni va nihoyat yo'lni 150,0 ga yopadigan yo'lni belgilaydi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="210" width="400">\
&#x20; \<path d="M150 0 L75 200 L225 200 Z" />\
\</svg>

***

***

### 2-misol

Bezier egri chiziqlari cheksiz ravishda masshtablash mumkin bo'lgan silliq egri chiziqlarni modellashtirish uchun ishlatiladi. Odatda, foydalanuvchi ikkita so'nggi nuqta va bir yoki ikkita nazorat nuqtasini tanlaydi. Bitta nazorat nuqtasi bo'lgan Bezier egri chizig'i kvadratik Bezier egri chizig'i deb ataladi va ikkita nazorat nuqtasi bo'lgan tur kubik deb ataladi.

Quyidagi misol kvadratik Bezier egri chizig'ini yaratadi, bu erda A va C - boshlang'ich va yakuniy nuqtalar, B - nazorat nuqtasi:

&#x20;A B C Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="400" width="450">\
&#x20; \<path id="lineAB" d="M 100 350 l 150 -300" stroke="red"\
&#x20; stroke-width="3" fill="none" />\
&#x20; \<path id="lineBC" d="M 250 50 l 150 300" stroke="red"\
&#x20; stroke-width="3" fill="none" />\
&#x20; \<path d="M 175 200 l 150 0" stroke="green" stroke-width="3"\
&#x20; fill="none" />\
&#x20; \<path d="M 100 350 q 150 -300 300 0" stroke="blue"\
&#x20; stroke-width="5" fill="none" />\
&#x20; \<!-- Mark relevant points -->\
&#x20; \<g stroke="black" stroke-width="3" fill="black">\
&#x20;   \<circle id="pointA" cx="100" cy="350" r="3" />\
&#x20;   \<circle id="pointB" cx="250" cy="50" r="3" />\
&#x20;   \<circle id="pointC" cx="400" cy="350" r="3" />\
&#x20; \</g>\
&#x20; \<!-- Label the points -->\
&#x20; \<g font-size="30" font-family="sans-serif" fill="black" stroke="none"\
&#x20; text-anchor="middle">\
&#x20;   \<text x="100" y="350" dx="-30">A\</text>\
&#x20;   \<text x="250" y="50" dy="-10">B\</text>\
&#x20;   \<text x="400" y="350" dx="30">C\</text>\
&#x20; \</g>\
\</svg>

Kompleksmi? HA!!!! Chizish yo'llari murakkabligi sababli, murakkab grafiklarni yaratish uchun SVG muharriridan foydalanish tavsiya etiladi.
