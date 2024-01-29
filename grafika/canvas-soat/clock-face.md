# Clock Face

### II qism - Soat yuzini chizish

Soatga soat yuzi kerak. Soat yuzini chizish uchun JavaScript funksiyasini yarating:

#### JavaScript:

function drawClock() {\
&#x20; **drawFace(ctx, radius);**\
}\
\
function drawFace(ctx, radius) {\
&#x20; var grad;\
\
&#x20; ctx.beginPath();\
&#x20; ctx.arc(0, 0, radius, 0, 2 \* Math.PI);\
&#x20; ctx.fillStyle = 'white';\
&#x20; ctx.fill();\
\
&#x20; grad = ctx.createRadialGradient(0, 0 ,radius \* 0.95, 0, 0, radius \* 1.05);\
&#x20; grad.addColorStop(0, '#333');\
&#x20; grad.addColorStop(0.5, 'white');\
&#x20; grad.addColorStop(1, '#333');\
&#x20; ctx.strokeStyle = grad;\
&#x20; ctx.lineWidth = radius\*0.1;\
&#x20; ctx.stroke();\
\
&#x20; ctx.beginPath();\
&#x20; ctx.arc(0, 0, radius \* 0.1, 0, 2 \* Math.PI);\
&#x20; ctx.fillStyle = '#333';\
&#x20; ctx.fill();\
}\


***

***

### Kod tushuntirildi

Soat yuzini chizish uchun drawFace() funksiyasini yarating:

function drawClock() {\
&#x20; **drawFace(ctx, radius);**\
}\
\
function drawFace(ctx, radius) {\
}

Oq doira chizing:

ctx.beginPath();\
ctx.arc(0, 0, radius, 0, 2 \* Math.PI);\
ctx.fillStyle = 'white';\
ctx.fill();

Radial gradient yarating (asl soat radiusining 95% va 105%):

grad = ctx.createRadialGradient(0, 0, radius \* 0.95, 0, 0, radius \* 1.05);

Yoyning ichki, o'rta va tashqi chetiga mos keladigan 3 ta rangli to'xtash joyini yarating:

grad.addColorStop(0, '#333');\
grad.addColorStop(0.5, 'white');\
grad.addColorStop(1, '#333');

Rang to'xtashlari 3D effektini yaratadi.

Gradientni chizilgan ob'ektning chiziq uslubi sifatida belgilang:

ctx.strokeStyle = grad;

Chizilgan ob'ektning chiziq kengligini aniqlang (radiusning 10%):

ctx.lineWidth = radius \* 0.1;

Doira chizing:

ctx.stroke();

Soat markazini chizish:

ctx.beginPath();\
ctx.arc(0, 0, radius \* 0.1, 0, 2 \* Math.PI);\
ctx.fillStyle = '#333';\
ctx.fill();
