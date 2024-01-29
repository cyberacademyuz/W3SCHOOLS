# O'yin Kontrollerlar

Qizil kvadratni siljitish uchun tugmalarni bosing:

\
\
\
\
\
\


***

### Nazoratga o'ting

Endi biz qizil maydonni nazorat qilmoqchimiz.

Yuqoriga, pastga, chapga va o'ngga to'rtta tugma qo'shing.

Komponentni tanlangan yo'nalishda siljitish uchun har bir tugma uchun funktsiyani yozing.

Konstruktorda ikkita yangi xususiyat yarating `component`va ularni `speedX`va deb chaqiring `speedY`. Ushbu xususiyatlar tezlik ko'rsatkichlari sifatida ishlatiladi.

`component`Konstruktorga komponent oʻrnini oʻzgartirish uchun va xususiyatlaridan `newPos()`foydalanadigan funksiya qoʻshing .`speedXspeedY`

Newpos funktsiyasi komponentni chizishdan oldin updateGameArea funksiyasidan chaqiriladi:

#### Misol

\<script>function component(width, height, color, x, y) {\
&#x20; this.width = width;\
&#x20; this.height = height;\
&#x20; **this.speedX = 0;**\
&#x20; **this.speedY = 0;**\
&#x20; this.x = x;\
&#x20; this.y = y;\
&#x20; this.update = function() {\
&#x20;   ctx = myGameArea.context;\
&#x20;   ctx.fillStyle = color;\
&#x20;   ctx.fillRect(this.x, this.y, this.width, this.height);\
&#x20; }\
&#x20; **this.newPos = function() {**\
&#x20;   **this.x += this.speedX;**\
&#x20;   **this.y += this.speedY;**\
&#x20; **}**\
}\
\
function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **myGamePiece.newPos();**\
&#x20; myGamePiece.update();\
}\
\
function moveup() {\
&#x20; **myGamePiece.speedY -= 1;**\
}\
\
function movedown() {\
&#x20; **myGamePiece.speedY += 1;**\
}\
\
function moveleft() {\
&#x20; **myGamePiece.speedX -= 1;**\
}\
\
function moveright() {\
&#x20; **myGamePiece.speedX += 1;**\
}\
\</script>\
\
\<button onclick="moveup()">UP\</button>\
\<button onclick="movedown()">DOWN\</button>\
\<button onclick="moveleft()">LEFT\</button>\
\<button onclick="moveright()">RIGHT\</button>

***

***

### Harakat qilishni to'xtating

Agar xohlasangiz, tugmani bo'shatganingizda qizil kvadratni to'xtatishingiz mumkin.

Tezlik ko'rsatkichlarini 0 ga o'rnatadigan funksiya qo'shing.

Oddiy ekranlar va sensorli ekranlar bilan ishlash uchun ikkala qurilma uchun kod qo'shamiz:

#### Misol

**function stopMove() {**\
&#x20; **myGamePiece.speedX = 0;**\
&#x20; **myGamePiece.speedY = 0;**\
}\
\</script>\
\
\<button onmousedown="moveup()" **onmouseup="stopMove()" ontouchstart="moveup()**">UP\</button>\
\<button onmousedown="movedown()" **onmouseup="stopMove()" ontouchstart="movedown()"**>DOWN\</button>\
\<button onmousedown="moveleft()" **onmouseup="stopMove()" ontouchstart="moveleft()"**>LEFT\</button>\
\<button onmousedown="moveright()" **onmouseup="stopMove()" ontouchstart="moveright()"**>RIGHT\</button>

***

### Klaviatura boshqaruvchi sifatida

Shuningdek, biz qizil kvadratni klaviaturadagi o'q tugmalari yordamida boshqarishimiz mumkin.

Klaviatura bosilishini tekshiradigan usul yarating va `key`ob'ekt xususiyatini `myGameArea`kalit kodiga o'rnating. Kalit bo'shatilganda, `key`xususiyatni quyidagicha o'rnating `false`:

#### Misol

var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   this.interval = setInterval(updateGameArea, 20);\
&#x20;   **window.addEventListener('keydown', function (e) {**\
&#x20;     **myGameArea.key = e.keyCode;**\
&#x20;   **})**\
&#x20;   **window.addEventListener('keyup', function (e) {**\
&#x20;     **myGameArea.key = false;**\
&#x20;   **})**\
&#x20; },\
&#x20; clear : function(){\
&#x20;   this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);\
&#x20; }\
}\


Keyin o'q tugmalaridan biri bosilsa, qizil kvadratni siljitishimiz mumkin:

#### Misol

function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **myGamePiece.speedX = 0;**\
&#x20; **myGamePiece.speedY = 0;**\
&#x20; **if (myGameArea.key && myGameArea.key == 37) {myGamePiece.speedX = -1; }**\
&#x20; **if (myGameArea.key && myGameArea.key == 39) {myGamePiece.speedX = 1; }**\
&#x20; **if (myGameArea.key && myGameArea.key == 38) {myGamePiece.speedY = -1; }**\
&#x20; **if (myGameArea.key && myGameArea.key == 40) {myGamePiece.speedY = 1; }**\
&#x20; myGamePiece.newPos();\
&#x20; myGamePiece.update();\
}

***

### Bir nechta tugmalar bosildi

Agar bir vaqtning o'zida bir nechta tugmachalar bosilsa-chi?

Yuqoridagi misolda komponent faqat gorizontal yoki vertikal ravishda harakatlanishi mumkin. Endi biz komponentning diagonal bo'ylab harakatlanishini xohlaymiz.

Ob'ekt uchun `keys` _massiv_ yarating `myGameArea`va har bir bosilgan tugma uchun bitta elementni kiriting va unga qiymat bering `true`, qiymat tugma bosilmaguncha to'g'ri bo'lib qoladi va qiymat _keyup_ hodisasi tinglovchisi funksiyasiga `false`aylanadi :

#### Misol

var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   this.interval = setInterval(updateGameArea, 20);\
&#x20;   **window.addEventListener('keydown', function (e) {**\
&#x20;     **myGameArea.keys = (myGameArea.keys || \[]);**\
&#x20;     **myGameArea.keys\[e.keyCode] = true;**\
&#x20;   **})**\
&#x20;   **window.addEventListener('keyup', function (e) {**\
&#x20;     **myGameArea.keys\[e.keyCode] = false;**\
&#x20;   **})**\
&#x20; },\
&#x20; clear : function(){\
&#x20;   this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);\
&#x20; }\
}\
\
&#x20;function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; myGamePiece.speedX = 0;\
&#x20; myGamePiece.speedY = 0;\
&#x20; if (**myGameArea.keys && myGameArea.keys\[37]**) {myGamePiece.speedX = -1; }\
&#x20; if (**myGameArea.keys && myGameArea.keys\[39]**) {myGamePiece.speedX = 1; }\
&#x20; if (**myGameArea.keys && myGameArea.keys\[38]**) {myGamePiece.speedY = -1; }\
&#x20; if (**myGameArea.keys && myGameArea.keys\[40]**) {myGamePiece.speedY = 1; }\
&#x20; myGamePiece.newPos();\
&#x20; myGamePiece.update();\
}

***

### Sichqoncha kursorini boshqaruvchi sifatida ishlatish

Agar siz sichqoncha kursori yordamida qizil kvadratni boshqarmoqchi bo'lsangiz, ob'ektga `myGameArea`sichqoncha kursorining x va y koordinatalarini yangilaydigan usulni qo'shing:.

#### Misol

var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   **this.canvas.style.cursor = "none"; //hide the original cursor**\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   this.interval = setInterval(updateGameArea, 20);\
&#x20;   **window.addEventListener('mousemove', function (e) {**\
&#x20;     **myGameArea.x = e.pageX;**\
&#x20;     **myGameArea.y = e.pageY;**\
&#x20;   **})**\
&#x20; },\
&#x20; clear : function(){\
&#x20;   this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);\
&#x20; }\
}\


Keyin sichqoncha kursori yordamida qizil kvadratni siljitishimiz mumkin:

#### Misol

function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **if (myGameArea.x && myGameArea.y) {**\
&#x20;   **myGamePiece.x = myGameArea.x;**\
&#x20;   **myGamePiece.y = myGameArea.y;**\
&#x20; **}**\
&#x20; myGamePiece.update();\
}

***

### O'yinni boshqarish uchun ekranni bosing

Sensorli ekranda qizil kvadratni ham boshqarishimiz mumkin.

`myGameArea`Ob'ektga ekran tegilgan joyning x va y koordinatalaridan foydalanadigan usulni qo'shing :

#### Misol

var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   this.interval = setInterval(updateGameArea, 20);\
&#x20;   **window.addEventListener('touchmove', function (e) {**\
&#x20;     **myGameArea.x = e.touches\[0].screenX;**\
&#x20;     **myGameArea.y = e.touches\[0].screenY;**\
&#x20;   **})**\
&#x20; },\
&#x20; clear : function(){\
&#x20;   this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);\
&#x20; }\
}\


Keyin, agar foydalanuvchi ekranga tegsa, sichqoncha kursori bilan bir xil koddan foydalanib, qizil kvadratni siljitishimiz mumkin:

#### Misol

function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **if (myGameArea.x && myGameArea.y) {**\
&#x20;   **myGamePiece.x = myGameArea.x;**\
&#x20;   **myGamePiece.y = myGameArea.y;**\
&#x20; **}**\
&#x20; myGamePiece.update();\
}\


***

### Tuvaldagi kontrollerlar

Shuningdek, biz tuvalga o'z tugmalarimizni chizishimiz va ularni boshqaruvchi sifatida ishlatishimiz mumkin:

#### Misol

function startGame() {\
&#x20; myGamePiece = new component(30, 30, "red", 10, 120);\
&#x20; **myUpBtn = new component(30, 30, "blue", 50, 10);**\
&#x20; **myDownBtn = new component(30, 30, "blue", 50, 70);**\
&#x20; **myLeftBtn = new component(30, 30, "blue", 20, 40);**\
&#x20; **myRightBtn = new component(30, 30, "blue", 80, 40);**\
&#x20; myGameArea.start();\
}\


Komponent, bu holda tugma bosilganligini aniqlaydigan yangi funksiya qo'shing.

`mousedown`Sichqoncha tugmasi ( va ) bosilganligini tekshirish uchun voqea tinglovchilarini qo'shishdan boshlang `mouseup`. `touchstart`Sensorli ekranlar bilan ishlash uchun, shuningdek, ekranga ( va ) bosilganligini tekshirish uchun voqea tinglovchilarini qo'shing `touchend`:

#### Misol

var myGameArea = {\
&#x20; canvas : document.createElement("canvas"),\
&#x20; start : function() {\
&#x20;   this.canvas.width = 480;\
&#x20;   this.canvas.height = 270;\
&#x20;   this.context = this.canvas.getContext("2d");\
&#x20;   document.body.insertBefore(this.canvas, document.body.childNodes\[0]);\
&#x20;   this.interval = setInterval(updateGameArea, 20);\
&#x20;   **window.addEventListener('mousedown', function (e) {**\
&#x20;     **myGameArea.x = e.pageX;**\
&#x20;     **myGameArea.y = e.pageY;**\
&#x20;   **})**\
&#x20;   **window.addEventListener('mouseup', function (e) {**\
&#x20;     **myGameArea.x = false;**\
&#x20;     **myGameArea.y = false;**\
&#x20;   **})**\
&#x20;   **window.addEventListener('touchstart', function (e) {**\
&#x20;     **myGameArea.x = e.pageX;**\
&#x20;     **myGameArea.y = e.pageY;**\
&#x20;   **})**\
&#x20;   **window.addEventListener('touchend', function (e) {**\
&#x20;     **myGameArea.x = false;**\
&#x20;     **myGameArea.y = false;**\
&#x20;   **})**\
&#x20; },\
&#x20; clear : function(){\
&#x20;   this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);\
&#x20; }\
}\


Endi `myGameArea`ob'ekt bosishning x va y koordinatalarini bildiruvchi xususiyatlarga ega. Biz ushbu xususiyatlarni bosish ko'k tugmalarimizdan birida bajarilganligini tekshirish uchun foydalanamiz.

Yangi usul , deb ataladi `clicked`, u konstruktorning usuli bo'lib `component`, komponentning bosilishini tekshiradi.

&#x20;Funktsiyada `updateGameArea`, agar ko'k tugmalardan biri bosilsa, biz kerakli amallarni bajaramiz:

#### Misol

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
&#x20; **this.clicked = function() {**\
&#x20;   **var myleft = this.x;**\
&#x20;   **var myright = this.x + (this.width);**\
&#x20;   **var mytop = this.y;**\
&#x20;   **var mybottom = this.y + (this.height);**\
&#x20;   **var clicked = true;**\
&#x20;   **if ((mybottom < myGameArea.y) || (mytop > myGameArea.y) || (myright < myGameArea.x) || (myleft > myGameArea.x)) {**\
&#x20;     **clicked = false;**\
&#x20;   **}**\
&#x20;   **return clicked;**\
&#x20; **}**\
}\
\
function updateGameArea() {\
&#x20; myGameArea.clear();\
&#x20; **if (myGameArea.x && myGameArea.y) {**\
&#x20;   **if (myUpBtn.clicked()) {**\
&#x20;     **myGamePiece.y -= 1;**\
&#x20;   **}**\
&#x20;   **if (myDownBtn.clicked()) {**\
&#x20;     **myGamePiece.y += 1;**\
&#x20;   **}**\
&#x20;   **if (myLeftBtn.clicked()) {**\
&#x20;     **myGamePiece.x += -1;**\
&#x20;   **}**\
&#x20;   **if (myRightBtn.clicked()) {**\
&#x20;     **myGamePiece.x += 1;**\
&#x20;   **}**\
&#x20; **}**\
&#x20; **myUpBtn.update();**\
&#x20; **myDownBtn.update();**\
&#x20; **myLeftBtn.update();**\
&#x20; **myRightBtn.update();**\
&#x20; myGamePiece.update();\
}
