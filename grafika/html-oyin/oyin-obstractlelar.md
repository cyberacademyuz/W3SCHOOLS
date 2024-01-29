# O'yin Obstractlelar

Qizil kvadratni siljitish uchun tugmalarni bosing:

\
\
\
\
\


***

### Ba'zi to'siqlarni qo'shing

Endi biz o'yinimizga ba'zi to'siqlarni qo'shmoqchimiz.

O'yin maydoniga yangi komponent qo'shing. Uni yashil qilib, kengligi 10px, balandligi 200px va oʻngga 300px va pastga 120px joylashtiring.

Shuningdek, har bir ramkadagi to'siq komponentini yangilang:

#### Misol

var myGamePiece;\
**var myObstacle;**\
\
function startGame() {\
&#x20; myGamePiece = new component(30, 30, "red", 10, 120);\
&#x20; **myObstacle = new component(10, 200, "green", 300, 120);**\
&#x20; myGameArea.start();\
}\
\
function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **myObstacle.update();**\
&#x20; myGamePiece.newPos();\
&#x20; myGamePiece.update();\
}\


***

***

### To'siqni bosing = O'yin tugadi

Yuqoridagi misolda siz to'siqni urganingizda hech narsa sodir bo'lmaydi. O'yinda bu unchalik qoniqarli emas.

Qizil kvadratimiz to'siqqa tegib ketganini qanday bilamiz?

Komponent konstruktorida komponent boshqa komponent bilan ishlamay qolganligini tekshiradigan yangi usul yarating. Bu usul har sekundiga 50 marta kadrlar yangilanganda chaqirilishi kerak.

Shuningdek , `stop()`ob'ektga `myGameArea`20 millisekundlik intervalni tozalaydigan usul qo'shing.

#### Misol

var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   this.interval = setInterval(updateGameArea, 20);\
&#x20; },\
&#x20; clear : function() {\
&#x20;   this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);\
&#x20; }**,**\
&#x20; **stop : function() {**\
&#x20;   **clearInterval(this.interval);**\
&#x20; **}**\
}\
\
function component(width, height, color, x, y) {\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.speedX = 0;\
&#x20; this.speedY = 0;\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   ctx.fillStyle = color;\
&#x20;   ctx.fillRect(this.x, this.y, this.width, this.height);\
&#x20; }\
&#x20; this.newPos = function() {\
&#x20;   this.x += this.speedX;\
&#x20;   this.y += this.speedY;\
&#x20; }\
&#x20; **this.crashWith = function(otherobj) {**\
&#x20;   **var myleft = this.x;**\
&#x20;   **var myright = this.x + (this.width);**\
&#x20;   **var mytop = this.y;**\
&#x20;   **var mybottom = this.y + (this.height);**\
&#x20;   **var otherleft = otherobj.x;**\
&#x20;   **var otherright = otherobj.x + (otherobj.width);**\
&#x20;   **var othertop = otherobj.y;**\
&#x20;   **var otherbottom = otherobj.y + (otherobj.height);**\
&#x20;   **var crash = true;**\
&#x20;   **if ((mybottom < othertop) ||**\
&#x20;   **(mytop > otherbottom) ||**\
&#x20;   **(myright < otherleft) ||**\
&#x20;   **(myleft > otherright)) {**\
&#x20;     **crash = false;**\
&#x20;   **}**\
&#x20;   **return crash;**\
&#x20; **}**\
}\
\
function updateGameArea() {\
&#x20; **if (myGamePiece.crashWith(myObstacle)) {**\
&#x20;   **myGameArea.stop();**\
&#x20; **} else {**\
&#x20;   myGameArea.clear();\
&#x20;   myObstacle.update();\
&#x20;   myGamePiece.newPos();\
&#x20;   myGamePiece.update();\
&#x20; }\
}

***

### Harakatlanuvchi to'siq

To'siq statik bo'lsa, hech qanday xavf tug'dirmaydi, shuning uchun biz uning harakatlanishini xohlaymiz.

`myObstacle.x`Har bir yangilanishda mulk qiymatini o'zgartiring :

#### Misol

function updateGameArea() {\
&#x20; if (myGamePiece.crashWith(myObstacle)) {\
&#x20;   myGameArea.stop();\
&#x20; } else {\
&#x20;   myGameArea.clear();\
&#x20;   **myObstacle.x += -1;**\
&#x20;   myObstacle.update();\
&#x20;   myGamePiece.newPos();\
&#x20;   myGamePiece.update();\
&#x20; }\
}

***

### Bir nechta to'siqlar

Bir nechta to'siqlarni qo'shish haqida nima deyish mumkin?

Buning uchun bizga kadrlarni sanash xususiyati va ma'lum kvadrat tezligida biror narsani bajarish usuli kerak bo'ladi.

#### Misol

var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   **this.frameNo = 0;**       \
&#x20;   this.interval = setInterval(updateGameArea, 20);\
&#x20; },\
&#x20; clear : function() {\
&#x20;   this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);\
&#x20; },\
&#x20; stop : function() {\
&#x20;   clearInterval(this.interval);\
&#x20; }\
}\
\
**function everyinterval(n) {**\
&#x20; **if ((myGameArea.frameNo / n) % 1 == 0) {return true;}**\
&#x20; **return false;**\
**}**\


Agar joriy freym raqami berilgan intervalga to'g'ri kelsa, everyinterval funksiyasi true qiymatini qaytaradi.

Bir nechta to'siqlarni aniqlash uchun avval to'siq o'zgaruvchisini massiv sifatida e'lon qiling.

Ikkinchidan, updateGameArea funksiyasida ba'zi o'zgarishlar qilishimiz kerak.

#### Misol

var myGamePiece;\
**var myObstacles = \[];**\
\
**function updateGameArea() {**\
&#x20; **var x, y;**\
&#x20; **for (i = 0; i < myObstacles.length; i += 1) {**\
&#x20;   **if (myGamePiece.crashWith(myObstacles\[i])) {**\
&#x20;     **myGameArea.stop();**\
&#x20;     **return;**\
&#x20;   **}**\
&#x20; **}**\
&#x20; **myGameArea.clear();**\
&#x20; **myGameArea.frameNo += 1;**\
&#x20; **if (myGameArea.frameNo == 1 || everyinterval(150)) {**\
&#x20;   **x = myGameArea.canvas.width;**\
&#x20;   **y = myGameArea.canvas.height - 200**\
&#x20;   **myObstacles.push(new component(10, 200, "green", x, y));**\
&#x20; **}**\
&#x20; **for (i = 0; i < myObstacles.length; i += 1) {**\
&#x20;   **myObstacles\[i].x += -1;**\
&#x20;   **myObstacles\[i].update();**\
&#x20; **}**\
&#x20; myGamePiece.newPos();\
&#x20; myGamePiece.update();\
**}**

Funktsiyada `updateGameArea`biz har qanday to'siqni bosib o'tishimiz kerak, bunda nosozlik bor yoki yo'qligini ko'rishimiz kerak. Agar nosozlik bo'lsa, `updateGameArea`funktsiya to'xtaydi va boshqa chizma bajarilmaydi.

Funktsiya `updateGameArea`freymlarni hisoblaydi va har 150-kadr uchun to'siq qo'shadi.

***

### Tasodifiy o'lchamdagi to'siqlar

O'yinni biroz qiyinroq va qiziqarli qilish uchun biz tasodifiy o'lchamdagi to'siqlarni yuboramiz, shunda qizil kvadrat qulab tushmasligi uchun yuqoriga va pastga harakatlanishi kerak.

#### Misol

function updateGameArea() {\
&#x20; var x, height, gap, minHeight, maxHeight, minGap, maxGap;\
&#x20; for (i = 0; i < myObstacles.length; i += 1) {\
&#x20;   if (myGamePiece.crashWith(myObstacles\[i])) {\
&#x20;     myGameArea.stop();\
&#x20;     return;\
&#x20;   }\
&#x20; }\
&#x20; myGameArea.clear();\
&#x20; myGameArea.frameNo += 1;\
&#x20; **if (myGameArea.frameNo == 1 || everyinterval(150)) {**\
&#x20;   **x = myGameArea.canvas.width;**\
&#x20;   **minHeight = 20;**\
&#x20;   **maxHeight = 200;**\
&#x20;   **height = Math.floor(Math.random()\*(maxHeight-minHeight+1)+minHeight);**\
&#x20;   **minGap = 50;**\
&#x20;   **maxGap = 200;**\
&#x20;   **gap = Math.floor(Math.random()\*(maxGap-minGap+1)+minGap);**\
&#x20;   **myObstacles.push(new component(10, height, "green", x, 0));**\
&#x20;   **myObstacles.push(new component(10, x - height - gap, "green", x, height + gap));**\
&#x20; **}**\
&#x20; for (i = 0; i < myObstacles.length; i += 1) {\
&#x20;   myObstacles\[i].x += -1;\
&#x20;   myObstacles\[i].update();\
&#x20; }\
&#x20; myGamePiece.newPos();\
&#x20; myGamePiece.update();\
}
