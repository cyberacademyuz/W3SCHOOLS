# SVG Ellipse

### SVG ellips - \<ellips>

\<ellips> elementi ellips yaratish uchun ishlatiladi.

Ellips aylana bilan chambarchas bog'liq. Farqi shundaki, ellips bir-biridan farq qiluvchi x va ay radiusiga ega, aylana esa teng x va y radiusga ega:

***

### 1-misol

Quyidagi misol ellips hosil qiladi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="140" width="500">\
&#x20; \<ellipse cx="200" cy="80" rx="100" ry="50"\
&#x20; style="fill:yellow;stroke:purple;stroke-width:2" />\
\</svg>

Kod tushuntirish:

* cx atributi ellips markazining x koordinatasini belgilaydi
* cy atributi ellips markazining y koordinatasini belgilaydi
* rx atributi gorizontal radiusni belgilaydi
* Ry atributi vertikal radiusni belgilaydi

***

***

### 2-misol

Quyidagi misol bir-birining ustiga uchta ellips hosil qiladi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="150" width="500">\
&#x20; \<ellipse cx="240" cy="100" rx="220" ry="30" style="fill:purple" />\
&#x20; \<ellipse cx="220" cy="70" rx="190" ry="20" style="fill:lime" />\
&#x20; \<ellipse cx="210" cy="45" rx="170" ry="15" style="fill:yellow" />\
\</svg>

***

### 3-misol

Quyidagi misol ikkita ellipsni birlashtiradi (bitta sariq va bitta oq):

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="100" width="500">\
&#x20; \<ellipse cx="240" cy="50" rx="220" ry="30" style="fill:yellow" />\
&#x20; \<ellipse cx="220" cy="50" rx="190" ry="20" style="fill:white" />\
\</svg>
