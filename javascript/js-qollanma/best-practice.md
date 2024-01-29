# Best practice

Global oʻzgaruvchilar, `new`, `==` va `eval()` dan foydalanishdan saqlaning.

### Global o'zgaruvchilardan saqlaning

Global oʻzgaruvchilardan foydalanishni kamaytiring.

Bu barcha ma'lumotlar turlari, obyektlar va funksiyalarni o'z ichiga oladi.

Global oʻzgaruvchilar va funksiyalar boshqa scriptlar tomonidan qayta yozilib qolishi mumkin.

Buning o'rniga lokal o'zgaruvchilardan foydalaning va [yopishni](https://www.w3schools.com/js/js\_function\_closures.asp) qanday ishlatishni o'rganing.

### Har doim lokal o'zgaruvchilarni e'lon qiling

Funktsiyada ishlatiladigan barcha o'zgaruvchilar lokal o'zgaruvchi sifatida e'lon qilinishi kerak.

Lokal oʻzgaruvchilar `var`, `let` yoki `const` kalit soʻzlari bilan eʼlon qilinishi kerak, aks holda ular global oʻzgaruvchilarga aylanadi.

{% hint style="warning" %}
Qatiy rejim eʼlon qilinmagan oʻzgaruvchilardan foydalanishga ruhsat bermaydi.
{% endhint %}

### Yuqorida e'lon qilish

Eʼlon qilishni script yoki funksiya tepasida yozish good practice hisoblanadi.

Bu:

* ‌Kodni tartibli qladi
* ‌Lokal o'zgaruvchilarni qidirish uchun yagona joyni taqdim etadi
* ‌Keraksiz global o'zgaruvchilardan saqlanishni osonlashtiradi
* ‌Keraksiz narsani qayta eʼlon qilish ehtimolini kamaytiradi.

```
// Declare at the beginning
let firstName, lastName, price, discount, fullPrice;

// Use later
firstName = "John";
lastName = "Doe";

price = 19.90;
discount = 0.10;

fullPrice = price - discount;
```

Bu loopning o'zgaruvchilari uchun ham amal qiladi:

```
for (let i = 0; i < 5; i++) {
```

### O'zgaruvchilarni ishga tushirish

Oʻzgaruvchini eʼlon qilinishi bilanoq ishga tushirish good practice hisoblanadi.

Bu:

* ‌Kodni tartibli qiladi
* ‌‌O'zgaruvchilarni ishga tushirish uchun bitta joyni taqdim etadi
* `‌undefined` qiymatlardan saqlaniladi

```
// Declare and initiate at the beginning
let firstName = "";
let lastName = "";
let price = 0;
let discount = 0;
let fullPrice = 0,
const myArray = [];
const myObject = {};
```

{% hint style="warning" %}
O'zgaruvchilarni ishga tushirish foydalanishga va ma'lumotlar turiga moʻljallangan tushuncha beradi.
{% endhint %}

### Obyektlarni const bilan e'lon qiling

Obyektlarni const bilan e'lon qilish har qanday tasodifiy turdagi o'zgarishlarning oldini oladi:

```
let car = {type:"Fiat", model:"500", color:"white"};
car = "Fiat";      // Changes object to string
```

```
const car = {type:"Fiat", model:"500", color:"white"};
car = "Fiat";      // Not possible
```

### Araylarni const bilan e'lon qiling

Massivlarni const bilan e'lon qilish har qanday tasodifiy turdagi o'zgarishlarning oldini oladi:

```
let cars = ["Saab", "Volvo", "BMW"];
cars = 3;    // Changes array to number
```

```
const cars = ["Saab", "Volvo", "BMW"];
cars = 3;    // Not possible
```

### New Object() dan foydalanmang

* `new Object()`dan foydalanmang&#x20;
* `new String()` o'rniga `""` dan foydalaning&#x20;
* `new Number()` oʻrniga `0` dan foydalaning
* `new Boolean()` o'rniga `false` dan foydalaning&#x20;
* `new Object()` oʻrniga `{}` dan foydalaning
* `new Array()` oʻrniga `[]` dan foydalaning&#x20;
* `new RegExp()` oʻrniga `/()/` dan foydalaning&#x20;
* `new Function()` oʻrniga function `(){}` dan foydalaning

```
let x1 = "";             // new primitive string
let x2 = 0;              // new primitive number
let x3 = false;          // new primitive boolean
const x4 = {};           // new object
const x5 = [];           // new array object
const x6 = /()/;         // new regexp object
const x7 = function(){}; // new function object
```

### Avtomatik turdagi konversiyalardan ehtiyot bo'ling

JavaScript erkin turda.

O'zgaruvchi barcha ma'lumotlar turlarini o'z ichiga olishi mumkin.

O'zgaruvchi ma'lumotlar turini o'zgartirishi mumkin.

```
let x = "Hello";     // typeof x is a string
x = 5;               // changes typeof x to a number
```

E'tibor bering, raqamlar tasodifan stringlarga yoki `NaN` ga aylantirilishi mumkin.

Arifmetik amallarni bajarayotganda, JavaScript raqamlarni stringga aylantira oladi:

```
let x = 5 + 7;       // x.valueOf() is 12,  typeof x is a number
let x = 5 + "7";     // x.valueOf() is 57,  typeof x is a string
let x = "5" + 7;     // x.valueOf() is 57,  typeof x is a string
let x = 5 - 7;       // x.valueOf() is -2,  typeof x is a number
let x = 5 - "7";     // x.valueOf() is -2,  typeof x is a number
let x = "5" - 7;     // x.valueOf() is -2,  typeof x is a number
let x = 5 - "x";     // x.valueOf() is NaN, typeof x is a number
```

Stringni stringdan ayirish xato boʻlmaydi, ammo NaN qaytaradi.

```
"Hello" - "Dolly"    // returns NaN
```

### === li taqqoslashdan foydalaning

`==` taqqoslash operatori har doim taqqoslashdan oldin (mos turlarga) aylantiradi.

`===` operatori qiymatlar va malumot turini taqqoslaydi:

```
0 == "";        // true
1 == "1";       // true
1 == true;      // true

0 === "";       // false
1 === "1";      // false
1 === true;     // false
```

### Standart parametrlardan foydalaning

Agar funksiya yetishmayotgan argument bilan chaqirilsa, yetishmayotgan argumentning qiymati undefined deb belgilanadi.

Undefined qiymatlar kodingizni buzishi mumkin. Argumentlarga standart qiymatlar berish good practice hisoblanadi.

```
function myFunction(x, y) {
  if (y === undefined) {
    y = 0;
  }
}
```

{% code title="ECMAScript 2015 funksiyada standart parametrlarga ruxsat beradi:" %}
```
function (a=1, b=1) { /*function code*/ }
```
{% endcode %}

[Funksiya parametrlari](https://www.w3schools.com/js/js\_function\_parameters.asp) boʻlimida funksiyaning parametrlari va argumentlari haqida batafsil bilib oling.

### Switchlaringizni default bilan tugating

Switch steytmentlaringizni har doim default bilan yakunlang. Garchi bunga hojat yo'q deb o'ylasangiz ham.

```
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
    break;
  default:
    day = "Unknown";
}
```

### Raqam, string va booleanlardan obyekt sifatida foydalanishdan saqlaning

Raqamlar, stringlar yoki booleanlardan har doim primitiv qiymat sifatida foydalaning. Obyekt sifatida emas.

Ushbu maʼlumot turlarini obyekt sifatida e'lon qilish, kodni ishlash tezligini sekinlashtiradi va yomon oqibatlarga olib keladi:

```
let x = "John";             
let y = new String("John");
(x === y) // is false because x is a string and y is an object.
```

Yoki undan ham yomoni:

```
let x = new String("John");             
let y = new String("John");
(x == y) // is false because you cannot compare objects.
```

### eval() dan foydalanishdan saqlaning

`Eval()` funksiyasi matnni kod sifatida ishlatish uchun ishlatiladi. Deyarli barcha holatlarda uni ishlatishga hojat boʻlmaydi.

Chunki u istalgan kodni ishga tushirishga imkon beradi, bu xavfsizlik muammosini ham keltirib chiqaradi.
