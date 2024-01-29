---
description: >-
  BigInt o'zgaruvchilari oddiy raqamlarga qaraganda juda katta bo'lgan
  qiymatlarni saqlash uchun ishlatiladi.
---

# BigInt

### JavaScript butun son aniqligi

Butun sonlar 15 tagacha aniq ko'rsatiladi.

```javascript
let x = 999999999999999;   // x 999999999999999 bo'ladi
let y = 9999999999999999;  // y 10000000000000000 bo'ladi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_inaccurate1" %}

JavaScript-da barcha raqamlar 64-bitli float formatida (IEEE 754 standarti) saqlanadi.

Ushbu standart bilan katta integerni aniq ko'rsatib bo'lmaydi va u yaxlitlanadi.

Shu sababli, JavaScript faqat integerlarni xavfsiz tarzda ifodalashi mumkin:

9007199254740991 gacha +(2⁵³ -1)

va

Manfiy -9007199254740991 -(2⁵³ -1).

Bu diapazondan katta yoki kichi bo'lgan integer qiymatlar aniqlikni yo'qotadi.

### BigInt qanday yaratiladi

`BigInt()` ni yaratish uchun integerning oxiriga n qo'shing yoki `BigInt`ni chaqiring:

```javascript
let x = 9999999999999999;
let y = 9999999999999999n;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_bigint" %}

```javascript
let x = 1234567890123456789012345n;
let y = BigInt(1234567890123456789012345)
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_bigint_create" %}

### BigInt: JavaScriptning yangi ma'lumot turi

JavaScriptda `BigInt`ning `typeof` qiymati "`bigint`":

```javascript
let x = BigInt(999999999999999);
let type = typeof x;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_bigint_typeof" %}

`BigInt` JavaScript-dagi ikkinchi raqamli ma'lumotlar turi hisoblanadi ( `Number`dan keyin ).

`BigInt` bilan hisoblaganda javaScript-dagi ma'lumot turlarining umumiy soni 8 tani tashkil qiladi:

1. String
2. Number
3. Bigint
4. Boolean
5. Undefined
6. Null
7. Symbol
8. Object

### BigInt operatorlari

`Number`da ishlatilishi mumkin bo'lgan operatorlar `BigInt`-da ham ishlatilishi mumkin.

{% code title="BigInt-ni ko'paytirishga misol" %}
```javascript
let x = 9007199254740995n;
let y = 9007199254740995n;
let z = x * y;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_bigint_multiply" %}

{% hint style="warning" %}
### Eslatmalar

`BigInt` va  `Number` o'rtasida arifmetik amal bajarishga ruxsat berilmaydi (ma'lumot turini konvertatsiya qilish ma'lumotlarni yo'qotadi).

Unsigned right shift (>>>)  `BigInt`da amalga oshirilmaydi (u belgilangan kenglikka ega emas).
{% endhint %}

### BigInt o'nlik raqamlari

`BigInt`da oʻnli kasrlar boʻlishi mumkin emas.

{% code title="BigInt qiymatlarni bo'lishga misol" %}
```javascript
let x = 5n;
let y = x / 2;
// Error: Cannot mix BigInt and other types, use explicit conversion.
let x = 5n;
let y = Number(x) / 2;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_bigint_divide" %}

### BigInt Hex, Octal va Binary

`BigIntda` oʻn oltilik, sakkizlik yoki ikkilik sanoq tizimilari ham ham yozilishi mumkin:

{% code title="BigIntda Hex-ga misol" %}
```javascript
let hex = 0x20000000000003n;
let oct = 0o400000000000000003n
let bin = 0b100000000000000000000000000000000000000000000000000011n;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_bigint_octal" %}

### Aniqlikdagi sinchkovlik

Yaxlitlash dastur xavfsizligini buzishi mumkin:

{% code title=" MAX_SAFE_INTEGERga misol:" %}
```javascript
9007199254740992 === 9007199254740993; // true bo'ladi !!!
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_max_safe_error" %}

### Brauzerning qo'llab-quvvatlashi

`BigInt` 2020-yil sentabridan boshlab barcha brauzerlarda qo‘llab-quvvatlanadi:

| Chrome    | Edge     | Firefox    | Safari    |          |
| --------- | -------- | ---------- | --------- | -------- |
| Chrome 67 | Edge 79  | Firefox 68 | Safari 14 | Opera 54 |
| May 2018  | Jan 2020 | Jul 2019   | Sep 2020  | Jun 2018 |

### Minimal va maksimal xavfsiz integerlar

[ES6](https://www.w3schools.com/js/js\_es6.asp) Number obyektiga max va min xususiyatlarini qo'shdi:

* `MAX_SAFE_INTEGER`
* `MIN_SAFE_INTEGER`

{% code title="MAX_SAFE_INTEGERga  misol" %}
```javascript
let x = Number.MAX_SAFE_INTEGER;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_es6_max_safe" %}

{% code title="MIN_SAFE_INTEGERga misol" %}
```javascript
let x = Number.MIN_SAFE_INTEGER;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_es6_min_safe" %}

### Nymberning tangi metodlari

[ES6](https://www.w3schools.com/js/js\_es6.asp) shuningdek Number obektiga ikkita yangi metod qo'shdi:

* `Number.isInteger()`
* `Number.isSafeInteger()`

### Number.isInteger() metodi

Argument integer bo'lsa, `Number.isInteger()` metodi `true` aytaradi.

{% code title="isInteger() ga misol" %}
```javascript
Number.isInteger(10);
Number.isInteger(10.5);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_es6_isinteger" %}

### Number.isSafeInteger() metodi

Xavfsiz integer - bu ikki tomonlama aniqlikdagi son sifatida aniq ifodalanishi mumkin bo'lgan integer.

Argument xavfsiz integer bo'lsa, `Number.isSafeInteger()` metodi `true` aytariladi.

{% code title="SafeInteger() ga misol" %}
```javascript
Number.isSafeInteger(10);
Number.isSafeInteger(12345678901234567890);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_es6_issafeinteger" %}

{% hint style="warning" %}
Xavfsiz integerlar  -(2 53 - 1) dan +(2 53 - 1) gacha bo'lgan integerlar hisoblanadi.\
Bu xavfsiz: 9007199254740991. Bu xavfsiz emas: 9007199254740992.
{% endhint %}
