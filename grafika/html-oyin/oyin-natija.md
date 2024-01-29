# O'yin Natija

Qizil kvadratni siljitish uchun tugmalarni bosing:

\
\
\
\
\
\


***

### Ballarni hisoblang

O'yinda hisobni saqlashning ko'plab usullari mavjud, biz sizga hisobni tuvalga qanday yozishni ko'rsatamiz.

Avval ball komponentini yarating:

#### Misol

var myGamePiece;\
var myObstacles = \[];\
**var myScore;**\
\
function startGame() {\
&#x20; myGamePiece = new component(30, 30, "red", 10, 160);\
&#x20; **myScore = new component("30px", "Consolas", "black", 280, 40, "text");**\
&#x20; myGameArea.start();\
}\
\


Tuval elementiga matn yozish sintaksisi to'rtburchak chizishdan farq qiladi. Shuning uchun biz qo'shimcha argument yordamida komponent konstruktoriga qo'ng'iroq qilishimiz kerak va konstruktorga ushbu komponent "matn" turida ekanligini aytishimiz kerak.

Komponent konstruktorida komponentning "matn" turida ekanligini tekshiramiz va usul `fillText`o'rniga usuldan foydalanamiz `fillRect`:

#### Misol

function component(width, height, color, x, y**, type**) {\
&#x20; **this.type = type;**\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.speedX = 0;\
&#x20; this.speedY = 0;\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   **if (this.type == "text") {**\
&#x20;     **ctx.font = this.width + " " + this.height;**\
&#x20;     **ctx.fillStyle = color;**\
&#x20;     **ctx.fillText(this.text, this.x, this.y);**\
&#x20;   **} else {**\
&#x20;     ctx.fillStyle = color;\
&#x20;     ctx.fillRect(this.x, this.y, this.width, this.height);\
&#x20;   **}**\
&#x20; }\
...\
}\
\


***

***

Nihoyat, biz ballni tuvalga yozadigan updateGameArea funksiyasiga ba'zi kodlarni qo'shamiz. `frameNo`Ballarni hisoblash uchun biz xususiyatdan foydalanamiz :

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
&#x20; **myGameArea.frameNo += 1;**\
&#x20; if (myGameArea.frameNo == 1 || everyinterval(150)) {\
&#x20;   x = myGameArea.canvas.width;\
&#x20;   minHeight = 20;\
&#x20;   maxHeight = 200;\
&#x20;   height = Math.floor(Math.random()\*(maxHeight-minHeight+1)+minHeight);\
&#x20;   minGap = 50;\
&#x20;   maxGap = 200;\
&#x20;   gap = Math.floor(Math.random()\*(maxGap-minGap+1)+minGap);\
&#x20;   myObstacles.push(new component(10, height, "green", x, 0));\
&#x20;   myObstacles.push(new component(10, x - height - gap, "green", x, height + gap));\
&#x20; }\
&#x20; for (i = 0; i < myObstacles.length; i += 1) {\
&#x20;   myObstacles\[i].speedX = -1;\
&#x20;   myObstacles\[i].newPos();\
&#x20;   myObstacles\[i].update();\
&#x20; }\
&#x20; **myScore.text = "SCORE: " + myGameArea.frameNo;**\
&#x20; **myScore.update();**\
&#x20; myGamePiece.newPos();\
&#x20; myGamePiece.update();\
}
