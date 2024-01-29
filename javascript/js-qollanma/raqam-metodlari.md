# Raqam metodlari

### JavaScript raqamlari usullari

Ushbu Number metodlarini barcha raqamlar bilan ishlatish mumkin:

| Metod           | Tavsif                                               |
| --------------- | ---------------------------------------------------- |
| toString()      | Raqamni stringga o'tkazadi                           |
| toExponential() | Ilmiy yozuvda yozilgan sonni qaytaradi               |
| toFixed()       | O'nli kasrlar bilan yozilgan raqamni qaytaradi       |
| toPrecision()   | Belgilangan uzunlik bilan yozilgan raqamni qaytaradi |
| ValueOf()       | Raqamni raqam sifatida qaytaradi                     |

### toString() metodi

`toString()` metodi raqamni string sifatida qaytaradi.

Barcha number metodlari har qanday turdagi raqamlarda (harf, o'zgaruvchilar yoki expressionlar) ishlatilishi mumkin:

```javascript
let x = 123;
x.toString();
(123).toString();
(100 + 23).toString();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_tostring" %}

### toExponential() metodi

`toExponential()`  yaxlitlangan va ilmiy belgilar bilan yozilgan string qaytaradi.

Parametr kasrning orqasidagi belgilar sonini belgilaydi:

```javascript
let x = 9.656;
x.toExponential(2);
x.toExponential(4);
x.toExponential(6);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_toexponential" %}

Parametr berish ixtiyoriy.  Agar parametr bermasangiz, JavaScript raqamni yaxlitlamaydi.

### toFixed() metodi

`toFixed()` o'nli kasrlar bilan yozilgan string qaytaradi:

```javascript
let x = 9.656;
x.toFixed(0);
x.toFixed(2);
x.toFixed(4);
x.toFixed(6);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_tofixed" %}

{% hint style="warning" %}
`toFixed(2)` pul bilan ishlash uchun juda mos keladi.
{% endhint %}

### toPrecision() metodi

`toPrecision()` maxsus uzunlik bilan birga berilgan raqamni stringda qaytaradi:

```javascript
let x = 9.656;
x.toPrecision();
x.toPrecision(2);
x.toPrecision(4);
x.toPrecision(6);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_toprecision" %}

### valueOf() metodi

`valueOf()` raqamni raqam sifatida qaytaradi.

```javascript
let x = 123;
x.valueOf();
(123).valueOf();
(100 + 23).valueOf();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_valueof" %}

JavaScript-da raqam primitive qiymat (typeof = number) yoki obyekt (typeof = object) bo'lishi mumkin.

`valueOf()` metodi JavaScript-da Number obyektlarini primitiv qiymatlarga aylantirish uchun ishlatiladi.

Uni kodingizda ishlatish uchun boshqa hech qanday sabab yo'q.

{% hint style="warning" %}
Barcha ma'lumot turlari `valueOf()` va `toString()` metodlariga ega.
{% endhint %}

### O'zgaruvchilarni raqamlarga aylantirish

O'zgaruvchini raqamga aylantirish uchun 3 ta JavaScript metodi mavjud:

| Metod        | Tavsif                                                |
| ------------ | ----------------------------------------------------- |
| number()     | Argumentdan konvertatsiya qilingan raqamni qaytaradi. |
| parseFloat() | Argumentni parse qiladi va float raqam qaytaradi      |
| parseInt()   | Argumentini parse qiladi va integer raqam qaytaradi   |

Yuqoridagi metodlar `number`ning metodlari emas. Ular JavaScriptdagi  **global** metodlardir.

### Number() metodi

`Number()` metodi o'zgaruvchilarni raqamlarga aylantirish uchun ishlatilishi mumkin:

```javascript
Number(true);
Number(false);
Number("10");
Number("  10");
Number("10  ");
Number(" 10  ");
Number("10.33");
Number("10,33");
Number("10 33");
Number("John");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_global_number" %}

{% hint style="warning" %}
Agar raqamni o'zgartirib bo'lmasa, `NaN` (Raqam emas) qaytariladi.
{% endhint %}

### Sanalarda ishlatiladigan Number() metodi

`Number()` sanani raqamga aylantirishi ham mumkin.

```javascript
Number(new Date("1970-01-01"))
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_global_number_date_0" %}

{% hint style="warning" %}
### Eslatma

`Date()` metodi 1.1.1970 yildan boshlab millisekundlar sonini qaytaradi.

1970-01-01 va 1970-01-02 oralig'idagi millisekundlar soni 86400000:
{% endhint %}

```javascript
Number(new Date("1970-01-02"))
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_global_number_date_1" %}

```javascript
Number(new Date("2017-09-30"))
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_global_number_date" %}

### parseInt() metodi

`parseInt()` stringni parse qiladi va integer qaytaradi. Bo'sh joylar kiritish mumkin. Lekin faqat birinchi raqam qaytariladi:

```javascript
parseInt("-10");
parseInt("-10.33");
parseInt("10");
parseInt("10.33");
parseInt("10 20 30");
parseInt("10 years");
parseInt("years 10");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_global_parseint" %}

Agar raqamni o'zgartirib bo'lmasa, `NaN` qaytariladi.

### parseFloat() metodi

`parseFloat()` stringni parse qiladi va raqam qaytaradi. Bo'sh joylar kiritish mumkin. Lekin faqat birinchi raqam qaytariladi:

```javascript
parseFloat("10");
parseFloat("10.33");
parseFloat("10 20 30");
parseFloat("10 years");
parseFloat("years 10");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_global_parsefloat" %}

Agar raqamni o'zgartirib bo'lmasa, `NaN` qaytariladi.

### Numberli obyekt metodlar

Ushbu obyekt metodlari Number obyektiga tegishli:

| Metod                  | Tavsif                                         |
| ---------------------- | ---------------------------------------------- |
| Number.isInteger()     | Argument integer bo'lsa, true  qaytaradi       |
| Number.isSafeInteger() | Argument xavfsiz integer bo'lsa true qaytaradi |
| Number.parseFloat()    | Stringni raqamga o'tkazadi                     |
| Number.parseInt()      | Stringni integerga o'tkazadi                   |



{% hint style="warning" %}
### O'zgaruvchilarda raqam metodlarini qo'llash mumkin emas

Yuqoridagi number metodlari faqati number obyektiga tegishli.

Ushbu metodlardan faqat `Number.isInteger()` kabi foydalanish mumkin.

X o'zgaruvchisidan  `X.isInteger()`  kabi foydalanish quyidagi hatoni chiqadi:

`TypeError X.isInteger is not a function`&#x20;
{% endhint %}

### Number.isInteger() metodi

Argument integer bo'lsa, `Number.isInteger()` metodi `true` qaytaradi.

```javascript
Number.isInteger(10);
Number.isInteger(10.5);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_es6_isinteger" %}

### Number.isSafeInteger() metodi

Xavfsiz integer - bu ikki tomonlama aniqlikdagi son sifatida aniq ifodalanishi mumkin bo'lgan integerdir.

Argument xavfsiz integer bo'lsa, `Number.isSafeInteger()` `true` qaytariladi.

```javascript
Number.isSafeInteger(10);
Number.isSafeInteger(12345678901234567890);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_es6_issafeinteger" %}

{% hint style="warning" %}
Xavfsiz integerlar  -(2⁵³ - 1) dan +(2⁵³ - 1) gacha bo'lgan butun sonlardir.\
Bu safe: 9007199254740991. Bu safe emas: 9007199254740992.
{% endhint %}

### Number.parseFloat() metodi

`Number.parseFloat()` stringni parse qiladi va raqamni qaytaradi.

Bo'sh joylarga ruxsat beriladi. Faqat birinchi raqam qaytariladi:

```javascript
Number.parseFloat("10");
Number.parseFloat("10.33");
Number.parseFloat("10 20 30");
Number.parseFloat("10 years");
Number.parseFloat("years 10");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_parsefloat" %}

Agar raqamni o'zgartirib bo'lmasa, `NaN` qaytariladi.

{% hint style="warning" %}
### Eslatma

`Number.parseInt()` va `Number.parseFloat()` Number metodlari&#x20;

&#x20;`parseInt()` va `parseFloat()` global metodlari bilan bir xil.

Maqsad globallarni modullashtirish (bir xil kodni brauzerdan tashqarida ishlatishni osonlashtirish uchun).
{% endhint %}

### Number.parseInt() metodi

`Number.parseInt()` stringni parse qiladi va integer qaytaradi.

Bo'sh joylarga ruxsat beriladi. Faqat birinchi raqam qaytariladi:

```javascript
Number.parseInt("-10");
Number.parseInt("-10.33");
Number.parseInt("10");
Number.parseInt("10.33");
Number.parseInt("10 20 30");
Number.parseInt("10 years");
Number.parseInt("years 10");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_parseint" %}

Agar raqamni o'zgartirib bo'lmasa, `NaN` qaytariladi.

{% hint style="warning" %}
### Number haqida to'liq ma'lumotnoma

Number haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda number haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_number.asp)

Ma'lumotnomada barcha number xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
