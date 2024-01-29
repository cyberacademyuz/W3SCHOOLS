# O'yin Harakatlanish

O'yinni aylantirish bobida tushuntirilgan komponentlarni chizishning yangi usuli bilan harakatlar yanada moslashuvchan.

***

### Ob'ektlarni qanday ko'chirish kerak?

`speed`Konstruktorga `component`komponentning joriy tezligini ifodalovchi xususiyat qo'shing .

Shuningdek, usulda ba'zi o'zgarishlar qiling `newPos()`, komponentning o'rnini hisoblash uchun, `speed`va asosida `angle`.

Odatiy bo'lib, komponentlar yuqoriga qaratiladi va tezlik xususiyatini 1 ga o'rnatish orqali komponent oldinga siljiy boshlaydi.

#### Misol

function component(width, height, color, x, y) {\
&#x20; this.gamearea = gamearea;\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.angle = 0;\
&#x20; **this.speed = 1;**\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   ctx.save();\
&#x20;   ctx.translate(this.x, this.y);\
&#x20;   ctx.rotate(this.angle);\
&#x20;   ctx.fillStyle = color;\
&#x20;   ctx.fillRect(this.width / -2, this.height / -2, this.width, this.height);\
&#x20;   ctx.restore();\
&#x20; }\
&#x20; **this.newPos = function() {**\
&#x20;   **this.x += this.speed \* Math.sin(this.angle);**\
&#x20;   **this.y -= this.speed \* Math.cos(this.angle);**\
&#x20; **}**\
}\


***

***

### Burilishlar qilish

Shuningdek, biz chapga va o'ngga burilishni xohlaymiz. `moveAngle`Joriy harakat qiymatini yoki aylanish burchagini ko'rsatadigan yangi xususiyat yarating . Usulda mulk asosida `newPos()`hisoblang :`anglemoveAngle`

#### Misol

Moveangle xususiyatini 1 ga o'rnating va nima sodir bo'lishini ko'ring:

function component(width, height, color, x, y) {\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.angle = 0;\
&#x20; **this.moveAngle = 1;**\
&#x20; this.speed = 1;\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   ctx.save();\
&#x20;   ctx.translate(this.x, this.y);\
&#x20;   ctx.rotate(this.angle);\
&#x20;   ctx.fillStyle = color;\
&#x20;   ctx.fillRect(this.width / -2, this.height / -2, this.width, this.height);\
&#x20;   ctx.restore();\
&#x20; }\
&#x20; this.newPos = function() {\
&#x20;   **this.angle += this.moveAngle \* Math.PI / 180;**\
&#x20;   this.x += this.speed \* Math.sin(this.angle);\
&#x20;   this.y -= this.speed \* Math.cos(this.angle);\
&#x20; }\
}\


### Klaviaturadan foydalaning

Klaviaturadan foydalanganda qizil kvadrat qanday harakat qiladi? Yuqoriga va pastga, yonma-yon yonma-yon harakat qilish o'rniga, qizil kvadrat "yuqoriga" o'qni ishlatganda oldinga siljiydi va chap va o'ng o'qlarni bosganda chapga va o'ngga aylanadi.
