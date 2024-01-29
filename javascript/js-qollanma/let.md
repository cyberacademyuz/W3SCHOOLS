# Let

{% hint style="success" %}
`let` kalit so'zi [ES6 (2015)](https://www.w3schools.com/js/js\_es6.asp) da kiritilgan.

E'lon qilingan o'zgaruvchilarni `let` bilan qayta e'lon qilib bo'lmaydi.

`let`bilan e'lon qilingan o'zgaruvchilar foydalanishdan avval e'lon qilinishi kerak.

`let` bilan e'lon qilingan o'zgaruvchilar **block scope**ga ega.
{% endhint %}

## Qayta e'lon qilib bo'lmaydi

`let` bilan e'lon qilingan o'zgaruvchilarni qayta e'lon qilib bo'lmaydi.

O'zgaruvchini bexosdan qayta e'lon qila olmaysiz.

{% code title="let bilan quyidagidek qila olmaysiz:" %}
```javascript
let x = "John Doe";

let x = 0;

// SyntaxError: 'x' has already been declared
```
{% endcode %}

{% code title="var  bilan esa qila olasiz:" %}
```javascript
var x = "John Doe";

var x = 0;
```
{% endcode %}

## Blok Scope

ES6 (2015) dan oldin JavaScript faqat **Global Scope** va **Function Scope**ga ega edi.

ES6 ikkita muhim yangi kalit so'zlarni taqdim qildi: `let` va `const`.

Ushbu ikki kalit so'z JavaScript-da **Block Scope**ni taqdim qildi.

{ } bloki ichida e'lon qilingan o'zgaruvchilardan blokdan tashqarida foydalanib bo'lmaydi:

```javascript
{
  let x = 2;
}
// x dan bu yerda foydalanib bo'lmayd
```

`var` kalit so'zi bilan e'lon qilingan o'zgaruvchilar **block scope**ga ega emas.

{ } bloki ichida e'lon qilingan o'zgaruvchilardan blokdan tashqarida foydalanish mumkin.

```javascript
{
  var x = 2;
}
// x dan bu yerda foydalansa bo'ladi
```

## O'zgaruvchilarni qayta e'lon qilish

`var` yordamida o'zgaruvchini qayta e'lon qilish turli muammolar keltirib chiqarishi mumkin.

O'zgaruvchini block ichida qayta e'lon qilish uni blokdan tashqarida ham qayta e'lon qiladi:

```javascript
var x = 10;
// Bu yerda x qiymati 10

{
var x = 2;
// Bu yerda x qiymati 2
}

// Bu yerda x qiymati 2
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_es6_var" %}

O'zgaruvchini `let` kalit so'zi yordamida qayta e'lon qilish bu muammoni hal qilishi mumkin.

O'zgaruvchini block ichida qayta e'lon qilish uni blokdan tashqarida qayta e'lon qilmaydi:

```javascript
let x = 10;
// Bu yerda x qiymati 10

{
let x = 2;
// Bu yerda x qiymati 2
}

// Bu yerda x qiymati 10
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_es6_let" %}

## var, let va const o'rtasidagi farq

|       | Blok doirasida | Qayta e'lon qilish | Qayta tayinlash | Hoisting | this-ga bog'lanish |
| ----- | -------------- | ------------------ | --------------- | -------- | ------------------ |
| var   | Yo'q           | Ha                 | Ha              | Ha       | Ha                 |
| let   | Ha             | Yo'q               | Ha              | Yo'q     | Yo'q               |
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

## Brauzerni qo'llab-quvvatlash

`let` kalit so'zi **Internet Explorer 11** yoki undan avvalgi versiyalarda to'liq qo'llab-quvvatlanmaydi.

Quyidagi jadvalda brauzerlar qaysi versiyadan boshlab `let`ni to'liq qo'llab-quvvatlashi ko'rsatilgan:

| Chrome     | Edge       | Firefox      | Safari        |           |
| ---------- | ---------- | ------------ | ------------- | --------- |
| Chrome 49  | Edge 12    | Firefox 44   | Safari 11     | Opera 36  |
| Mart, 2016 | Iyul, 2015 | Yanvar, 2015 | Sentabr, 2017 | Mar, 2016 |

## Qayta e'lon qilish

JavaScript oʻzgaruvchini dasturning istalgan joyida `var` bilan qayta eʼlon qilishga  ruxsat beriladi:

```javascript
var x = 2;
// x hozir 2

var x = 3;
// x hozir 3
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_let_redeclare_var" %}

`let` bilan bir xil blokdagi o'zgaruvchini qayta e'lon qilib bo'lmaydi.

```javascript
var x = 2;   // Mumkin
let x = 3;   // Mumkin emas

{
let x = 2;   // Mumkin
let x = 3;   // Mumkin emas
}

{
let x = 2;   // Mumkin 
var x = 3;   // Mumkin emas
}
```

Boshqa blokda oʻzgaruvchini let bilan qayta eʼlon qilishga ruxsat beriladi:

```javascript
let x = 2;   // Mumkin

{
let x = 3;   // Mumkin
}

{
let x = 4;    // Mumkin
}


console.log(x) // 2
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_let_redeclare" %}

## Let Hoisting

`var` bilan e'lon qilingan o'zgaruvchilar tepaga ko'tariladi  va istalgan vaqtda ishga tushirilishi mumkin.

Bu degani: O'zgaruvchini e'lon qilingan joydan tepada ham ishlatishingiz mumkin, bu **hoisting** deyiladi:

{% code title="Bu yaxshi:" %}
```javascript
carName = "Volvo";
var carName;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_let_hoisting_var" %}

Agar siz **hoisting** haqida ko'proq ma'lumotga ega bo'lmoqchi bo'lsangiz, [JavaScript hoisting](hoisting.md) bo'limini o'rganing.

`let` bilan e'lon qilingan o'zgaruvchilar ham blokning yuqori qismiga chiqadi, lekin ishlamaydi.

**Bu degani**: let bilan e'lon qilingan o'zgaruvchining tepa qismida o'zgaruvchidan foydalanish `ReferenceError` xatoligiga olib keladi.



{% hint style="danger" %}
{% code title="Misol:" %}
```javascript
carName = "Saab";
let carName = "Volvo";
```
{% endcode %}
{% endhint %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_let_hoisting_let" %}
