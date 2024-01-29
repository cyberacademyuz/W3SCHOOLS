# O'yin Rasmlar

Smaylni siljitish uchun tugmalarni bosing:

\
\
\
\
\
\


***

### Rasmlardan qanday foydalanish kerak?

Tuvalga rasmlar qo'shish uchun getContext("2d") ob'ekti o'rnatilgan tasvir xususiyatlari va usullariga ega.

Bizning o'yinimizda o'yinni tasvir sifatida yaratish uchun komponent konstruktoridan foydalaning, lekin rangga murojaat qilish o'rniga tasvirning url-ga murojaat qilishingiz kerak. Va siz konstruktorga ushbu komponent "image" turiga ega ekanligini aytishingiz kerak:

#### Misol

function startGame() {\
&#x20; myGamePiece = new component(30, 30, **"smiley.gif"**, 10, 120, **"image"**);\
&#x20; myGameArea.start();\
}\


Komponent konstruktorida biz komponentning "image" turida ekanligini tekshiramiz va o'rnatilgan "new Image()" ob'ekt konstruktoridan foydalanib tasvir ob'ektini yaratamiz. Tasvirni chizishga tayyor bo'lgach, fillRect usuli o'rniga drawImage usulidan foydalanamiz:

#### Misol

function component(width, height, color, x, y, type) {\
&#x20; this.type = type;\
&#x20; **if (type == "image") {**\
&#x20;   **this.image = new Image();**\
&#x20;   **this.image.src = color;**\
&#x20; **}**\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.speedX = 0;\
&#x20; this.speedY = 0;\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   **if (type == "image") {**\
&#x20;     **ctx.drawImage(this.image,**\
&#x20;       **this.x,**\
&#x20;       **this.y,**\
&#x20;       **this.width, this.height);**\
&#x20;   **} else {**\
&#x20;     ctx.fillStyle = color;\
&#x20;     ctx.fillRect(this.x, this.y, this.width, this.height);\
&#x20;   }\
&#x20; }\
}\


***

***

### Tasvirlarni o'zgartirish

Komponentingiz ob'ektining `src`xususiyatini o'zgartirish orqali tasvirni xohlagan vaqtda o'zgartirishingiz mumkin .`image`

![](https://www.w3schools.com/graphics/smiley.gif) ![](https://www.w3schools.com/graphics/angry.gif)

Agar tabassumni har safar harakatlanayotganda o‘zgartirmoqchi bo‘lsangiz, foydalanuvchi tugmani bosganida tasvir manbasini o‘zgartiring va tugma bosilmaganda esa normal holatga qayting:

#### Misol

function move(dir) {\
&#x20; **myGamePiece.image.src = "angry.gif";**\
&#x20; if (dir == "up") {myGamePiece.speedY = -1; }\
&#x20; if (dir == "down") {myGamePiece.speedY = 1; }\
&#x20; if (dir == "left") {myGamePiece.speedX = -1; }\
&#x20; if (dir == "right") {myGamePiece.speedX = 1; }\
}\
\
function clearmove() {\
&#x20; **myGamePiece.image.src = "smiley.gif";**\
&#x20; myGamePiece.speedX = 0;\
&#x20; myGamePiece.speedY = 0;\
}\


***

### Fon rasmlari

Komponent sifatida qo'shish orqali o'yin maydoniga fon tasvirini qo'shing, shuningdek, har bir kadrda fonni yangilang:

#### Misol

var myGamePiece;\
**var myBackground;**\
\
function startGame() {\
&#x20; myGamePiece = new component(30, 30, "smiley.gif", 10, 120, "image");\
&#x20; **myBackground = new component(656, 270, "citymarket.jpg", 0, 0, "image");**\
&#x20; myGameArea.start();\
}\
\
function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **myBackground.newPos();**\
&#x20; **myBackground.update();**\
&#x20; myGamePiece.newPos();\
&#x20; myGamePiece.update();\
}\


***

### Harakatlanuvchi fon

`speedX`Fonni siljitish uchun fon komponentining xususiyatini o'zgartiring :

#### Misol

function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **myBackground.speedX = -1;**\
&#x20; myBackground.newPos();\
&#x20; myBackground.update();\
&#x20; myGamePiece.newPos();\
&#x20; myGamePiece.update();\
}\


***

### Fon tsikli

Bir xil fon tsiklini abadiy qilish uchun biz ma'lum bir texnikadan foydalanishimiz kerak.

_Komponent konstruktoriga bu fon_ ekanligini aytib boshlang . Keyin komponent konstruktori rasmni ikki marta qo'shib, ikkinchi rasmni birinchi rasmdan keyin darhol joylashtiradi.

Usulda komponentning o'rni tasvirning oxirigacha yetib kelganligini `newPos()`tekshiring , agar u bo'lsa, komponent o'rnini 0 ga o'rnating:`xx`

#### Misol

function component(width, height, color, x, y, type) {\
&#x20; this.type = type;\
&#x20; if (type == "image" **|| type == "background"**) {\
&#x20;   this.image = new Image();\
&#x20;   this.image.src = color;\
&#x20; }\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.speedX = 0;\
&#x20; this.speedY = 0;\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   if (type == "image" || type == "background") {\
&#x20;     ctx.drawImage(this.image, this.x, this.y, this.width, this.height);\
&#x20;     **if (type == "background") {**\
&#x20;       **ctx.drawImage(this.image, this.x + this.width, this.y, this.width, this.height);**\
&#x20;     **}**\
&#x20;   } else {\
&#x20;     ctx.fillStyle = color;\
&#x20;     ctx.fillRect(this.x, this.y, this.width, this.height);\
&#x20;   }\
&#x20; }\
&#x20; this.newPos = function() {\
&#x20;   this.x += this.speedX;\
&#x20;   this.y += this.speedY;\
&#x20;   **if (this.type == "background") {**\
&#x20;     **if (this.x == -(this.width)) {**\
&#x20;       **this.x = 0;**\
&#x20;     **}**\
&#x20;   **}**\
&#x20; }\
}
