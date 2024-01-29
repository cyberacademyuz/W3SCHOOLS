# Typeof

JavaScript-da qiymatlarni o'z ichiga oluvchi 5 xil ma'lumotlar turi mavjud:

* `string`
* `number`
* `boolean`
* `object`
* `function`

6 xil obekt turlari bor:

* `Object`
* `Date`
* `Array`
* `String`
* `Number`
* `Boolean`

va qiymatni o'z ichiga olmaydi 2 ma'lumot turi mavjud:

* `null`
* `undefined`

### typeof operatori

O'zgaruvchining ma'lumot turini aniqlash uchun `typeof` operatoridan foydalanishingiz mumkin.

```
typeof "John"                 // Returns "string"
typeof 3.14                   // Returns "number"
typeof NaN                    // Returns "number"
typeof false                  // Returns "boolean"
typeof [1,2,3,4]              // Returns "object"
typeof {name:'John', age:34}  // Returns "object"
typeof new Date()             // Returns "object"
typeof function () {}         // Returns "function"
typeof myCar                  // Returns "undefined" *
typeof null                   // Returns "object"
```

E'tibor bering:

* NaN ma'lumotlar turi - number (raqam)
* Massivning ma'lumot turi obekt
* Date ma'lumot turi obekt
* Null ma'lumot turi obekt
* Undefined o'zgaruvchining ma'lumot turi **undefined** \*
* Qiymat tayinlanmagan o'zgaruvchining ma'lumotlar turi ham **undefined** \*

{% hint style="warning" %}
Obyek massiv (yoki Date) ekanligini aniqlash uchun `typeof` dan foydalana olmaysiz.
{% endhint %}

### Primitiv ma'lumotlar

Primitiv ma'lumotlar qo'shimcha xususiyat va metodlarga ega bo'lmagan oddiy ma'lumot qiymatlari hisoblanadi.

`typeof` operatori bu primitiv turlardan birini qaytarishi mumkin:

* `string`
* `number`
* `boolean`
* `undefined`

```
typeof "John"              // Returns "string"
typeof 3.14                // Returns "number"
typeof true                // Returns "boolean"
typeof false               // Returns "boolean"
typeof x                   // Returns "undefined" (if x has no value)
```

### Complex ma'lumotlar

`typeof` operatori ikkita complex turdan birini qaytaradi:

* `function`
* `object`

`typeof` operatori obektlar, massivlar va null ma'lumot turlari uchun "object" ni qaytaradi.

`typeof` operatori funksiyalar uchun "obekt" qaytarmaydi.

```
typeof {name:'John', age:34} // Returns "object"
typeof [1,2,3,4]             // Returns "object" (not "array", see note below)
typeof null                  // Returns "object"
typeof function myFunc(){}   // Returns "function"
```

{% hint style="warning" %}
`typeof` operatori massivlar uchun "`object`" qaytaradi, chunki JavaScript-da massivlar obekt hisoblanadi
{% endhint %}

### Typeof-ning ma'lumot turi

`typeof` operatori o'zgaruvchi emas. U operator. Operatorlar ( + - \* / ) ma'lumot turiga ega bo'lmaydi.

Biroq, `typeof` operatori har doim **string** qaytaradi (operand turini o'z ichiga olgan).

### constructor xususiyati

`constructor` xususiyati barcha o'zgaruvchilar uchun `constructor` funksiyasini qaytaradi.

```
"John".constructor                // Returns function String()  {[native code]}
(3.14).constructor                // Returns function Number()  {[native code]}
false.constructor                 // Returns function Boolean() {[native code]}
[1,2,3,4].constructor             // Returns function Array()   {[native code]}
{name:'John',age:34}.constructor  // Returns function Object()  {[native code]}
new Date().constructor            // Returns function Date()    {[native code]}
function () {}.constructor        // Returns function Function(){[native code]}
```

Obektning `Array` ("Array" so'zini o'z ichiga olgan) ekanligini bilish uchun konstruktor xususiyatini tekshirishingiz mumkin:

```
function isArray(myArray) {
  return myArray.constructor.toString().indexOf("Array") > -1;
}
```

Yoki undan ham osoni, obektning **Array funktsiyasi** ekanligini tekshirishingiz mumkin:

```
function isArray(myArray) {
  return myArray.constructor === Array;
}
```

Obektning `Date`("Date" so'zini o'z ichiga olgan) ekanligini aniqlash uchun constructor xususiyatini tekshirishingiz mumkin:

```
function isDate(myDate) {
  return myDate.constructor.toString().indexOf("Date") > -1;
}
```

Yoki undan ham osoni, obektning **Date funktsiyasi** ekanligini tekshirishingiz mumkin :

```
function isDate(myDate) {
  return myDate.constructor === Date;
}
```

### Undefined

JavaScript-da qiymatsiz o'zgaruvchi `undefined` qiymatiga ega. Uning turi ham `undefined`.

```
let car;    // Value is undefined, type is undefined
```

Qiymatni `undefined` qilish orqali har qanday o'zgaruvchini bo'shatish mumkin. Shunda uning turi ham  `undefined` bo'ladi.

```
car = undefined;    // Value is undefined, type is undefined
```

### Bo'sh qiymatlar

Bo'sh qiymatni `undefined` bilan  hech qanday aloqasi yo'q.

Bo'sh string, qiymatga ham , o'z turiga ham  ega.

```
let car = "";    // The value is "", the typeof is "string"
```

### Null

JavaScript-da `null` "hech narsa". Bu hali mavjud bo'lmagan narsa bo'lishi kerak.

Afsuski, JavaScript-da `null`ning ma'lumot turi obekt hisoblanadi.

{% hint style="warning" %}
Siz JavaScript-dagi xato deb hisoblashingiz mumkin bo'lgan narsa `typeof null`ning obektligi. U null bo'lishi kerak.
{% endhint %}

Obektni `null` qilish orqali uni bo'shatish mumkin:

```
let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
person = null;    // Now value is null, but type is still an object
```

Obektni `undefined` qilish orqali ham bo'shatish mumkin:

```
let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
person = undefined;   // Now both value and type is undefined
```

### Undefined va null o'rtasidagi farq

`undefined` va `null` qiymat jihatidan bir xil, ammo ularning turi farq qiladi:

```
typeof undefined           // undefined
typeof null                // object

null === undefined         // false
null == undefined          // true
```

### instanceof operatori

Agar obekt berilgan obektning namunasi bo'lsa, `instanceof` operatori `true` qaytaradi:

```
const cars = ["Saab", "Volvo", "BMW"];

(cars instanceof Array);
(cars instanceof Object);
(cars instanceof String);
(cars instanceof Number);
```

### void operatori

Void operatori expressionni baholaydi va **undefined** qaytaradi. Ushbu operator ko'pincha "void (0)" yordamida undefined primitiv qiymatni olish uchun ishlatiladi (returndan foydalanmasdan expressionni baholashda foydali).

```
<a href="javascript:void(0);">
  Useless link
</a>

<a href="javascript:void(document.body.style.backgroundColor='red');">
  Click me to change the background color of body to red
</a>
```
