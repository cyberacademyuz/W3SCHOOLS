# Canvas Gradientlar

### Kanvas - Gradientlar

Gradientlar to'rtburchaklar, doiralar, chiziqlar, matn va hokazolarni to'ldirish uchun ishlatilishi mumkin. Tuvaldagi shakllar faqat bitta ranglar bilan chegaralanmaydi.

Ikki xil gradient turi mavjud:

* createLinearGradient( _x,y,x1,y1_ ) - chiziqli gradient yaratadi
* createRadialGradient( _x,y,r,x1,y1,r1_ ) - radial/dumaloq gradient yaratadi

Gradient ob'ektiga ega bo'lganimizdan so'ng, biz ikkita yoki undan ko'p rangli to'xtash joylarini qo'shishimiz kerak.

addColorStop() usuli rang to'xtash joylarini va uning gradient bo'ylab o'rnini belgilaydi. Gradient pozitsiyalari 0 dan 1 gacha bo'lishi mumkin.

Gradientdan foydalanish uchun fillStyle yoki strokeStyle xossasini gradientga o'rnating, so'ngra shaklni (to'rtburchak, matn yoki chiziq) chizing.

***

### createLinearGradient() dan foydalanish

#### Misol

Chiziqli gradient yarating. To'rtburchakni gradient bilan to'ldiring:

JavaScript:

var c = document.getElementById("myCanvas");\
var ctx = c.getContext("2d");\
\
// Create gradient\
var grd = ctx.createLinearGradient(0, 0, 200, 0);\
grd.addColorStop(0, "red");\
grd.addColorStop(1, "white");\
\
// Fill with gradient\
ctx.fillStyle = grd;\
ctx.fillRect(10, 10, 150, 80);

***

***

### createRadialGradient() dan foydalanish:

#### Misol

Radial/dumaloq gradient yarating. To'rtburchakni gradient bilan to'ldiring:

JavaScript:

var c = document.getElementById("myCanvas");\
var ctx = c.getContext("2d");\
\
// Create gradient\
var grd = ctx.createRadialGradient(75, 50, 5, 90, 60, 100);\
grd.addColorStop(0, "red");\
grd.addColorStop(1, "white");\
\
// Fill with gradient\
ctx.fillStyle = grd;\
ctx.fillRect(10, 10, 150, 80);
