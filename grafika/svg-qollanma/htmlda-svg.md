# HTMLda SVG

***

S

VG elementlarini to'g'ridan-to'g'ri HTML sahifalaringizga joylashtirishingiz mumkin.

***

### SVG-ni to'g'ridan-to'g'ri HTML sahifalariga joylashtiring

Mana oddiy SVG grafigiga misol:

&#x20;Sorry, your browser does not support inline SVG.

va bu erda HTML kodi:

#### Misol

\<!DOCTYPE html>\
\<html>\
\<body>\
\
\<h1>My first SVG\</h1>\
\
\<svg width="100" height="100">\
&#x20; \<circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />\
\</svg>\
\
\</body>\
\</html>

SVG kodi tushuntirishi:

* SVG tasviri \<svg> elementi bilan boshlanadi
* \<svg> elementining kengligi va balandligi atributlari SVG tasvirining kengligi va balandligini belgilaydi.
* \<circle> elementi aylana chizish uchun ishlatiladi
* cx va cy atributlari aylana markazining x va y koordinatalarini belgilaydi. Agar cx va cy o'rnatilmagan bo'lsa, aylana markazi (0, 0) ga o'rnatiladi.
* r atributi aylana radiusini belgilaydi
* Chiziq va chiziq kengligi atributlari shakl konturi qanday ko'rinishini boshqaradi. Biz doira konturini 4px yashil "chegara" ga o'rnatdik.
* Fill atributi doira ichidagi rangga ishora qiladi. To'ldirish rangini sariq rangga o'rnatdik
* Yopuvchi \</svg> tegi SVG tasvirini yopadi

**Eslatma:** SVG XML-da yozilgani uchun barcha elementlar to'g'ri yopilishi kerak!
