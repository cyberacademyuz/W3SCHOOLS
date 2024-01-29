# Ma'lumot turlari

{% hint style="success" %}
### Javasript 8 ta  ma'lumot turiga ega

1. String
2. Raqam
3. Bigint
4. Boolean
5. Undefuned
6. Null
7. Symbol
8. Object



### Obyekt ma'lumotlar turi

Obyekt ma'lumot turi quyidagilarni o'z ichiga olishi mumkin:

1. Obyekt
2. Massiv
3. Sana
{% endhint %}

```javascript
// Raqamlar:
let length = 16;
let weight = 7.5;

// Stringlar:
let color = "Yellow";
let lastName = "Johnson";

// Booleanlar
let x = true;
let y = false;

// Obyektlar:
const person = {firstName:"John", lastName:"Doe"};

// Massiv lar:
const cars = ["Saab", "Volvo", "BMW"];

// Date obyektlari:
const date = new Date("2022-03-25"); 
```

{% hint style="warning" %}
### Eslatma

JavaScriptda o'zgaruvchi har qanday turdagi ma'lumotlarni saqlashi mumkin.
{% endhint %}

### Ma'lumot turlari haqida tushuncha

Dasturlashda ma'lumot turlari muhim tushuncha hisoblanadi.

O'zgaruvchilar bilan ishlash uchun uning turi haqida bilish muhimdir.

Ma'lumot turlarisiz kompyuter uni to'g'ri bajara olmaydi:

```javascript
let x = 16 + "Volvo";
```

"**Volvo**" ni o'n oltiga qo'shishdan biror ma'no bormi ? Bunda xatolik yuzaga keladimi yoki to'g'ri ishlaydimi ?

JavaScript yuqoridagi misolni quyidagicha qabul qialadi:

```javascript
let x = "16" + "Volvo";
```

{% hint style="warning" %}
### Eslatma

Raqam va string qo'shilganda, JavaScript raqamni string sifatida ko'radi.
{% endhint %}

```javascript
let x = 16 + "Volvo";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_addstring" %}

```javascript
let x = "Volvo" + 16;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_addstring2" %}

JavaScript expressionlarni chapdan o'ngga qarab bajaradi. Turli xil ketma-ketliklar turlicha natija berishi mumkin:

{% code title="JavaScript:" %}
```javascript
let x = 16 + 4 + "Volvo";

// Natija
20Volvo
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_addstrings_1" %}

{% code title="JavaScript:" %}
```javascript
let x = "Volvo" + 16 + 4;

// Natija
Volvo164
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_addstrings_2" %}

Birinchi misolda JavaScript "Volvo" gacha 16 va 4 ni raqam sifatida ko'radi.

Ikkinchi misolda, birinchi operand string bo'lganligi sababli, barcha operandlar string sifatida ko'riladi.

### JavaScriptda typelar dinamikdir

JavaScript dinamik turlarga ega. Bu bir o'zgaruvchi turli xil ma'lumot turlarini saqlash uchun ishlatilishi mumkinligini anglatadi:

```javascript
let x;       // Hozir x undefined
x = 5;       // Hozir x raqam
x = "John";  // Hozir x string
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_dynamic" %}

### JavaScriptda stringlar

String "**Jon Doe**" kabi belgilar to'plamidir.

Stringlar tirnoqlar bilan yoziladi. Siz birtirnoq yoki qo'shtirnoqdan foydalanishingiz mumkin:

```javascript
// Qo'shtirnoqdan foydalanish:
let carName1 = "Volvo XC60";

// Birtirnoqdan foydalanish:
let carName2 = 'Volvo XC60';
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_string_quotes" %}

Agar ular stringni o'rashda ishlatilgan tirnoqlarga mos kelmasa, string ichida boshqa tirnoqlardan foydalanishingiz mumkin:

```javascript
// Qo'shtirnoq ichida bir tirnoqdan foydalanish:
let answer1 = "It's alright";

// Qo'shtirnoq ichida bir tirnoqdan foydalanish:
let answer2 = "He is called 'Johnny'";

// Birtirnoq ichida qo'shtirnoqdan foydalanish:
let answer3 = 'He is called "Johnny"';
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_string" %}

{% hint style="warning" %}
Keyinchalik [string](stringlar.md)lar haqida ko'proq bilib olasiz.
{% endhint %}

### JavaScript raqamlar

Javascriptda barcha raqamlar o'nlik sonlar sifatida saqlanadi.

Raqamlar o'nli kasrlar bilan yoki o'nlik kasrlarsiz yozilishi mumkin:

```javascript
// O'nlik kasr bilan:
let x1 = 34.00;

// On'lik kassiz:
let x2 = 34;
```

### Eksponensial belgi

Haddan tashqari katta yoki juda kichik raqamlar ilmiy belgilar bilan yozilishi mumkin:

```javascript
let y = 123e5;    // 12300000
let z = 123e-5;   // 0.00123
```

{% hint style="warning" %}
[Raqam](raqamlar.md)lar haqida keyinroq bilib olasiz.
{% endhint %}

{% hint style="warning" %}
### Eslatma

Ko'pgina dasturlash tillarida ko'plab raqam turlari mavjud:

Butun sonlar (integer-lar):\
byte (8-bit), short (16-bit), int (32-bit), long (64-bit)

Haqiqiy raqamlar (float):\
float (32-bit), double (64-bit).

Javascript har doim bir turdagi raqam mavjud:\
double (64-bit float)
{% endhint %}

### BigInt

JavaScriptda barcha raqamlar 64 bitli float formatida saqlanadi.

JavaScript BigInt - bu oddiy javascriptda Number bilan ifodalash uchun juda kattalik qiladigan butun son qiymatlarini saqlash uchun ishlatilishi mumkin bo'lgan yangi ma'lumotlar turi (2020).

```javascript
let x = BigInt("123456789012345678901234567890");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_bigint" %}

### Mantiqiy

Boolean qiymatlar faqat ikkita qiymatga ega bo'lishi mumkin: `true` yoki `false`.

```javascript
let x = 5;
let y = 5;
let z = 6;
(x == y)       // true qaytaradi
(x == z)       // false qaytaradi
```

Mantiqiy amallar ko'pincha shartni tekshirishda qo'llaniladi.

Shartni bajarish haqida keyinroq batafsil bilib oqlasiz.

### Massivlar

JavaScript massivlari kvadrat qavslar bilan yoziladi.

Massiv elementlari vergul bilan ajratiladi.

Quyidagi kod uchta elementni (avtomobil nomlarini) o'z ichiga olgan `cars` nomli massivni e'lon qiladi (yaratadi):

```javascript
const cars = ["Saab", "Volvo", "BMW"];
```

Massiv indekslari nolga asoslangan, ya'ni birinchi element \[0], ikkinchisi \[1] va hokazo.

{% hint style="warning" %}
[Arraylar](arraylar.md) haqida keyinroq bilib olasiz.
{% endhint %}

### JavaScript obyektlari

JavaScript obyektlari jingalak `{}` qavslar bilan yoziladi.

Obyekt xususiyatlari nom sifatida yoziladi: qiymat juftliklari vergul bilan ajratiladi.

```javascript
const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_object" %}

Yuqoridagi misoldagi obekt (person nomli) 4 ta xususiyatga ega: firstName, lastName, age, va eyeColor.

{% hint style="warning" %}
Obyektlar haqida keyinchalik batafsil bilib olasiz.
{% endhint %}

### typeof operatori

Javascriptda o'zgaruvchi turini aniqlash uchun `typeof` operatoridan foydalanishingiz mumkin.

`typeof` operatori o'zgaruvchi yoki expression turini qaytaradi:

```javascript
typeof ""             // "string" qaytaradi
typeof "John"         // "string" qaytaradi
typeof "John Doe"     // "string" qaytaradi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_typeof_string" %}

```javascript
typeof 0              // "number" qaytaradi
typeof 314            // "number" qaytaradi
typeof 3.14           // "number" qaytaradi
typeof (3)            // "number" qaytaradi
typeof (3 + 4)        // "number" qaytaradi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_typeof_number" %}

{% hint style="warning" %}
`typeof` haqida keyinchalik batafsil bilib olasiz.
{% endhint %}

### Undefined

JavaScript-da qiymatsiz o'zgaruvchi `undefined` qiymatiga ega bo'ladi. Uning turi ham `undefined` bo'ladi.

```javascript
let car;    // Qiymati undefined, turi undefined
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_undefined" %}

aQiymatni `undefined` qilish orqali har qanday o'zgaruvchini bo'shatish mumkin. Uning turi ham `undefined` bo'ladi.

```javascript
car = undefined;    // Qiymati undefined, turi undefined
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_undefined_2" %}

### Bo'sh qiymatlar

Bo'sh qiymatni `undefined` bilan hech qanday aloqasi yo'q.

Bo'sh string qiymatga ham ma'lumot turiga ham ega.

```javascript
let car = "";    // Qiymati "", turi "string"
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_datatypes_empty" %}
