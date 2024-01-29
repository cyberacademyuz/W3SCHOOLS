# O'yin Sakrash

Bu qizil kvadrat polga tushganda sakraydi:

\
\


***

### Sakrash

Biz qo'shmoqchi bo'lgan yana bir funksiya - bu `bounce`xususiyat.

Bu `bounce`xususiyat komponentning tortishish kuchi erga tushishiga olib kelganda orqaga qaytishini ko'rsatadi.

Qaytish xususiyati qiymati raqam bo'lishi kerak. 0 hech qanday sakrash emas va 1 komponentni yiqila boshlagan joyga to'liq sakrashga majbur qiladi.

#### Misol

function component(width, height, color, x, y, type) {\
&#x20; this.type = type;\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.speedX = 0;\
&#x20; this.speedY = 0;\
&#x20; this.gravity = 0.1;\
&#x20; this.gravitySpeed = 0;\
&#x20; **this.bounce = 0.6;**\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   ctx.fillStyle = color;\
&#x20;   ctx.fillRect(this.x, this.y, this.width, this.height);\
&#x20; }\
&#x20; this.newPos = function() {\
&#x20;   this.gravitySpeed += this.gravity;\
&#x20;   this.x += this.speedX;\
&#x20;   this.y += this.speedY + this.gravitySpeed;\
&#x20;   this.hitBottom();\
&#x20; }\
&#x20; this.hitBottom = function() {\
&#x20;   var rockbottom = this.gamearea.canvas.height - this.height;\
&#x20;   if (this.y > rockbottom) {\
&#x20;     this.y = rockbottom;\
&#x20;     **this.gravitySpeed = -(this.gravitySpeed \* this.bounce);**\
&#x20;   }\
&#x20; }\
}
