# Clock Raqamlar

### III qism - Soat raqamlarini chizish

Soat raqamlarga muhtoj. Soat raqamlarini chizish uchun JavaScript funksiyasini yarating:

#### JavaScript:

function drawClock() {\
&#x20; drawFace(ctx, radius);\
&#x20; **drawNumbers(ctx, radius);**\
}\
\
function drawNumbers(ctx, radius) {\
&#x20; var ang;\
&#x20; var num;\
&#x20; ctx.font = radius \* 0.15 + "px arial";\
&#x20; ctx.textBaseline = "middle";\
&#x20; ctx.textAlign = "center";\
&#x20; for(num = 1; num < 13; num++){\
&#x20;   ang = num \* Math.PI / 6;\
&#x20;   ctx.rotate(ang);\
&#x20;   ctx.translate(0, -radius \* 0.85);\
&#x20;   ctx.rotate(-ang);\
&#x20;   ctx.fillText(num.toString(), 0, 0);\
&#x20;   ctx.rotate(ang);\
&#x20;   ctx.translate(0, radius \* 0.85);\
&#x20;   ctx.rotate(-ang);\
&#x20; }\
}\


***

***

### Misol tushuntirildi

Shrift hajmini (chizilgan ob'ektning) radiusning 15% ga o'rnating:

ctx.font = radius \* 0.15 + "px arial";

Matnni tekislashni bosib chiqarish joyining o'rtasiga va markaziga o'rnating:

ctx.textBaseline = "middle";\
ctx.textAlign = "center";

Har bir raqam uchun aylantirilgan (PI/6) radiusning 85% gacha bosib chiqarish joyini (12 ta raqam uchun) hisoblang:

for(num = 1; num < 13; num++) {\
&#x20; ang = num \* Math.PI / 6;\
&#x20; ctx.rotate(ang);\
&#x20; ctx.translate(0, -radius \* 0.85);\
&#x20; ctx.rotate(-ang);\
&#x20; ctx.fillText(num.toString(), 0, 0);\
&#x20; ctx.rotate(ang);\
&#x20; ctx.translate(0, radius \* 0.85);\
&#x20; ctx.rotate(-ang);\
}
