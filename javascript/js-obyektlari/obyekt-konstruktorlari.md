# Obyekt konstruktorlari

```
function Person(first, last, age, eye) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eye;
}
```

{% hint style="warning" %}
### Eslatmalar

Konstruktor funksiyalarini katta harf bilan nomlash good practice hisoblanadi.

### This haqida

Konstruktor funksiyasida `this` qiymatga ega emas. Bu yangi obyektning o'rnini bosuvchi vositadir. `This`ning qiymati yangi obyekt yaratilganda yangi obyektga aylanadi.

### Buni ham o'qing:

[Javascriptda **this** qo'llanmasi](https://www.w3schools.com/js/js\_this.asp)
{% endhint %}

### Obyekt turlari (rejalar) (klasslar)

Oldingi bo'limlardagi misollar qisqacha misol edi. Ular faqat bitta obyekt yaratardi.

Ba'zan bizga bir xil "turdagi" ko'plab obyektlarni yaratish uchun "**reja"** kerak bo'ladi**.**

**"Obyekt turi"** ni yaratish usuli **obyekt konstruktori funktsiyasidan** foydalanishdir.

Yuqoridagi misolda `function Person()` obyekt konstruktor funktsiyasi hisoblanadi.

Bir xil turdagi obyektlar konstruktor funksiyasini `new` kalit so'zi bilan chaqirish orqali yaratiladi:

```
const myFather = new Person("John", "Doe", 50, "blue");
const myMother = new Person("Sally", "Rally", 48, "green");
```

### This nima ?

JavaScript-da `this` kalit so'zi obyektga yo'naladi qiladi.

`this` qaysi obyekt qanday chaqirilayotganiga (ishlatilganiga yoki chaqirilganiga) bog'liq.

`this` kalit so'zi qanday ishlatilishiga qarab turli xil obyektlarga yo'naladi qiladi:

| `this` obyekt metodida obyektning o'ziga yo'naladi.                                             |
| ----------------------------------------------------------------------------------------------- |
| `this`  yakka holda,  global obyektga yo'naladi.                                                |
| `this` funktsiyada global obyektga yo'naladi.                                                   |
| `this` qat'iy rejimda funktsiyada `undefined` bo'ladi                                           |
| `this` eventda, hodisani qabul qilgan elementga yo'naladi.                                      |
| `call()`, `apply()`va `bind()` kabi metodlar `this`ni har qanday obyektga yo'naltirishi mumkin. |

{% hint style="warning" %}
### Eslatma

`this` o'zgaruvchi emas. Bu kalit so'z. `this`ning qiymatini o'zgartira olmaysiz.

### Shuningdek qarang:

[JavaScriptda **this** qo'llanmasi](https://www.w3schools.com/js/js\_this.asp)
{% endhint %}

### Obyektga xususiyat qo'shish

Mavjud obyektga yangi xususiyat qo'shish oson:

```
myFather.nationality = "English";
```

Xusuiyat `myFather`-ga qo'shiladi. `myMother`-ga emas. (Boshqa hech qaysi person obyektiga emas).

### Obyektga metod qo'shish

Mavjud obyektga yangi metod qo'shish oson:

```
myFather.name = function () {
  return this.firstName + " " + this.lastName;
};
```

Metod `myFather`-ga qo'shiladi. `myMother`-ga emas. (Boshqa hech qaysi person obyektiga emas).

### Konstruktorga xususiyat qo'shish

Siz mavjud obyektga yangi xususiyat qo'shgan usulingizda foydalanib obyekt konstruktoriga yangi xususiyat qo'sha olmaysiz:

```
Person.nationality = "English";
```

Konstruktorga yangi xususiyat qo'shish uchun uni konstruktor funksiyasiga qo'shishingiz kerak:

```
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
  this.nationality = "English";
}
```

{% hint style="warning" %}
Bunda obyekt xususiyatlari standart qiymatlarga ega bo'lishi mumkin.
{% endhint %}

### Konstruktorga metod qo'shish

Konstruktor funksiyangiz metodlarni ham belgilashi mumkin:

```
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
  this.name = function() {
    return this.firstName + " " + this.lastName;
  };
}
```

Siz mavjud obyektga yangi metod qo'shgan usulingizdan foydalanib obyekt konstruktoriga yangi metod qo'sha olmaysiz.

Obyekt konstruktoriga metodlarni qo'shish konstruktor funktsiyasi ichida amalga oshirilishi kerak:

```
function Person(firstName, lastName, age, eyeColor) {
  this.firstName = firstName; 
  this.lastName = lastName;
  this.age = age;
  this.eyeColor = eyeColor;
  this.changeName = function (name) {
    this.lastName = name;
  };
}
```

ChangeName() funksiyasi name qiymatini personning lastName xususiyatiga belgilaydi.

#### Endi sinab ko'rishingiz mumkin:

```
myMother.changeName("Doe");
```

JavaScript `this`ni myMother bilan “almashtirish” orqali qaysi person haqida gapirayotganingizni biladi.

### Built-in konstruktorlar

JavaScript-da lokal obyektlar uchun built-in konstruktorlar mavjud:

```
new String()    // A new String object
new Number()    // A new Number object
new Boolean()   // A new Boolean object
new Object()    // A new Object object
new Array()     // A new Array object
new RegExp()    // A new RegExp object
new Function()  // A new Function object
new Date()      // A new Date object
```

{% hint style="warning" %}
`Math()` obyekti ro'yxatda yo'q. `Math` global obyekt hisoblanadi. `Math` da `new` kalit so'zidan foydalanib bo'lmaydi.
{% endhint %}

### Bilasizmi ?

Yuqorida ko'rib turganingizdek, JavaScript-da `String`, `Number` va `Boolean` kabi sodda ma'lumot turlarining obyekt versiyalari mavjud. Murakkab obyekt yaratish uchun biror bir sabab yo'q. Sodda tur bilan e'lon qilingan o'zgaruvchilar obyekt sifatida e'lon qilinganlaridan tezroq ishlaydi.

`new Object()` ning o'rniga `{}` dan foydalaning

`new String()` o'rniga `""` dan foydalaning

`new Number()` ning o'rniga `0` dan foydalaning

`new Boolean()` ning o'rniga `false` dan foydalaning

&#x20;`new Array()` ning o'rniga `[]` dan foydalaning

`new RegExp()` ning o'rniga `/()/` dan foydalaning

`new Function()` ning o'rniga funksiya ifodasi bo'lgan  `() {}` dan foydalaning.

```
let x1 = "";             // new primitive string
let x2 = 0;              // new primitive number
let x3 = false;          // new primitive boolean

const x4 = {};           // new Object object
const x5 = [];           // new Array object
const x6 = /()/          // new RegExp object
const x7 = function(){}; // new function
```

### String obyektlari

Odatda, stringlar primitiv sifatida yaratiladi: `firstName = "John"`

Ammo stringlar `new` kalit so'zi yordamida obekt sifatida ham yaratilishi mumkin:\
`firstName = new String("John")`

Nima uchun stringlar obyekt sifatida yaratilmasligi kerakligi haqida Javascriptda Stringlar bo'limida bilib oling.

### Raqamli obyektlar

Odatda, raqamlar primitiv sifatida sifatida yaratiladi: `x = 30`

Ammo raqamlarni `new` kalit so'zi yordamida obyekt sifatida ham yaratish mumkin:\
`x = new Number(30)`

Nima uchun raqamlar obyekt sifatida yaratilmasligi kerakligini JS raqamlari bo'limida bilib oling.

### Boolean obyektlar

Odatda, booleanlar promitiv sifatida yaratiladi: `x = false`

Ammo booleanlarni ham `new` kalit so'zi yordamida obyekt sifatida yaratish mumkin:\
`x = new Boolean(false)`

[JS Boolean](https://www-w3schools-com.translate.goog/js/js\_booleans.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) bo'limida nega booleanlarni obyekt sifatida yaratmaslik kerakligini bilib oling.
