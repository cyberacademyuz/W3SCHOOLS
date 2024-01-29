# SVG To'rtburchak

### SVG shakllari

SVG-da ishlab chiquvchilar foydalanishi mumkin bo'lgan oldindan belgilangan shakl elementlari mavjud:

* To'rtburchak \<to'g'ri>
* Doira \<doira>
* Ellips \<ellips>
* \<chiziq> qatori
* Polyline \<poliline>
* Ko'pburchak \<ko'pburchak>
* Yo'l \<yo'l>

Keyingi boblarda to'g'ri elementdan boshlab har bir element tushuntiriladi.

***

### SVG to'rtburchak - \<to'g'ri>

### 1-misol

\<rect> elementi to'rtburchak va to'rtburchak shaklining o'zgarishlarini yaratish uchun ishlatiladi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg width="400" height="110">\
&#x20; \<rect width="300" height="100" style="fill:rgb(0,0,255);stroke-width:3;stroke:rgb(0,0,0)" />\
\</svg>

Kod tushuntirish:

* \<rect> elementining kengligi va balandligi atributlari to'rtburchakning balandligi va kengligini belgilaydi.
* Style atributi to'rtburchak uchun CSS xususiyatlarini aniqlash uchun ishlatiladi
* CSS to'ldirish xususiyati to'rtburchakning to'ldirish rangini belgilaydi
* CSS stroke-width xususiyati to'rtburchaklar chegarasining kengligini belgilaydi
* CSS kontur xususiyati to'rtburchaklar chegarasining rangini belgilaydi

***

***

### 2-misol

Keling, ba'zi yangi atributlarni o'z ichiga olgan boshqa misolni ko'rib chiqaylik:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg width="400" height="180">\
&#x20; \<rect x="50" y="20" width="150" height="150"\
&#x20; style="fill:blue;stroke:pink;stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" />\
\</svg>

Kod tushuntirish:

* x atributi to'rtburchakning chap holatini belgilaydi (masalan, x="50" to'rtburchakni chap chetidan 50 piksel masofada joylashtiradi)
* y atributi to'rtburchakning yuqori o'rnini belgilaydi (masalan, y = "20" to'rtburchakni yuqori chetidan 20 pikselga joylashtiradi)
* CSS to'ldirish-shaffoflik xususiyati to'ldirish rangining shaffofligini belgilaydi (huquqiy diapazon: 0 dan 1 gacha)
* CSS stroke-opacity xususiyati chiziq rangining shaffofligini belgilaydi (huquqiy diapazon: 0 dan 1 gacha)

***

### 3-misol

Butun element uchun shaffoflikni aniqlang:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg width="400" height="180">\
&#x20; \<rect x="50" y="20" width="150" height="150"\
&#x20; style="fill:blue;stroke:pink;stroke-width:5;opacity:0.5" />\
\</svg>

Kod tushuntirish:

* CSS noaniqlik xususiyati butun element uchun shaffoflik qiymatini belgilaydi (huquqiy diapazon: 0 dan 1 gacha)

***

### 4-misol

Oxirgi misol, burchaklari yumaloq bo'lgan to'rtburchaklar yarating:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg width="400" height="180">\
&#x20; \<rect x="50" y="20" rx="20" ry="20" width="150" height="150"\
&#x20; style="fill:red;stroke:black;stroke-width:5;opacity:0.5" />\
\</svg>

Kod tushuntirish:

* rx va ry atributlari to'rtburchak burchaklarini yaxlitlaydi
