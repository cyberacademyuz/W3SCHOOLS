# Canvas Kordinatalar

### Kanvas koordinatalari

HTML kanvasi ikki o'lchovli panjaradir.

Tuvalning yuqori chap burchagida koordinatalar mavjud (0,0)

Oldingi bobda siz ushbu usul ishlatilganligini ko'rdingiz: fillRect (0,0,150,75).

Buning ma'nosi: Yuqori chap burchakdan (0,0) boshlang va 150x75 pikselli to'rtburchak chizing.

***

### Koordinatalar misoli

X va y koordinatalarini ko‘rish uchun quyidagi to‘rtburchak ustiga sichqonchani bosing:

XY

***

### Chiziq chizish

Tuvalga to'g'ri chiziq chizish uchun quyidagi usullardan foydalaning:

* moveTo( _x,y_ ) - chiziqning boshlanish nuqtasini belgilaydi
* lineTo( _x,y_ ) - chiziqning tugash nuqtasini belgilaydi

Chiziqni chizish uchun siz stroke() kabi "siyoh" usullaridan birini qo'llashingiz kerak.

#### Misol

Boshlanish nuqtasini (0,0) va yakuniy nuqtani (200,100) holatida aniqlang. Keyin chiziqni chizish uchun stroke() usulidan foydalaning:

var canvas = document.getElementById("myCanvas");\
var ctx = canvas.getContext("2d");\
ctx.moveTo(0, 0);\
ctx.lineTo(200, 100);\
ctx.stroke();

***

***

### Doira chizish

Tuvalga doira chizish uchun quyidagi usullardan foydalaning:

* beginPath() - yo'lni boshlaydi
* arc(x,y,r,startangle,endangle) - yoy/egri chiziq hosil qiladi. arc() yordamida aylana yaratish uchun: Boshlanish burchagini 0 ga va tugash burchagini 2\*Math.PI ga o'rnating. X va y parametrlari aylana markazining x va y koordinatalarini aniqlaydi. r parametri aylana radiusini belgilaydi.

#### Misol

arc() usuli bilan aylana belgilang. Keyin doirani chizish uchun stroke() usulidan foydalaning:

var canvas = document.getElementById("myCanvas");\
var ctx = canvas.getContext("2d");\
ctx.beginPath();\
ctx.arc(95, 50, 40, 0, 2 \* Math.PI);\
ctx.stroke();
