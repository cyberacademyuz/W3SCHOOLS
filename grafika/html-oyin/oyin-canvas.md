# O'yin Canvas

HTML `<canvas>`elementi veb-sahifada to'rtburchaklar ob'ekt sifatida ko'rsatiladi:

***

### HTML Canvas

Element `<canvas>`HTMLda o'yinlar yaratish uchun juda mos keladi.

Element `<canvas>`o'yinlar yaratish uchun zarur bo'lgan barcha funksiyalarni taqdim etadi.

.ga chizish, yozish, rasm qo'shish va boshqalar uchun JavaScript-dan foydalaning `<canvas>`.

***

### .getContext("2d")

Elementda ob'ekt deb ataladigan, chizish usullari va xususiyatlariga ega `<canvas>`o'rnatilgan ob'ekt mavjud .`getContext("2d")`

`<canvas>`Element va `getContext("2d")`ob'ekt haqida ko'proq ma'lumotni [Canvas qo'llanmamizdan](https://www-w3schools-com.translate.goog/graphics/canvas\_intro.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) olishingiz mumkin .

***

### Boshlash

O'yinni yaratish uchun o'yin maydonini yaratishdan boshlang va uni chizishga tayyorlang:

#### Misol

function startGame() {\
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
&#x20; }\
}\


`myGameArea`Ushbu qo'llanmada keyinroq ob'ekt ko'proq xususiyat va usullarga ega bo'ladi.

Funktsiya ob'ektning `startGame()`usulini chaqiradi . `start() myGameArea`

Usul element `start()`yaratadi `<canvas>`va uni elementning birinchi tuguni sifatida kiritadi `<body>`.
