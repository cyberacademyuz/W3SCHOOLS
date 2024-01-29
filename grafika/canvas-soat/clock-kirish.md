# Clock Kirish

Ushbu boblarda biz HTML kanvasidan foydalangan holda analog soat quramiz.

***

### I qism - Tuval yaratish

Soatga HTML konteyner kerak. HTML kanvasini yarating:

#### HTML kodi:

\<!DOCTYPE html>\
\<html>\
\<body>\
\
\<canvas id="canvas" width="400" height="400" style="background-color:#333">\</canvas>\
\
\<script>\
var canvas = document.getElementById("canvas");\
var ctx = canvas.getContext("2d");\
var radius = canvas.height / 2;\
ctx.translate(radius, radius);\
radius = radius \* 0.90\
drawClock();\
\
function drawClock() {\
&#x20; ctx.arc(0, 0, radius, 0 , 2 \* Math.PI);\
&#x20; ctx.fillStyle = "white";\
&#x20; ctx.fill();\
}\
\</script>\
\
\</body>\
\</html>\


***

***

### Kod tushuntirildi

Sahifangizga HTML \<canvas> elementini qo'shing:

\<canvas id="canvas" width="400" height="400" style="background-color:#333">\</canvas>\


HTML tuval elementidan kanvas ob'ektini (var canvas) yarating:

var canvas = document.getElementById("canvas");

Tuval obyekti uchun 2D chizma ob'ektini (var ctx) yarating:

var ctx = canvas.getContext("2d");

Tuval balandligidan foydalanib, soat radiusini hisoblang:

var radius = canvas.height / 2;

Soat radiusini hisoblash uchun tuval balandligidan foydalanib, soat barcha tuval o'lchamlari uchun ishlaydi.

(0,0) holatini (chizilgan ob'ektning) tuvalning o'rtasiga o'zgartiring:

ctx.translate(radius, radius);

Tuval ichida soatni yaxshi chizish uchun soat radiusini (90% gacha) kamaytiring:

radius = radius \* 0.90;

Soatni chizish funksiyasini yarating:

function drawClock() {\
&#x20; ctx.arc(0, 0, radius, 0 , 2 \* Math.PI);\
&#x20; ctx.fillStyle = "white";\
&#x20; ctx.fill();\
}
