---
description: >-
  JavaScript-da faqat bitta turdagi raqam bor. Raqamlar o'nli kasrlar bilan yoki
  o'nlik kasrsiz yozilishi mumkin:
---

# Raqamlar



```javascript
let x = 3.14;    // A number with decimals
let y = 3;       // A number without decimals
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers1" %}

Haddan tashqari katta yoki haddan tashqari kichik raqamlar ilmiy belgilar bilan yozilishi mumkin:

```javascript
let x = 123e5;    // 12300000
let y = 123e-5;   // 0.00123
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers2" %}

### Javascriptda raqamlar har doim 64 bitli float hisoblanadi

Ko'pgina boshqa dasturlash tillaridan farqli o'laroq, JavaScriptda integer, short, long, float  va boshqa turli formatdagi raqamlar bo'lmaydi.

JavaScriptda raqamlar har doim xalqaro IEEE 754 standartiga muvofiq ikki tomonlama aniqlikdagi float raqam sifatida saqlanadi.\
\
Bu format raqamlarni 64 bitda saqlaydi, bunda raqam (kasr) 0 dan 51 gacha, eksponent 52 dan 62 gacha va belgilar 63 bitda saqlanadi:

| Qiymat (aka Fraction/Mantissa) | Ko'rsatkich      | Belgi      |
| ------------------------------ | ---------------- | ---------- |
| 52 bit (0 - 51)                | 11 bit (52 - 62) | 1 bit (63) |

### Butun sondagi aniqlik

Butun sonlar (nuqtasiz yoki eksponentsiz raqamlar) 15 tagacha aniq ko'rsatiladi.

```javascript
let x = 999999999999999;   // x 999999999999999 bo'ladi
let y = 9999999999999999;  // y 10000000000000000 bo'ladi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_inaccurate1" %}

O'nli kasrlarning maksimal uzunligi - 17.

### Floatdagi aniqlik

Float arifmetikasi har doim ham 100% aniq bo'lmaydi:

```javascript
let x = 0.2 + 0.1;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_inaccurate2" %}

Yuqoridagi muammoni hal qilish uchun u ko'paytiruv va bo'lish yordam beradi:

```javascript
let x = (0.2 * 10 + 0.1 * 10) / 10;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_inaccurate3" %}

### Raqamlar va stringlarni qo'shish

{% hint style="danger" %}
OGOHLANTIRISH!!

JavaScriptda qoʻshish va birlashtirish uchun + operatoridan foydalaniladi.

Raqamlar qo'shiladi. Stringlar birlashtiriladi.
{% endhint %}

Agar ikkita raqamni qo'shsangiz, natija raqam bo'ladi:

```javascript
let x = 10;
let y = 20;
let z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_add" %}

Agar ikkita stringni qo'shsangiz, natija string birikmasi bo'ladi:

```javascript
let x = "10";
let y = "20";
let z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_add_strings1" %}

Agar raqam va stringni qo'shsangiz, natija string birikmasi bo'ladi:

```javascript
let x = 10;
let y = "20";
let z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_add_strings2" %}

Agar string va raqamni qo'shsangiz ham natija string birikmasi bo'ladi:

```javascript
let x = "10";
let y = 20;
let z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_add_strings5" %}

Natija 30 bo'ladi deb o'ylash keng tarqalgan xato tushuncha hisoblanadi:

```javascript
let x = 10;
let y = 20;
let z = "The result is: " + x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_add_strings3" %}

Natijani 102030 deb o'ylash keng tarqalgan xato tushuncha hisoblanadi:

```javascript
let x = 10;
let y = 20;
let z = "30";
let result = x + y + z;    
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_add_strings4" %}

{% hint style="warning" %}
JavaScript interpreteri chapdan o'ngga qarab bajaradi.

Birinchi 10 + 20ni qo'shiladi, chunki x va y ning ikkalasi ham raqam.

Keyin 30 + "30" birlashtiriladi, chunki z o'zgaruvchisi string.
{% endhint %}

### Raqamli stringlar

JavaScript stringlari raqamli bo'lishi mumkin:

```javascript
let x = 100;         // x bu raqam

let y = "100";       // y bu string
```

JavaScript barcha raqamli arifmetik amallarda stringlarni raqamga aylantirishga harakat qiladi:

Bu ishlaydi:

```javascript
let x = "100";
let y = "10";
let z = x / y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_string1" %}

Bu ham ishlaydi:

```javascript
let x = "100";
let y = "10";
let z = x * y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_string2" %}

Va bu ham ishlaydi:

```javascript
let x = "100";
let y = "10";
let z = x - y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_string3" %}

Ammo bu ishlamaydi:

```javascript
let x = "100";
let y = "10";
let z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_string4" %}

Oxirgi misolda JavaScript stringlarni birlashtirish uchun + operatoridan foydalanadi.

### NaN - Not a Number (Raqam emas)

`NaN`bu raqam  haqiqiy raqam emasligini ko'rsatadigan JavaScriptga kiritilgan kalit so'zdir.

Raqam bo'lmagan string bilan arifmetik amal bajarishga harakat qilish natijasida `NaN` yuzaga keladi:

```javascript
let x = 100 / "Apple";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_divide_string" %}

Biroq, agar string raqamli bo'lsa, natija raqam bo'ladi:

```javascript
let x = 100 / "10";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_divide_number" %}

Qiymat raqam emasligini bilish uchun `isNaN()`  funksiyasidan foydalanishingiz mumkin:

```javascript
let x = 100 / "Apple";
isNaN(x);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_isnan_true" %}

Yodda tuting. Agar siz matematik amalda `NaN` dan foydalansangiz, natija ham `NaN` bo'ladi:

```javascript
let x = NaN;
let y = 5;
let z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_nan_math" %}

Yoki natija NaN5 kabi birikma ham bo'lishi mumkin:

```javascript
let x = NaN;
let y = "5";
let z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_nan_concat" %}

`NaN` bu raqam: `typeof NaN` `number` qaytaradi:

```javascript
typeof NaN;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_nan_typeof" %}

### Infinity

Agar eng katta raqamdanda katta raqamni hisoblasangiz, JavaScript `Infinity` (yoki `-Infinity`)  qaytariladi.

```javascript
let myNumber = 2;
// Execute until Infinity
while (myNumber != Infinity) {
  myNumber = myNumber * myNumber;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_infinity" %}

0 ga bo'linish  ham `Infinity` ni yuzaga keltiradi:

```javascript
let x =  2 / 0;
let y = -2 / 0;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_infinity_zero" %}

`Infinity` bu raqam: `typeof Infinity` `number` qaytaradi.

```javascript
typeof Infinity;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_infinity_typeof" %}

### Hexadecimal

Agar raqamli konstantalar oldida 0x bo'lsa, javascript ularni hexadecimal deb qabul qiladi.

```javascript
let x = 0xFF;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_hex" %}

{% hint style="warning" %}
Hech qachon raqamni 0 bilan boshlamang (masalan, 07).\
Ba'zi JavaScript versiyalarida, raqam 0 bilan boshlab yozilgan bo'lsa, raqamlarni sakkizlik sanoq sistemasida deb qabul qilinadi.
{% endhint %}

Defult tarzda, JavaScript raqamlarni **10 lik sanoq tizimidagi** kasr sifatida ko'rsatadi.

Lekin raqamlarni **2 lik sanoq tizimdan 36 lik sanoq tizimida**  ko'rsatish uchun `toString()` metodidan foydalanishingiz mumkin.

**Hexadecimal** - 16 lik sanoq tizimidir. **Decimal** - 10 lik sanoq tizimidir. **Octal** - 8 lik sanoq tizimidir. **Binary** - 2 lik sanoq tizmidir.

```javascript
let myNumber = 32;
myNumber.toString(32);
myNumber.toString(16);
myNumber.toString(12);
myNumber.toString(10);
myNumber.toString(8);
myNumber.toString(2);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_numbers_tostring" %}

### Raqamlarni obyekt sifatida e'lon qilsh

Odatda JavaScriptda raqamlar literallardan yaratilgan primitiv qiymat bo'ladi:

```javascript
let x = 123;
```

Ammo raqamlarni `new` kalit so'zi bilan obyekt sifatida ham e'lon qilish mumkin:

```javascript
let y = new Number(123);
```

```javascript
let x = 123;
let y = new Number(123);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_object" %}

{% hint style="warning" %}
Raqamli obyektlar yaratmang.

`new` kalit so'zi kodni murakkablashtiradi va bajarish tezligini sekinlashtiradi.

Raqamli obyektlar kutilmagan holatlarga olib kelishi mumkin:
{% endhint %}

`==` operatoridan foydalanganda x va y teng bo'ladi:

```javascript
let x = 500;
let y = new Number(500);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_object1" %}

`===` operatoridan foydalanganda x va y teng bo'lmaydi.

```javascript
let x = 500;
let y = new Number(500);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_object2" %}

`(x==y)` va  `(x===y)` o'rtasidagi farqga e'tibor bering.

`(x == y)` True-mi yoki false?

```javascript
let x = new Number(500);
let y = new Number(500);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_object3" %}

`(x === y)` True-mi yoki false?

```javascript
let x = new Number(500);
let y = new Number(500);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_number_object4" %}

{% hint style="warning" %}
Ikki obyektni taqqoslash har doim `false` qaytaradi.
{% endhint %}

{% hint style="warning" %}
### Number haqida to'liq ma'lumotnoma

Number haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda number haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_number.asp)

Ma'lumotnomada barcha number xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
