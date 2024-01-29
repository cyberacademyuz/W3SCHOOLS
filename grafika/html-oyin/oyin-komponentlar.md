# O'yin Komponentlar

O'yin maydoniga qizil kvadrat qo'shing:

***

### Komponent qo'shing

O'yin maydoniga komponentlar qo'shish imkonini beruvchi komponent konstruktorini yarating.

Ob'ekt konstruktori chaqiriladi `component`va biz birinchi komponentimizni yaratamiz, deb nomlangan `myGamePiece`:

#### Misol

**var myGamePiece;**\
\
function startGame() {\
&#x20; myGameArea.start();\
&#x20; **myGamePiece = new component(30, 30, "red", 10, 120);**\
}\
\
**function component(width, height, color, x, y) {**\
&#x20; **this.width = width;**\
&#x20; **this.height = height;**\
&#x20; **this.x = x;**\
&#x20; **this.y = y;**\
&#x20; **ctx = myGameArea.context;**\
&#x20; **ctx.fillStyle = color;**\
&#x20; **ctx.fillRect(this.x, this.y, this.width, this.height);**\
**}**

Komponentlar tashqi ko'rinishi va harakatlarini nazorat qilish uchun xususiyatlar va usullarga ega.

***

***

### Ramkalar

O'yinni harakatga tayyor qilish uchun biz displeyni soniyasiga 50 marta yangilaymiz, bu filmdagi kadrlarga o'xshaydi.

Birinchidan, deb nomlangan yangi funksiya yarating `updateGameArea()`.

Ob'ektda funktsiyani har 20 millisekundda (sekundiga 50 marta) `myGameArea`bajaradigan intervalni qo'shing . Shuningdek , butun tuvalni tozalaydigan `updateGameArea()`funktsiyani qo'shing .`clear()`

Konstruktorda komponentning chizmasini boshqarish uchun , `component`deb nomlangan funktsiyani qo'shing . `update()`

Funktsiya va usulini `updateGameArea()`chaqiradi .`clear()update()`

Natijada komponent sekundiga 50 marta chiziladi va tozalanadi:

#### Misol

var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   **this.interval = setInterval(updateGameArea, 20);**\
&#x20; },\
&#x20; **clear : function() {**\
&#x20;   **this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);**\
&#x20; **}**\
}\
\
function component(width, height, color, x, y) {\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; **this.update = function(){**\
&#x20;   ctx = myGameArea.context;\
&#x20;   ctx.fillStyle = color;\
&#x20;   ctx.fillRect(this.x, this.y, this.width, this.height);\
&#x20; **}**\
}\
\
**function updateGameArea() {**\
&#x20; **myGameArea.clear();**\
&#x20; **myGamePiece.update();**\
**}**

***

### Uni harakatga keltiring

Qizil kvadrat soniyada 50 marta chizilganligini isbotlash uchun o'yin maydonini har yangilaganimizda x o'rnini (gorizontal) bir pikselga o'zgartiramiz:

#### Misol

function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **myGamePiece.x += 1;**\
&#x20; myGamePiece.update();\
}\


***

### Nima uchun o'yin maydonini tozalash kerak?

Har bir yangilanishda o'yin maydonini tozalash kerak emasdek tuyulishi mumkin. Ammo, agar biz usulni tashlab qo'ysak `clear()`, komponentning barcha harakatlari oxirgi ramkada joylashgan joyning izini qoldiradi:

#### Misol

function updateGameArea() {\
&#x20; // myGameArea.clear();\
&#x20; **myGamePiece.x += 1;**\
&#x20; myGamePiece.update();\
}\


***

### O'lchamni o'zgartiring

Komponentning kengligi va balandligini boshqarishingiz mumkin:

#### Misol

10x140 pikselli to'rtburchak yarating:

function startGame() {\
&#x20; myGameArea.start();\
&#x20; myGamePiece = new component(**140**, **10**, "red", 10, 120);\
}

***

### Rangni o'zgartiring

Siz komponentning rangini boshqarishingiz mumkin:

#### Misol

function startGame() {\
&#x20; myGameArea.start();\
&#x20; myGamePiece = new component(30, 30, **"blue"**, 10, 120);\
}

Hex, rgb yoki rgba kabi boshqa rang qiymatlaridan ham foydalanishingiz mumkin:

#### Misol

function startGame() {\
&#x20; myGameArea.start();\
&#x20; myGamePiece = new component(30, 30, **"rgba(0, 0, 255, 0.5)"**, 10, 120);\
}

***

### Lavozimni o'zgartiring

Komponentlarni o'yin maydoniga joylashtirish uchun biz x va y koordinatalaridan foydalanamiz.

Tuvalning yuqori chap burchagida koordinatalar mavjud (0,0)

X va y koordinatalarini ko'rish uchun quyidagi o'yin maydoni ustiga sichqonchani bosing:

XY

Komponentlarni o'yin maydonining istalgan joyiga joylashtirishingiz mumkin:

#### Misol

function startGame() {\
&#x20; myGameArea.start();\
&#x20; myGamePiece = new component(30, 30, "red", **2**, **2**);\
}

***

### Ko'p komponentlar

O'yin maydoniga xohlaganingizcha ko'p komponentlarni qo'yishingiz mumkin:

#### Misol

**var redGamePiece, blueGamePiece, yellowGamePiece;**\
\
function startGame() {\
&#x20; **redGamePiece = new component(75, 75, "red", 10, 10);**\
&#x20; **yellowGamePiece = new component(75, 75, "yellow", 50, 60);**\
&#x20; **blueGamePiece = new component(75, 75, "blue", 10, 110);**\
&#x20; myGameArea.start();\
}\
\
function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **redGamePiece.update();**\
&#x20; **yellowGamePiece.update();**\
&#x20; **blueGamePiece.update();**\
}\


***

### Harakatlanuvchi komponentlar

Barcha uchta komponentni turli yo'nalishlarda harakatlantiring:

#### Misol

function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **redGamePiece.x += 1;**\
&#x20; **yellowGamePiece.x += 1;**\
&#x20; **yellowGamePiece.y += 1;**\
&#x20; **blueGamePiece.x += 1;**\
&#x20; **blueGamePiece.y -= 1;**\
&#x20; redGamePiece.update();\
&#x20; yellowGamePiece.update();\
&#x20; blueGamePiece.update();\
}
