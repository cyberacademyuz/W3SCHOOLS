# Clock Strelkalar

### IV qism - Soat qo'llarini chizish

Soat qo'llar kerak. Soat qo'llarini chizish uchun JavaScript funksiyasini yarating:

#### JavaScript:

function drawClock() {\
&#x20; drawFace(ctx, radius);\
&#x20; drawNumbers(ctx, radius);\
&#x20; **drawTime(ctx, radius);**\
}\
\
function drawTime(ctx, radius){\
&#x20; var now = new Date();\
&#x20; var hour = now.getHours();\
&#x20; var minute = now.getMinutes();\
&#x20; var second = now.getSeconds();\
&#x20; //hour\
&#x20; hour = hour%12;\
&#x20; hour = (hour\*Math.PI/6)+(minute\*Math.PI/(6\*60))+(second\*Math.PI/(360\*60));\
&#x20; drawHand(ctx, hour, radius\*0.5, radius\*0.07);\
&#x20; //minute\
&#x20; minute = (minute\*Math.PI/30)+(second\*Math.PI/(30\*60));\
&#x20; drawHand(ctx, minute, radius\*0.8, radius\*0.07);\
&#x20; // second\
&#x20; second = (second\*Math.PI/30);\
&#x20; drawHand(ctx, second, radius\*0.9, radius\*0.02);\
}\
\
function drawHand(ctx, pos, length, width) {\
&#x20; ctx.beginPath();\
&#x20; ctx.lineWidth = width;\
&#x20; ctx.lineCap = "round";\
&#x20; ctx.moveTo(0,0);\
&#x20; ctx.rotate(pos);\
&#x20; ctx.lineTo(0, -length);\
&#x20; ctx.stroke();\
&#x20; ctx.rotate(-pos);\
}\


***

***

### Misol tushuntirildi

Soat, daqiqa, soniyani olish uchun sanadan foydalaning:

var now = new Date();\
var hour = now.getHours();\
var minute = now.getMinutes();\
var second = now.getSeconds();

Soat tilining burchagini hisoblang va uning uzunligini (radiusning 50%) va kengligini (radiusning 7%) chizing:

hour = hour%12;\
hour = (hour\*Math.PI/6)+(minute\*Math.PI/(6\*60))+(second\*Math.PI/(360\*60));\
drawHand(ctx, hour, radius\*0.5, radius\*0.07);

Xuddi shu texnikani daqiqalar va soniyalar uchun ishlating.

DrawHand() tartibi tushuntirishga muhtoj emas. U faqat berilgan uzunlik va kenglikdagi chiziqni tortadi.
