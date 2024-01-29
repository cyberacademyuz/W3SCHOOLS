# Funksiya yaratish

Javascriptda funksiyalar `function` kalit so'i bilan yaratiladi.

Siz **function declaration** yoki **function expression**dan foydalanishingiz mumkin.

### Funtion declaration

Ushbu qo'llanmaning boshida funksiyalar quyidagi sintaksis bilan **e'lon qilinishini** bilib olgandingiz**:**

```
function functionName(parameters) {
  // code to be executed
}
```

E'lon qilingan funksiyalar darhol ishga tushmaydi. Ular "keyinroq foydalanish uchun saqlanadi" va ular chaqirilganda sihga tushadi.

```
function myFunction(a, b) {
  return a * b;
}
```

{% hint style="warning" %}
Nuqtali vergul ishga tushadigan steytmentlarni ajratish uchun ishlatiladi.\
Function declarationda ishga tushadigan steytment bo'lmagani uchun uni nuqtali vergul bilan tugatish ko'p uchramaydi.
{% endhint %}

### Function expression

Fuunktsiyani **expression** yordamida ham yaratish mumkin.

Function expressionni o'zgaruvchida saqlanish mumkin:

```
const x = function (a, b) {return a * b};
```

Function expression o'zgaruvchida saqlanganidan so'ng, o'zgaruvchidan funksiya sifatida foydalanish mumkin:

```
const x = function (a, b) {return a * b};
let z = x(4, 3);
```

Yuqoridagi funksiya aslida **anonim funksiya** (nomsiz funksiya).

O'zgaruvchilarda saqlangan funksiyalar funksiya nomiga muhtoj emas. Ularni har doim o'zgaruvchi nomidan foydalanib chaqiriladi (chaqiriladi).

{% hint style="warning" %}
Yuqoridagi funksiya nuqta-vergul bilan tugaydi, chunki u bajariladigan operatorning bir qismidir.
{% endhint %}

### Function() konstruktori

Oldingi misollarda ko'rganingizdek, JavaScript funksiyalari `function` kalit so'zi bilan yaratiladi.

Funktsiyalar built-in `Function()` nomli funksiya konstruktori bilan ham yaratilishi mumkin.

```
const myFunction = new Function("a", "b", "return a * b");

let x = myFunction(4, 3);
```

Aslida funksiya konstruktoridan foydalanishingiz shart emas. Yuqoridagi misol quyidagi bilan bir xil:

```
const myFunction = function (a, b) {return a * b};

let x = myFunction(4, 3);
```

{% hint style="warning" %}
Ko'pincha JavaScript-da `new` kalit so'zni ishlatishdan saqlanishingiz mumkin.
{% endhint %}

### Funktsiyada hoisting

Ushbu qo'llanmaning boshida "hoisting" ([JavaScript Hoisting](../js-qollanma/hoisting.md)) haqida bilib oldingiz.

**Hoisting -** bu deklaratsiyalarni joriy doiraning yuqori qismiga ko'chirishning standart xatti-harakati.

Hoisting o'zgaruvchi va funktsiya e'lon qilishlarda ishlaydi.

Shu sababdan ham, funktsiyalarni e'lon qilinishidan oldin chaqirish mumkin:

```
myFunction(5);

function myFunction(y) {
  return y * y;
}
```

Function expression yordamida yaratilgan funksiyalar hoisting bo'lmaydi.

### O'z-o'zini chaqiruvchi funktsiyalar

Function expressionlar "o'zini-o'zi chaqirishi" mumkin.

O'z-o'zini chaqiruvchi expression chaqirilmasdan avval avtomatik tarzda chaqiriladi.

Function expressionda, agar ifodadan keyin () bo'lsa, avtomatik tarzda bajariladi.

Function declarationni o'zingiz chaqira olmaysiz.

Bu function expression ekanligini bildirish uchun uning atrofiga qavslar qo'shishingiz kerak:

```
(function () {
  let x = "Hello!!";  // I will invoke myself
})();
```

Yuqoridagi funktsiya aslida **anonim** o'z-o'zini chaqiruvchi funktsiyadir.

### Funktsiyalardan qiymat sifatida foydalanish mumkin

JavaScript funksiyalaridan qiymat sifatida foydalanish mumkin:

```
function myFunction(a, b) {
  return a * b;
}

let x = myFunction(4, 3);
```

JavaScript funksiyalari quyidagi expressionlarda ishlatilishi mumkin:

```
function myFunction(a, b) {
  return a * b;
}

let x = myFunction(4, 3) * 2;
```

### Funksiyalar obkyetlardir

`typeof` operatori funksiyalar uchun "function" qaytaradi.

Biroq, funktsiyalarni eng yaxshi obyektlar sifatida tasvirlash mumkin.

JavaScript funktsiyalari, ham **xususiyatlarga**, ham **metodlarga** ega.

`arguments.length` xususiyati funksiya chaqirilganda olingan argumentlar sonini qaytaradi:

```
function myFunction(a, b) {
  return arguments.length;
}
```

`toString()` metodi funktsiyani string sifatida qaytaradi:

```
function myFunction(a, b) {
  return a * b;
}

let text = myFunction.toString();
```

{% hint style="warning" %}
Obyektning xossasi sifatida yaratilgan funktsiya obyekt uchun metodi deb chaqiriladi.\
Yangi obyektlarni yaratish uchun mo'ljallangan funksiya obyekt konstruktori deb ataladi.
{% endhint %}

### Arrow funksiyalar

Arrow funksiyalar function expressionni qisqa sintaksisda yozish imkonini beradi.

Sizga `function`, `return` kalit so'zlari va jingalak qavslar ham kerak emas.

```
// ES5
var x = function(x, y) {
  return x * y;
}

// ES6
const x = (x, y) => x * y;

```

Arrow funksiyalari o'zining `this-`iga ga emas. Ular obyekt metodlarini yaratish uchun mos kelmaydi.

Arrow funksiyalar hoisting bo'lmaydi. Ularni foydalanishdan avval e'lon qilish kerak.

`const` foydalanish `var`dan foydalanishdan ko'ra xavfsizroqdir, chunki function expression har doim konstanta qiymat hisoblanadi.

Agar funktsiyada bitta expression bo'lsa, `return` kalit so'zi va jingalak qavslardan foydalanmasligingiz mumkin. Shu sababli ham, ulardan doimo foydalanish yaxshi odat bo'lishi mumkin:

```
const x = (x, y) => { return x * y };
```

{% hint style="warning" %}
Arrow funksiyalari IE11 yoki undan oldingi versiyalarda qo‘llab-quvvatlanmaydi.
{% endhint %}
