# Array Const

### ECMAScript 2015 (ES6)

2015 yilda JavaScript muhim yangi `const` kalit so'zini taqdim qildi.

`const` dan foydalanib massiv e'lon qilish odatiy holga aylandi :

```
const cars = ["Saab", "Volvo", "BMW"];
```

### Qayta tayinlab bo'lmaydi

`const` bilan e'lon qilingan massivni qayta tayinlab bo'lmaydi:

```
const cars = ["Saab", "Volvo", "BMW"];
cars = ["Toyota", "Volvo", "Audi"];    // ERROR
```

### Massivlar konstanta emas

`const` kalit so'zi sizni biroz chalgishi mumkin

U o'zgarmas massivni e'lon qilmaydi. U massivga o'zgarmas nom beradi.

Shu sababli, biz o'zgarmas massivning elementlarini o'zgartirishimiz mumkin.

### Elementlarni qayta tayinlash mumkin

O'zgarmas massivning elementlarini o'zgartirishingiz mumkin:

```
// You can create a constant array:
const cars = ["Saab", "Volvo", "BMW"];

// You can change an element:
cars[0] = "Toyota";

// You can add an element:
cars.push("Audi");
```

### Brauzerning qo'llab-quvvatlashi

`const` kalit so'zi Internet Explorer 10 yoki undan oldingi versiyalarda ishlamaydi.

Quyidagi jadvalda `const` kalit so'zini to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyalarini belgilaydi:

| Chrome    | Internet Explrer | Firefox    | Safari    |           |
| --------- | ---------------- | ---------- | --------- | --------- |
| Chrome 49 | IE 11 / Edge     | Firefox 36 | Safari 10 | Opera 36  |
| Mar, 2016 | Oct, 2013        | Feb, 2015  | Sep, 2016 | Mar, 2016 |

### E'lon qilinganadayoq tayinlanadi

JavaScriptda `const` o'zgaruvchilari e'lon qilinganda ularga qiymat berilishi kerak:

Bu degani: `const` bilan e'lon qilingan massiv e'lon qilinganda ishga tushirilishi kerak.

Massivni ishga tushirmasdan `const`dan foydalanish sintaktik xatoga olib keladi:

{% code title="Bu ishlamaydi:" %}
```
const cars;
cars = ["Saab", "Volvo", "BMW"];
```
{% endcode %}

`var` bilan e'lon qilingan massivlar istalgan vaqtda ishga tushirilishi mumkin.

Siz hatto massivni e'lon qilinishdan oldin ham ishlatishingiz mumkin:

{% code title="Bu ishlaydi:" %}
```
cars = ["Saab", "Volvo", "BMW"];
var cars;
```
{% endcode %}

### Const Blok scope

`const` bilan e'lon qilingan massiv Block scopega ega.

Blok ichida e'lon qilingan massiv blokdan tashqarida e'lon qilingan massiv bilan bir xil emas:

```
const cars = ["Saab", "Volvo", "BMW"];
// Here cars[0] is "Saab"
{
  const cars = ["Toyota", "Volvo", "BMW"];
  // Here cars[0] is "Toyota"
}
// Here cars[0] is "Saab"
```

`var` bilan e'lon qilingan massiv block scopega ega emas:

```
var cars = ["Saab", "Volvo", "BMW"];
// Here cars[0] is "Saab"
{
  var cars = ["Toyota", "Volvo", "BMW"];
  // Here cars[0] is "Toyota"
}
// Here cars[0] is "Toyota"
```

Block Scop haqida ko'proq ma'lumotlarni, [JavaScript scope](https://www.w3schools.com/js/js\_scope.asp) bo'limidan olishingi mumkin.

### Massivlarni qayta e'lon qilish

JavaScript `var` bilan e'lon qilingan  massivni  dasturning istalgan joyida qayta e'lon qilishga ruxsat beriladi:

```
var cars = ["Volvo", "BMW"];   // Allowed
var cars = ["Toyota", "BMW"];  // Allowed
cars = ["Volvo", "Saab"];      // Allowed
```

Massivni bir scopeda yoki bir block ichida `const`ga qayta e'lon qilish yoki qayta tayinlash mumkin emas:

```
var cars = ["Volvo", "BMW"];     // Allowed
const cars = ["Volvo", "BMW"];   // Not allowed
{
  var cars = ["Volvo", "BMW"];   // Allowed
  const cars = ["Volvo", "BMW"]; // Not allowed
}
```

`const` bilan e'lon qilingan mavjud  massivni bir scopeda yoki bir block ichida `const`ga qayta e'lon qilish yoki qayta tayinlash mumkin emas:

```
const cars = ["Volvo", "BMW"];   // Allowed
const cars = ["Volvo", "BMW"];   // Not allowed
var cars = ["Volvo", "BMW"];     // Not allowed
cars = ["Volvo", "BMW"];         // Not allowed

{
  const cars = ["Volvo", "BMW"]; // Allowed
  const cars = ["Volvo", "BMW"]; // Not allowed
  var cars = ["Volvo", "BMW"];   // Not allowed
  cars = ["Volvo", "BMW"];       // Not allowed
}
```

Massivni `const` bilan boshqa scopeda yoki boshqa blokda qayta e'lon qilishga ruxsat beriladi:

```
const cars = ["Volvo", "BMW"];   // Allowed
{
  const cars = ["Volvo", "BMW"]; // Allowed
}
{
  const cars = ["Volvo", "BMW"]; // Allowed
}
```

{% hint style="warning" %}
### Massiv haqida to'liq ma'lumotnoma

Massiv haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda massiv haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_array.asp)

Ma'lumotnomada massivning barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
