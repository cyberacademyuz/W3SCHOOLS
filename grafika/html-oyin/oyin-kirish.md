# O'yin Kirish

HTML va JavaScript-dan boshqa hech narsa ishlatmasdan o'yinlar yaratishni o'rganing.

Qizil kvadratni siljitish uchun tugmalarni bosing:

\
\
\
\
\
\


***

### O'zingiz sinab ko'ring Misollar

Onlayn muharririmiz yordamida siz kodni tahrirlashingiz va natijani ko'rish uchun tugmani bosishingiz mumkin.

#### Misol

function startGame() {\
&#x20; myGamePiece = new component(30, 30, "red", 10, 120);\
&#x20; myGamePiece.gravity = 0.05;\
&#x20; myScore = new component("30px", "Consolas", "black", 280, 40, "text");\
&#x20; myGameArea.start();\
}\
\
var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   this.frameNo = 0;\
&#x20; },\
&#x20; clear : function() {\
&#x20;   this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);\
&#x20; }\
}
