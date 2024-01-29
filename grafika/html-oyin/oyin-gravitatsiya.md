# O'yin Gravitatsiya

Ba'zi o'yinlarda o'yin komponentini bir yo'nalishda tortadigan kuchlar mavjud, masalan, tortishish kuchi ob'ektlarni erga tortadi.

\
\


***

### Gravitatsiya

Ushbu funktsiyani komponent konstruktorimizga qo'shish uchun avval `gravity`joriy tortishish kuchini o'rnatadigan xususiyatni qo'shing. `gravitySpeed`Keyin har freymni yangilaganimizda ortib boruvchi xususiyatni qo'shing :

#### Misol

function component(width, height, color, x, y, type) {\
&#x20; this.type = type;\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.speedX = 0;\
&#x20; this.speedY = 0;\
&#x20; **this.gravity = 0.05;**\
&#x20; **this.gravitySpeed = 0;**\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   ctx.fillStyle = color;\
&#x20;   ctx.fillRect(this.x, this.y, this.width, this.height);\
&#x20; }\
&#x20; this.newPos = function() {\
&#x20;   **this.gravitySpeed += this.gravity;**\
&#x20;   this.x += this.speedX;\
&#x20;   this.y += this.speedY **+ this.gravitySpeed**;\
&#x20; }\
}\


***

***

### Pastki qismini bosing

Qizil kvadrat abadiy yiqilishiga yo'l qo'ymaslik uchun o'yin maydonining pastki qismiga tushganda tushishni to'xtating:

#### Misol

&#x20; this.newPos = function() {\
&#x20;   this.gravitySpeed += this.gravity;\
&#x20;   this.x += this.speedX;\
&#x20;   this.y += this.speedY + this.gravitySpeed;\
&#x20;   **this.hitBottom();**\
&#x20; }\
&#x20; **this.hitBottom = function() {**\
&#x20;   **var rockbottom = myGameArea.canvas.height - this.height;**\
&#x20;   **if (this.y > rockbottom) {**\
&#x20;     **this.y = rockbottom;**\
&#x20;   **}**\
&#x20; **}**\


***

### Yuqoriga tezlash

O'yinda sizni pastga tushiradigan kuchingiz bo'lsa, komponentni yuqoriga tezlashtirishga majburlash usuli bo'lishi kerak.

Kimdir tugmani bosganida funktsiyani ishga tushiring va qizil kvadratni havoda ko'taring:

#### Misol

\<script>function accelerate(n) {\
&#x20; myGamePiece.gravity = n;\
}\</script>\
\
\<button onmousedown="accelerate(-0.2)" onmouseup="accelerate(0.1)">ACCELERATE\</button>

***

### O'yin

Hozirgacha o'rgangan narsalarimiz asosida o'yin yarating:
