# Const

{% hint style="success" %}
`const` kalit so'zi ES6 (2015)da kiritilgan.

`const` bilan e'lon qilingan o'zgaruvchilarni qayta e'lon qilib bo'lmaydi.

`const` bilan e'lon qilingan  o'zgaruvchilarni qayta tayinlab bo'lmaydi.

`const` bilan e'lon qilingan o'zgaruvchilar **Block Scope** ga ega.
{% endhint %}

## Qayta tayinlash mumkin emas

`const` o'zgaruvchisini qayta tayinlab bo'lmaydi:

```javascript
const PI = 3.141592653589793;
PI = 3.14;      // Bu xatolik keltirib chiqaradi
PI = PI + 10;   // Bu ham xatolik keltirib chiqaradi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_const_value" %}

## Qiymat tayinlanishi shart

JavaScriptda `const` bilan o'zgaruvchi e'lon qilinganda ularga qiymat berilishi kerak:

{% code title="To'g'ri" %}
```javascript
const PI = 3.14159265359;
```
{% endcode %}

{% hint style="danger" %}
{% code title="Noto'g'ri" %}
```
const PI;
PI = 3.14159265359;
```
{% endcode %}
{% endhint %}

{% hint style="warning" %}
## const-dan qachon foydalanish kerak?

Qiymatni o'zgartirmasligini bilganingizda o'zgaruvchini har doim `const` bilan e'lon qiling.

Quyidagilardan birortasini e'lon qilganingizda `const`-dan foydalaning:

* Yangi massivda
* Yangi obyektda
* Yangi funksiyada
* Yangi RegExpda
{% endhint %}

### O'zgarmas obyektlar va massivlar

`const` biroz chalg'itadi.

`const` o'zgarmas qiymatni bildirmaydi. U qiymatga bo'glab qo'yiladigan o'zgarmas nomni ifodalaydi.

Shu sababli siz bularni qila olmaysiz:

* O'zgarmconsasning qiymatini qayta tayinlash
* O'zgarmas massivni qayta tayinlash
* O'zgarmas obyektni qayta tayinlash

Lekin bularni qila olasiz:

* O'zgarmas massiv elementlarini o'zgartirish
* O'zgarmas obyektning xususiyatlarini o'zgartirish

## O'zgarmas massivlar

O'zgarmas massivning elementlarini o'zgartirishingiz mumkin:

{% hint style="info" %}
O'zbek dasturchilari orasida **massiv**, **array** ham deyiladi
{% endhint %}

```javascript
// Siz o'zgarmas massiv yarata olasiz:
const cars = ["Saab", "Volvo", "BMW"];

// Uning elementlarini o'zgartira olasiz:
cars[0] = "Toyota";

// Unga yangi element ham qo'sha olasiz:
cars.push("Audi");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_const_array" %}

Lekin massivni qayta tayinlay olmaysiz:

```javascript
const cars = ["Saab", "Volvo", "BMW"];

cars = ["Toyota", "Volvo", "Audi"];    // XATO
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_const_array_assign" %}

### O'zgarmas obyektlar

O'zgarmas obyektning xususiyatlarini o'zgartirishingiz mumkin:

```javascript
// Siz o'zgarmas obyekt yarata olasiz:
const car = {type:"Fiat", model:"500", color:"white"};

// Uning xususiyatlarini o'zgartira olasiz:
car.color = "red";

// Unga yangi xususiyat qo'sha olasiz:
car.owner = "Johnson";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_const_object" %}

Lekin obyektni qayta tayinlay olmaysiz:

```javascript
const car = {type:"Fiat", model:"500", color:"white"};

car = {type:"Volvo", model:"EX60", color:"red"};    // XATO
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_const_object_assign" %}

## var, let va const o'rtasidagi farq

|       | Blok doirasida | Qayta e'lon qilish | Qatta tayinlash | Hoisting | this-ga bog'lanish |
| ----- | -------------- | ------------------ | --------------- | -------- | ------------------ |
| var   | Yo'q           | Ha                 | Ha              | Ha       | Ha                 |
| alet  | Ha             | Yo'q               | Ha              | Yo'q     | Yo'q               |
| const | Ha             | Yo'q               | Yo'q            | Yo'q     | Yo'q               |

## Afzalligi nimada ?

`let` va `const` blok doirasida bo'ladi.

`let` va `const` ni qayta e'lon qilib bo'lmaydi.

`let` va `const` foydalanilishdan avval e'lon qilinadi.

`let` va `const` `this` ga bog'lanmaydi.

`let` va `const` hoisting bo'lmaydi.

## Kamchiligi nimada ?

`var` e'lon qilinishi shart emas.

`var` hoisting bo'ladi.

`var` `this` ga bog'lanadi.

### Brauzerni qo'llab-quvvatlash

`const` kalit so'zi **Internet Explorer**-da to'liq qo'llab-quvvatlanmaydi.

Quyidagi jadvalda brauzerlar qaysi versiyadan boshlab `cons`ni to'liq qo'llab-quvvatlashi ko'rsatilgan:

| Chrom     | Edge      | Firefox    | Safari    |           |
| --------- | --------- | ---------- | --------- | --------- |
| Chrome 49 | Edge 12   | Firefox 36 | Safari 11 | Opera 36  |
| Mar, 2016 | Jul, 2015 | Feb, 2015  | Sep, 2017 | Mar, 2016 |

### Block scope

`const` bilan o'zgaruvchi e'lon qilishda **Block Scope** haqida gap ketsa u ham `let` ga o'xshaydi.

Ushbu misolda blok ichida e'lon qilingan `x` blokdan tashqarida e'lon qilingan `x` bilan bir xil emas:

```javascript
const x = 10;
// Bu yerda x 10

{
const x = 2;
// Bu yerda x 2
}

// Bu yerda x 10
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_const" %}

Block Scope haqida ko'proq ma'lumotlarni, [JavaScript scope](scope.md) bo'limidan olishingiz mumkin.

### Qayta e'lon qilish

JavaScriptda `var` bilan e'lon qilingan o'zgaruvchini dasturning istalgan joyida qayta e'lon qilishga ruxsat beriladi:

```javascript
var x = 2;     // Mumkin
var x = 3;     // Mumkin
x = 4;         // Mumkin
```

`var` yoki `let` bilan e'lon qilingan o'zgaruvchini  bir xil scopeda ham qayta e'lon qilib bo'lmaydi:

```javascript
var x = 2;     // Mumkin 
const x = 2;   // Mumkin emas

{
let x = 2;     // Mumkin 
const x = 2;   // Mumkin emas
}

{
const x = 2;   // Mumkin 
const x = 2;   // Mumkin emas
}
```

`const` bilan e'lon qilingan o'zgaruvchini bir xil scopeda qayta tayinlab bo'lmaydi:

```javascript
const x = 2;     // Mumkin 
x = 2;           // Mumkin emas
var x = 2;       // Mumkin emas
let x = 2;       // Mumkin emas
const x = 2;     // Mumkin emas

{
  const x = 2;   // Mumkin 
  x = 2;         // Mumkin emas
  var x = 2;     // Mumkin emas
  let x = 2;     // Mumkin emas
  const x = 2;   // Mumkin emas
}
```

`const` bilan e'lon qilingan o'zgaruvchini boshqa scope da yoki boshqa block da qayta e'lon qilishga ruxsat beriladi:

```javascript
const x = 2;       // Mumkin 

{
  const x = 3;   // Mumkin 
}

{
  const x = 4;   // Mumkin 
}
```

## Hoisting

`var` bilan e'lon qilingan o'zgaruvchilar tepaga ko'tariladi  va istalgan vaqtda ishga tushirilishi mumkin.

Bu degani: O'zgaruvchini e'lon qilingan joydan tepada ham ishlatishingiz mumkin, bu **hoisting** deyiladi:

{% code title="Bu yaxshi:" %}
```javascript
carName = "Volvo";
var carName;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_let_hoisting_var" %}

Agar siz **hoisting** haqida ko'proq ma'lumotga ega bo'lmoqchi bo'lsangiz, [JavaScript hoisting](https://www.w3schools.com/js/js\_hoisting.asp) bo'limini o'rganing.

`const` bilan e'lon qilingan o'zgaruvchilar ham blokning yuqori qismiga chiqadi, lekin ishlamaydi.

Bu degani: `const` bilan e'lon qilingan o'zgaruvchining tepa qismida o'zgaruvchidan foydalanish `ReferenceError` xatoligiga olib keladi.

{% code title="Xato" %}
```javascript
carName = "Saab";
const carName = "Volvo";
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_const_hoisting" %}
