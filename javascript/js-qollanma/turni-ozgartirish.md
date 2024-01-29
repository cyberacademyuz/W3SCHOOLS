# Turni o'zgartirish

{% hint style="success" %}
* Stringlarni raqamlarga aylantirish
* Raqamlarni stringlarga aylantirish
* Sanalarni raqamlarga aylantirish
* Raqamlarni sanaga aylantirish
* Booleanlarni raqamlarga aylantirish
* Raqamlarni booleanlarga aylantirish
{% endhint %}

### JavaScriptda turni konvertatsiya qilish

Ozgaruvchilar yangi o'zgaruvchiga va boshqa ma'lumot turiga aylantirilishi mumkin:

* Funksiyasidan foydalanish orqali
* JavaScript-ning o'zi tomonidan **avtomatik** ravishda

### Stringlarni raqamga aylantirish

Global  `Number()` metodi o'zgaruvchini (yoki qiymatni) raqamga aylantiradi.

Raqamli string (masalan, "3.14") raqamga aylanadi (masalan, 3.14).

Bo'sh satr (masalan, "") 0 ga aylanadi.

Raqamli bo'lmagan string (masalan, "Jon") `NaN` (Raqam emas) ga aylanadi.

{% code title="Bular number turiga aylanadi:" %}
```
Number("3.14")
Number(Math.PI)
Number(" ")
Number("")
```
{% endcode %}

{% code title="Bular number turiga aylanmaydi:" %}
```
Number("99 88")
Number("John")
```
{% endcode %}

### Number metodlari

[Raqam metodlari](raqam-metodlari.md) bo'limida stringlarni raqamga aylantirish uchun ishlatilishi mumkin bo'lgan boshqa metodlarni topasiz:

| Methd        | Ta'rif                                           |
| ------------ | ------------------------------------------------ |
| Number()     | Argumentidan aylantirilgan raqamni qaytaradi     |
| parseFloat() | Stringni parse qiladi va float raqamni qaytaradi |
| parseInt()   | Stringni parse qiladi va integer raqam qaytaradi |

### Unary + Operator

O'zgaruvchini raqamga aylantirish uchun unary + operatoridan foydalanish mumkin **:**

```
let y = "5";      // y is a string
let x = + y;      // x is a number
```

Agar o'zgaruvchini konvertatsiya qilib bo'lmasa, u baribir raqamga aylanadi, lekin `NaN`(Raqam emas) qiymati sifatida:

```
let y = "John";   // y is a string
let x = + y;      // x is a number (NaN)
```

### Raqamlarni stringga aylantirish

Global `String()` metodi raqamlarni stringga aylantirishi mumkin.

U har qanday turdagi raqamlar, harflar, o'zgaruvchilar yoki expressionlarda ishlatilishi mumkin:

```
String(x)         // returns a string from a number variable x
String(123)       // returns a string from a number literal 123
String(100 + 23)  // returns a string from a number from an expression
```

Raqam metodi `toString()`  ham xuddi shunday sihlaydi.

```
x.toString()
(123).toString()
(100 + 23).toString()
```

### Ko'proq metodlar

[Raqam metodlari](raqam-metodlari.md) bo'limida raqamlarni stringga aylantirish uchun ishlatilish mumkin bo'lgan boshqa metodlarni ham topasiz:

| Metod           | Ta'rif                                                          |
| --------------- | --------------------------------------------------------------- |
| toExponential() | Yaxlitlangan va ilmiy belgilar bilan yozilgan string qaytaradi. |
| toFixed()       | Yaxlitlangan va o'nli kasrlar bilan yozilgan  string qaytaradi  |
| toPrecision()   | Belgilangan uzunlik bilan yozilgan raqam vastring qaytaradi     |

### Sanalarni raqamlarga aylantirish

Sanalarni raqamlarga aylantirish uchun global `Number()` metodidan foydalanish mumkin.

```
d = new Date();
Number(d)          // returns 1404568027739
```

Date metodi  `getTime()` xam xuddi shunday ishlaydi.

```
d = new Date();
d.getTime()        // returns 1404568027739
```

### Sanalarni stringga aylantirish

Global `String()` metodi sanalarni stringga aylantirishi mumkin.

```
String(Date())  // returns "Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)"
```

Date metodi `toString()` ham xuddi shunday qiladi.

```
Date().toString()  // returns "Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)"
```

[Date metodlari](sana-get-metodi.md) bo'limida sanalarni stringga aylantirish uchun ishlatilishi mumkin bo'lgan boshqa metodlarni topasiz:

| Metod             | Ta'rif                                                              |
| ----------------- | ------------------------------------------------------------------- |
| getFullYear()     | Yilni to'rt xonali raqam sifatida oling (yyyy)                      |
| getMonth()        | Oyni raqam sifatida oling (0-11)                                    |
| getDate()         | Kunni raqam sifatida oling (1-31)                                   |
| getDay()          | Hafta kunini raqam sifatida oling (0-6)                             |
| getHours()        | Soatni oling (0-23)                                                 |
| getMinutes()      | Daqiqa olish (0-59)                                                 |
| getSeconds()      | Soniyani oling (0-59)                                               |
| getMilliseconds() | Millisekundni oling (0-999)                                         |
| getTime()         | Vaqtni oling (1970 yil 1 yanvardan boshlab millisekundlar hisobida) |

### Booleanlarni raqamlarga aylantirish

Global `Number()` metodi, boolean qiymatlarni raqamga aylantirishi mumkin.

```
Number(false)     // returns 0
Number(true)      // returns 1
```

### Booleanlarni stringga aylantirish

Global `String()` metodi booleanlarni stringga aylantirishi mumkin.

```
String(false)      // returns "false"
String(true)       // returns "true"
```

Boolean metodi `toString()` ham xuddi shunday qiladi.

```
false.toString()   // returns "false"
true.toString()    // returns "true"
```

### Avtomatik turdagi konvertatsiya

JavaScript "noto'g'ri" ma'lumot turida ishlashga harakat qilganda, u qiymatni "to'g'ri" turga aylantirishga harakat qiladi.

Natija har doim ham siz kutgandek bo'lmaydi:

```
5 + null    // returns 5         because null is converted to 0
"5" + null  // returns "5null"   because null is converted to "null"
"5" + 2     // returns "52"      because 2 is converted to "2"
"5" - 2     // returns 3         because "5" is converted to 5
"5" * "2"   // returns 10        because "5" and "2" are converted to 5 and 2
```

### Stringga avtomatik konvertatsiya

Obekt yoki o'zgaruvchini "chiqarish"ga harakat qilganingizda JavaScript avtomatik ravishda o'zgaruvchining `toString()` funksiyasini chaqiradi:

```
document.getElementById("demo").innerHTML = myVar;

// if myVar = {name:"Fjohn"}  // toString converts to "[object Object]"
// if myVar = [1,2,3,4]       // toString converts to "1,2,3,4"
// if myVar = new Date()      // toString converts to "Fri Jul 18 2014 09:08:55 GMT+0200"
```

Raqamlar va boolean qiymatlar ham o'zgartiriladi, ammo bu unchalik ko'rinmaydi:

```
// if myVar = 123             // toString converts to "123"
// if myVar = true            // toString converts to "true"
// if myVar = false           // toString converts to "false"
```

### Typeni konvertatsiyalash jadvali

Ushbu jadval turli xil qiymatlarni Number, String va Booleanga aylantirish natijasini ko'rsatadi:

| Asl qiymat        | Raqamga aylantirilgan: | Stringga aylantirilgan: | Booleanga aylantirilgan |   |
| ----------------- | ---------------------- | ----------------------- | ----------------------- | - |
| false             | 0                      | "false"                 | false                   |   |
| true              | 1                      | "true"                  | true                    |   |
| 0                 | 0                      | "0"                     | false                   |   |
| 1                 | 1                      | "1"                     | true                    |   |
| "0"               | 0                      | "0"                     | true                    |   |
| "000"             | 0                      | "000"                   | true                    |   |
| "1"               | 1                      | "1"                     | true                    |   |
| NaN               | NaN                    | "NaN"                   | false                   |   |
| Infinity          | Infinity               | "Infinity"              | true                    |   |
| -Infinity         | -Infinity              | "-Infinity"             | true                    |   |
| ""                | 0                      | ""                      | false                   |   |
| "20"              | 20                     | "20"                    | true                    |   |
| "twenty"          | NaN                    | "twenty"                | true                    |   |
| \[ ]              | 0                      | ""                      | true                    |   |
| \[20]             | 20                     | "20"                    | true                    |   |
| \[10,20]          | NaN                    | "10,20"                 | true                    |   |
| \["twenty"]       | NaN                    | "twenty"                | true                    |   |
| \["ten","twenty"] | NaN                    | "ten,twenty"            | true                    |   |
| function(){}      | NaN                    | "function(){}"          | true                    |   |
| { }               | NaN                    | "\[object Object]"      | true                    |   |
| null              | 0                      | "null"                  | false                   |   |
| undefined         | NaN                    | "undefined"             | false                   |   |

Qo'shtirnoq ichidagi qiymatlar string qiymatini bildiradi.

Qizil qiymatlar qiymatlarni bildiradi (ba'zi) dasturchilar kutmasligi mumkin.
