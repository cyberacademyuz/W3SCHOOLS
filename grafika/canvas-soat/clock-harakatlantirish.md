# Clock Harakatlantirish

Ushbu boblarda biz HTML Canvas yordamida analog soat quramiz.

***

### V qism - Soatni ishga tushirish

Soatni boshlash uchun oraliqda drawClock funksiyasini chaqiring:

#### JavaScript:

var canvas = document.getElementById("canvas");\
var ctx = canvas.getContext("2d");\
var radius = canvas.height / 2;\
ctx.translate(radius, radius);\
radius = radius \* 0.90\
//drawClock();\
setInterval(drawClock, 1000);\


***

### Misol tushuntirildi

Siz qilishingiz kerak bo'lgan yagona narsa (soatni boshlash uchun) vaqt oralig'ida drawClock funksiyasini chaqirishdir.

O'rinbosar:

drawClock();\


Bilan:

setInterval(drawClock, 1000);

Interval millisekundlarda. DrawClock har 1000 millisekundda chaqiriladi.
