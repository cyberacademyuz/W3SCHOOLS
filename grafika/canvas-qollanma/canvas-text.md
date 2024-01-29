# Canvas Text

### Tuvalga matn chizish

Tuvalga matn chizish uchun eng muhim xususiyat va usullar quyidagilardir:

* shrift - matn uchun shrift xususiyatlarini belgilaydi
* fillText( _text,x,y_ ) - tuvalga "to'ldirilgan" matnni chizadi
* strokeText ( _matn, x, y_ ) - tuvalga matn chizadi (to'ldirishsiz)

***

### fillText() dan foydalanish

#### Misol

Shriftni 30px "Arial" ga o'rnating va tuvalga to'ldirilgan matnni yozing:

JavaScript:

var canvas = document.getElementById("myCanvas");\
var ctx = canvas.getContext("2d");\
ctx.font = "30px Arial";\
ctx.fillText("Hello World", 10, 50);

***

### strokeText() dan foydalanish

#### Misol

Shriftni 30px "Arial" ga o'rnating va tuvalga to'ldirmasdan matn yozing:

JavaScript:

var canvas = document.getElementById("myCanvas");\
var ctx = canvas.getContext("2d");\
ctx.font = "30px Arial";\
ctx.strokeText("Hello World", 10, 50);

***

***

### Rang va markaziy matnni qo'shing

#### Misol

Shriftni 30px "Comic Sans MS" ga o'rnating va tuvalning o'rtasiga to'ldirilgan qizil matnni yozing:

JavaScript:

var canvas = document.getElementById("myCanvas");\
var ctx = canvas.getContext("2d");\
ctx.font = "30px Comic Sans MS";\
ctx.fillStyle = "red";\
ctx.textAlign = "center";\
ctx.fillText("Hello World", canvas.width/2, canvas.height/2);
