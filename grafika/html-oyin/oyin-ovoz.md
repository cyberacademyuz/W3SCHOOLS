# O'yin Ovoz

Ovoz balandligini oshiring. Qizil kvadrat to'siqqa tegsa, "dunk" eshitasizmi?

\
\
\
\
\
\


***

### Ovozlarni qanday qo'shish kerak?

O'yinlaringizga ovoz va musiqa qo'shish uchun HTML5 \<audio> elementidan foydalaning.

Bizning misollarimizda biz tovush ob'ektlarini boshqarish uchun yangi ob'ekt konstruktorini yaratamiz:

#### Misol

function sound(src) {\
&#x20; this.sound = document.createElement("audio");\
&#x20; this.sound.src = src;\
&#x20; this.sound.setAttribute("preload", "auto");\
&#x20; this.sound.setAttribute("controls", "none");\
&#x20; this.sound.style.display = "none";\
&#x20; document.body.appendChild(this.sound);\
&#x20; this.play = function(){\
&#x20;   this.sound.play();\
&#x20; }\
&#x20; this.stop = function(){\
&#x20;   this.sound.pause();\
&#x20; }\
}\


***

***

Yangi tovush ob'ektini yaratish uchun konstruktordan foydalaning `sound`va qizil kvadrat to'siqqa tegsa, ovozni ijro eting:

#### Misol

var myGamePiece;\
var myObstacles = \[];\
**var mySound;**\
\
function startGame() {\
&#x20; myGamePiece = new component(30, 30, "red", 10, 120);\
&#x20; **mySound = new sound("bounce.mp3");**\
&#x20; myGameArea.start();\
}\
\
function updateGameArea() {\
&#x20; var x, height, gap, minHeight, maxHeight, minGap, maxGap;\
&#x20; for (i = 0; i < myObstacles.length; i += 1) {\
&#x20;   if (myGamePiece.crashWith(myObstacles\[i])) {\
&#x20;     **mySound.play();**\
&#x20;     myGameArea.stop();\
&#x20;     return;\
&#x20;   }\
&#x20; }\
\
...\
\
}\


***

### Fon musiqa

O'yiningizga fon musiqasini qo'shish uchun yangi tovush ob'ektini qo'shing va o'yinni boshlaganingizda o'ynashni boshlang:

#### Misol

var myGamePiece;\
var myObstacles = \[];\
var mySound;\
**var myMusic;**\
\
function startGame() {\
&#x20; myGamePiece = new component(30, 30, "red", 10, 120);\
&#x20; mySound = new sound("bounce.mp3");\
&#x20; **myMusic = new sound("gametheme.mp3");**\
&#x20; **myMusic.play();**\
&#x20; myGameArea.start();\
}
