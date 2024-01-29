# O'yin Burilish

Qizil kvadrat aylanishi mumkin:

***

### Aylanadigan komponentlar

Ilgari ushbu qo'llanmada qizil kvadrat o'yin maydonida harakatlana oldi, lekin u aylana olmadi va aylana olmadi.

Komponentlarni aylantirish uchun biz komponentlarni chizish usulini o'zgartirishimiz kerak.

Tuval elementi uchun mavjud bo'lgan yagona aylantirish usuli butun tuvalni aylantiradi:

![](https://www.w3schools.com/graphics/rotate1.png)

Tuvalga chizgan boshqa hamma narsa nafaqat o'ziga xos komponentni emas, balki aylantiriladi.

Shuning uchun biz usulda ba'zi o'zgarishlar qilishimiz kerak `update()`:

Birinchidan, biz joriy tuval kontekst ob'ektini saqlaymiz:

`ctx.save();`

Keyin biz translate usulidan foydalanib, butun tuvalni muayyan komponentning markaziga o'tkazamiz:

`ctx.translate(x, y);`

![](https://www.w3schools.com/graphics/game\_movement1.png)

Keyin rotate() usuli yordamida kerakli aylanishni bajaramiz:

`ctx.rotate(`_`angle`_`);`

![](https://www.w3schools.com/graphics/game\_movement2.png)

Endi biz komponentni tuvalga chizishga tayyormiz, ammo endi biz uni tarjima qilingan (va aylantirilgan) tuvalning 0,0 pozitsiyasida markaziy holati bilan chizamiz:

`ctx.fillRect(width / -2, height / -2, width, height);`

![](https://www.w3schools.com/graphics/game\_movement3.png)

Tugatganimizdan so'ng, tiklash usulidan foydalanib, kontekst ob'ektini saqlangan holatiga qaytarishimiz kerak:

`ctx.restore();`

Komponent aylanadigan yagona narsa:

![](https://www.w3schools.com/graphics/game\_movement4.png)

***

***

### Komponent konstruktori

Konstruktorda `component`yangi xususiyat mavjud bo'lib `angle`, u komponentning burchagini ifodalovchi radian sondir.

`update`Konstruktorning usuli shundan `component`iboratki, biz komponentni chizamiz va bu erda komponentning aylanishiga imkon beradigan o'zgarishlarni ko'rishingiz mumkin:

#### Misol

function component(width, height, color, x, y) {\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; **this.angle = 0;**\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   **ctx.save();**\
&#x20;   **ctx.translate(this.x, this.y);**\
&#x20;   **ctx.rotate(this.angle);**\
&#x20;   ctx.fillStyle = color;\
&#x20;   **ctx.fillRect(this.width / -2, this.height / -2, this.width, this.height);**\
&#x20;   **ctx.restore();**\
&#x20; }\
}\
\
function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **myGamePiece.angle += 1 \* Math.PI / 180;**\
&#x20; myGamePiece.update();\
}
