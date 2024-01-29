# Raqam xususiyatlari

| Xususiyat          | Ta'rif                                                     |
| ------------------ | ---------------------------------------------------------- |
| EPSILON            | 1 va  > 1 dan katta bo'lgan eng kichik son orasidagi farq. |
| MAX\_VALUE         | JavaScript-da mumkin bo'lgan eng katta raqam               |
| MIN\_VALUE         | JavaScript-da mumkin bo'lgan eng kichik raqam              |
| MAX\_SAFE\_INTEGER | Maksimal xavfsiz butun son (2⁵³ - 1)                       |
| MIN\_SAFE\_INTEGER | Minimum xavfsiz butun son (-2⁵³ - 1)                       |
| POSITIVE\_INFINITY | Infinity                                                   |
| NEGATIVE\_INFINITY | Manfiy infinity                                            |
| NaN                | "Not-a-Number" qiymati                                     |

### JavaScript EPSILON

`Number.EPSILON` bu 1 va 1 dan katta bo'lgan eng kichik float o'rtasidagi farq.

```javascript
let x = Number.EPSILON;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_epsilon" %}

{% hint style="warning" %}
### Eslatma

`Number.EPSILON` [ES6](https://www.w3schools.com/js/js\_es6.asp)ning xususiyati hisoblanadi.&#x20;

Bu Internet Explorer-da ishlamaydi.
{% endhint %}

### MAX\_VALUE

`Number.MAX_VALUE` JavaScript-da mumkin bo'lgan eng katta sonni ifodalovchi konstanta.

```javascript
let x = Number.MAX_VALUE;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_max" %}



{% hint style="warning" %}
### O'zgaruvchilarda Number xususiyatlaridan foydalanib bo'lmaydi

Number xususiyatlari JavaScriptning Number **obektiga** tegishli.

Bu xususiyatlardan faqat `Number.MAX_VALUE` kabi foydalanish mumkin.

X o'zgaruvchi yoki qiymat bo'lgan joyda  x.MAX\_VALUE  kabi foydalanish `undefined` qaytaradi:
{% endhint %}

```javascript
let x = 6;
x.MAX_VALUE
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_max_undefined" %}

### MIN\_VALUE

`Number.MIN_VALUE` JavaScript-da mumkin bo'lgan eng kichik sonni ifodalovchi konstanta.

```javascript
let x = Number.MIN_VALUE;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_min" %}

### MAX\_SAFE\_INTEGER

`Number.MAX_SAFE_INTEGER` JavaScript-da eng katta safe integerni ifodalaydi.

`Number.MAX_SAFE_INTEGER` bu (2⁵³ - 1) bo'ladi.

```javascript
let x = Number.MAX_SAFE_INTEGER;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_max_safe" %}

### MIN\_SAFE\_INTEGER

`Number.MIN_SAFE_INTEGER` JavaScript-dagi eng kichik safe integerni ifodalaydi.

`Number.MIN_SAFE_INTEGER` bu -(2⁵³ - 1) bo'ladi.

```javascript
let x = Number.MIN_SAFE_INTEGER;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_min_safe" %}

{% hint style="warning" %}
### Eslatma

`MAX_SAFE_INTEGER`va `MIN_SAFE_INTEGER` [ES6](https://www.w3schools.com/js/js\_es6.asp)ning xususiyatlari hisoblanadi.

Ular Internet Explorer-da ishlamaydi.
{% endhint %}

### POSITIVE\_INFINITY

```javascript
let x = Number.POSITIVE_INFINITY;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_pos_infinity" %}

`POSITIVE_INFINITY` Cheksizlik sodir bo'lganda qaytariladi:

```javascript
let x = 1 / 0;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_pos_infinity2" %}

### NEGATIVE\_INFINITY

```javascript
let x = Number.NEGATIVE_INFINITY;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_neg_infinity" %}

`NEGATIVE_INFINITY` manfiy tomonga niisbatan cheksizlik sodir bo'lganda qaytariladi:

```javascript
 let x = -1 / 0;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_neg_infinity2" %}

### NaN - Raqam emas

`NaN` raqam boʻlmagan raqam uchun JavaScriptning standart kalit soʻzi.

```javascript
let x = Number.NaN;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_nan" %}

Raqamdan tashkil topmagan string bilan arifmetik amal bajarishga harakat qilsh natijasida `NaN` qaytariladi:

```javascript
let x = 100 / "Apple";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_divide_string" %}

{% hint style="warning" %}
### Number haqida to'liq ma'lumotnoma

Number haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda number haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_number.asp)

Ma'lumotnomada barcha number xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
