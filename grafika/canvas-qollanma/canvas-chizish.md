# Canvas Chizish

### Tuvalga JavaScript yordamida rasm chizish

HTML tuvalidagi barcha chizmalar JavaScript bilan bajarilishi kerak:

#### Misol

\<script>\
var canvas = document.getElementById("myCanvas");\
var ctx = canvas.getContext("2d");\
ctx.fillStyle = "#FF0000";\
ctx.fillRect(0, 0, 150, 75);\
\</script>\


***

### 1-qadam: Tuval elementini toping

Avvalo, siz \<canvas> elementini topishingiz kerak.

Bu getElementById() HTML DOM usuli yordamida amalga oshiriladi:

var canvas = document.getElementById("myCanvas");

***

### 2-qadam: Chizish ob'ektini yarating

Ikkinchidan, tuval uchun chizilgan ob'ekt kerak.

getContext() o'rnatilgan HTML ob'ekti bo'lib, u xususiyatlari va chizish usullariga ega:

var ctx = canvas.getContext("2d");

***

### 3-qadam: Tuvalga rasm chizish

Nihoyat, siz tuvalga chizishingiz mumkin.

Chizilgan ob'ektni to'ldirish uslubini qizil rangga o'rnating:

ctx.fillStyle = "#FF0000";

FillStyle xususiyati CSS rangi, gradient yoki naqsh bo'lishi mumkin. Standart fillStyle qora rangda.

fillRect( _x,y,width,height_ ) usuli tuvalga to'ldirish uslubi bilan to'ldirilgan to'rtburchak chizadi:

ctx.fillRect(0, 0, 150, 75);
