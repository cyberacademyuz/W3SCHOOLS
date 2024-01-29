# Arraylar

{% hint style="success" %}
Massiv - bu bir nechta qiymatga ega bo'lishi mumkin bo'lgan maxsus o'zgaruvchi :

```javascript
const cars = ["Saab", "Volvo", "BMW"];
```

[Sinab ko'rish ](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_array)
{% endhint %}

## Nima uchun arraylardan foydalaniladi ?

Agar sizda elementlar ro'yxati (masalan, avtomobil nomlari ro'yxati) bo'lsa, mashinalarni bitta o'zgaruvchida saqlash quyidagicha bo'lishi mumkin:

```javascript
let car1 = "Saab";
let car2 = "Volvo";
let car3 = "BMW";
```

Biroq, agar mashinalar orasidan birortasini topmoqchi bo'lsangiz-chi ? Va agar sizda 3 ta emas, 300 ta mashina bo'lsa-chi ?

Buning yechimi - array!

Array bitta o'zgaruvchi nomi ostida ko'plab qiymatlarni saqlashi mumkin va siz index raqamiga murojaat qilish orqali qiymatlarga ham murojaat qilishingiz mumkin.

## Array yaratish

Array literalidan foydalanish array yaratishning eng oson usuli hisoblanadi.

{% code title="Sintaksis:" %}
```javascript
const array_name = [item1, item2, ...];
```
{% endcode %}

{% hint style="warning" %}
Arraylarni `const` kalit so'zi bilan e'lon qilish odatiy holga aylangan.

[JS Array Const](array-const.md) bo'limida arraykar bilan `const` dan foydalanish haqida ko'proq ma'lumot oling.
{% endhint %}

```javascript
const cars = ["Saab", "Volvo", "BMW"];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array" %}

Bo'sh joylar va qatorlarni ajratish muhim emas. Deklaratsiya bir nechta qatorlardan tashkil topishi mumkin:

```javascript
const cars = [
  "Saab",
  "Volvo",
  "BMW"
];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_newlines" %}

Bundan tashqari, avval array yaratib uning elementlarini keyinroq ham berishingiz mumkin:

```javascript
const cars = [];
cars[0]= "Saab";
cars[1]= "Volvo";
cars[2]= "BMW";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_add_elements" %}

## Javascriptning `new` kalit so'zidan foydalanish.

Quyidagi misolda ham, massiv yaratilgan va unga qiymatlar tayinlangan:

```javascript
const cars = new Array("Saab", "Volvo", "BMW");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_new" %}

{% hint style="warning" %}
Yuqoridagi ikkita misol bir xil vazifa bajaradi.

`new Array()` dan foydalanishga hojat yo'q.

Sodda, o'qilishi oson va tezroq ishlashi uchun arrayning literal usulidan foydalaning.
{% endhint %}

### Array elementlariga murojaat qilish

Siz index raqamiga murojaat qilish orqali array elementiga murojaat qilasiz:

```javascript
const cars = ["Saab", "Volvo", "BMW"];
let car = cars[0];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_element" %}

{% hint style="warning" %}
**Eslatma:** Array indexlari 0 dan boshlanadi.

\[0] birinchi element. \[1] ikkinchi element hisoblanadi.
{% endhint %}

### Array elementini o'zgartirish

Ushbu steytment `cars`ni birinchi elementining qiymatini o'zgartiradi:

```javascript
cars[0] = "Opel";
```

```javascript
const cars = ["Saab", "Volvo", "BMW"];
cars[0] = "Opel";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_element_change" %}

### Arrayni stringga o'tkazish

Javascriptining `toString()` metodi arrayning (vergul bilan ajratilgan) qiymatlarini stringga o'tkazadi.

{% hint style="info" %}
{% code title="Misol" %}
```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
```
{% endcode %}

{% code title="Natija:" %}
```
 Banana,Orange,Apple,Mango
```
{% endcode %}
{% endhint %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_tostring" %}

### Butun arrayga murojaat qilish

JavaScript yordamida toʻliq arrayga murojaat qilishni array nomiga murojaat qilish orqali amalga oshirish mumkin:

```javascript
const cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_full" %}

### Arraylar obyektlardir

Arraylar - bu obyektlarning maxsus turi. JavaScript-dagi `typeof` operatori massivlar uchun "obyekt" ni qaytaradi.

Biroq, JavaScript arraylari array sifatida juda yaxshi tasvirlangan.

Arraylarda uning "elementlariga" murojaat qilish uchun **raqamlardan foydalaniladi.** Ushbu misolda `person[0]` John qiymatini qaytaradi:

{% code title="Array:" %}
```javascript
const person = ["John", "Doe", 46];
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_array" %}

Obyektlar o'zining  "xususiyatlariga" ga murojaat qilish uchun **nomlardan** foydalanadilar. Ushbu misolda `person.firstName` John qiymatini qaytaradi:

```javascript
const person = {firstName:"John", lastName:"Doe", age:46};
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_object" %}

### Array elementlari obyektlar ham bo'lishi mumkin

JavaScript o'zgaruvchilarida obyektlar bo'lishi mumkin. Arraylar - bu maxsus turdagi obektlardir.

Shu sababli, siz bir arrayda har xil turdagi o'zgaruvchilarga ega bo'lishingiz mumkin.

Siz arrayda obyektlarga, funksiyalarga va arraylarga ega bo'lishingiz mumkin:

```javascript
myArray[0] = Date.now;
myArray[1] = myFunction;
myArray[2] = myCars;
```

### Array xususiyatlari  va metodlari

Arrayning haqiqiy kuchi uning xususiyatlari va metodlaridir:

```javascript
cars.length   // elementlarning sonini qaytaradi
cars.sort()   // Massivni tartiblaydi
```

Array metodlari keyingi bo'limda batafsil tushuntiriladi.

### Length xususiyati

Arrayning `length` xususiyati array uzunligini (array elementlarining sonini) qaytaradi.

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.length;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_length" %}

{% hint style="warning" %}
`length` xususiyati har doim arrayning eng katta indexidan bittaga ko'p bo'ladi.
{% endhint %}

### Arrayning birinchi elementiga murojaat qilish

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits[0];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_first" %}

### Arrayning oxirgi elementiga murojaat qilish

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits[fruits.length - 1];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_last" %}

### Array elementlarini loop qilish

Array bo'ylab aylanishning birgina yo'li - `for` tsikldan foydalanish:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fLen = fruits.length;

let text = "<ul>";
for (let i = 0; i < fLen; i++) {
  text += "<li>" + fruits[i] + "</li>";
}
text += "</ul>";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_loop" %}

`Array.forEach()` funksiyasidan ham foydalanishingiz mumkin:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];

let text = "<ul>";
fruits.forEach(myFunction);
text += "</ul>";

function myFunction(value) {
  text += "<li>" + value + "</li>";
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_loop_foreach" %}

### Array elementlarini qo'shish

Arrayga yangi element qo'shishning eng oson usuli bu `push()` metodidan foydalanishdir:

```javascript
const fruits = ["Banana", "Orange", "Apple"];
fruits.push("Lemon");  // fruits-ga yangi element (lemeon) qo'shadi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_add_push" %}

`length` xususiyati yordamida massivga yangi element ham qo'shilishi mumkin:

```javascript
const fruits = ["Banana", "Orange", "Apple"];
fruits[fruits.length] = "Lemon";  // fruits-ga "lemon"ni qo'sh
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_add" %}

{% hint style="danger" %}
**OGOHLANTIRISH!**

Array elementlarining sonidan katta index berish natijasida massivda `undefined` qiymatli "elementlar" yaratilishi mumkin:
{% endhint %}

```javascript
const fruits = ["Banana", "Orange", "Apple"];
fruits[6] = "Lemon";  // fruits-da undefined elementlar yaratadi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_holes" %}

### Assotsiativ massivlar

Ko'pgina dasturlash tillari index sifatida arrayning element nomini kiritish mumkin bo'lgan arraylarni qo'llab-quvvatlaydi.

Index sifatida arrayning element nomi kiritiladigan arraylar assotsiativ massivlar (yoki heshlar) deb ataladi.

JavaScript bunday arraylarni qo'llab-quvvatlamaydi**.**

JavaScript-da **array**lar har doim **raqamli indexlardan** foydalanadi. &#x20;

```javascript
const person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46;
person.length;    // 3 qaytaradi
person[0];        // "John" qaytaradi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_associative_1" %}

{% hint style="danger" %}
**OGOHLANTIRISH!!**

Agar siz index sifatida arrayning element nomidan foydalansangiz, JavaScript arrayni obyektga aylantirib beradi.

Keyin esa, ba'zi array metodlari va xususiyatlari noto'g'ri sihlaydi.
{% endhint %}

```javascript
const person = [];
person["firstName"] = "John";
person["lastName"] = "Doe";
person["age"] = 46;
person.length;     // 0 qaytaradi
person[0];         // undefined qaytaradi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_associative_2" %}

### Array va obyektlar o'rtasidagi farq

JavaScript-da **arraylar raqamli indexlardan** foydalanadi.

JavaScript-da **obyektlar nomga ega indekslardan** foydalanadi.

{% hint style="warning" %}
**Arraylar** - bu raqamli indexlarga ega bo'lgan maxsus turdagi obyektlardir.
{% endhint %}

### Qachon arraylardan va qachon obyektlardan foydalanish kerak ?

* JavaScript assotsiativ arraylarni qo'llab-quvvatlamaydi.
* Indexda element nomlari string bo'lishini xohlaganingizda **obyektlardan** foydalanishingiz kerak.
* Indexda element nomlari raqamlar bo'lishini istasangiz, **arraylardan** foydalanishingiz kerak.

### new Array()

JavaScript-da `new Array()`  array konstruktori mavjud.

Lekin uning o'rniga `[]`dan foydalanishingiz ham mumkin.

Ushbu ikki xil steytment yangi bo'm bo'sh array yaratadi:

```javascript
const points = new Array();
const points = [];
```

Ushbu ikki xil steytment 6 ta raqamdan iborat yangi array yaratadi:

```javascript
const points = new Array(40, 100, 1, 5, 25, 10);
const points = [40, 100, 1, 5, 25, 10];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_literal" %}

`new` kalit so'zi ba'zi kutilmagan natijalarga olib kelishi mumkin:

```javascript
const points = new Array(40, 100, 1); // 3 ta elementli array yaratish:
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_new_array_three" %}

```javascript
const points = new Array(40, 100); // 2 ta elementli array yaratish:
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_new_array_two" %}

```javascript
const points = new Array(40); // 1 ta elementli array yaratish:
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_new_error" %}

{% code title="Ko'p kuzatiladigan xato:" %}
```javascript
const points = [40];
va
const points = new Array(40);
bir xil emas
```
{% endcode %}

```javascript
// Bir elementli array yaratadi:
const points = [40];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_one" %}

```javascript
// 40 ta undefined elementdan iborat array yaratadi:
const points = new Array(40);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_new_error2" %}

### Arrayni qanday tanib olish mumkin

Ko'p takrorlanuvchi savol: o'zgaruvchining array ekanligini qanday bilsam bo'ladi ?

Muammo shundaki, JavaScriptning `typeof` operatori  "`object`" qaytaradi:

```javascript
const fruits = ["Banana", "Orange", "Apple"];
let type = typeof fruits;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_typeof" %}

JavaScriptda array obyekt hisoblangani sabab `typeof` operatori `object` qaytaradi.

#### 1-yechim:

Ushbu muammoni hal qilish uchun ECMAScript 5 yangi `Array.isArray()` metodini kiritdi:

```javascript
Array.isArray(fruits);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_isarray_method" %}

#### 2-yechim:

Agar obyekt berilgan konstruktor tomonidan yaratilgan bo'lsa, `instanceof` operatori `true` qiymatini qaytaradi:

```javascript
const fruits = ["Banana", "Orange", "Apple"];
fruits instanceof Array;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_instanceof" %}

{% hint style="warning" %}
### Array haqida to'liq ma'lumotnoma

Array haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda array haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_array.asp)

Ma'lumotnomada arrayning barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
