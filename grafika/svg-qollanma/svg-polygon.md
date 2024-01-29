# SVG Polygon

### SVG ko'pburchak - \<ko'pburchak>

\<poligon> elementi kamida uchta tomonni o'z ichiga olgan grafik yaratish uchun ishlatiladi.

Ko'pburchaklar to'g'ri chiziqlardan iborat bo'lib, shakli "yopiq" (barcha chiziqlar birlashadi).

Poligon yunon tilidan keladi. "Poly" "ko'p" va "gon" "burchak" degan ma'noni anglatadi.

***

### 1-misol

Quyidagi misol uch tomoni bo'lgan ko'pburchak hosil qiladi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="210" width="500">\
&#x20; \<polygon points="200,10 250,190 160,210" style="fill:lime;stroke:purple;stroke-width:1" />\
\</svg>

Kod tushuntirish:

* Points atributi ko'pburchakning har bir burchagi uchun x va y koordinatalarini belgilaydi

***

### 2-misol

Quyidagi misol to'rt tomoni bo'lgan ko'pburchak hosil qiladi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="250" width="500">\
&#x20; \<polygon points="220,10 300,210 170,250 123,234" style="fill:lime;stroke:purple;stroke-width:1" />\
\</svg>

***

***

### 3-misol

Yulduz yaratish uchun \<poligon> elementidan foydalaning:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="210" width="500">\
&#x20; \<polygon points="100,10 40,198 190,78 10,78 160,198"\
&#x20; style="fill:lime;stroke:purple;stroke-width:5;fill-rule:nonzero;" />\
\</svg>

***

### 4-misol

Fill-qoida xususiyatini "evenodd" ga o'zgartiring:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="210" width="500">\
&#x20; \<polygon points="100,10 40,198 190,78 10,78 160,198"\
&#x20; style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;" />\
\</svg>
