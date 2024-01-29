# Array iteratorlar

Arrayning iterator metodlari har bir array elementida ishlaydi.

### Arrayda forEach()

`forEach()` metodi har bir array elementi uchun bir marta funksiyani chaqiradi.

```javascript
const numbers = [45, 4, 9, 16, 25];
let txt = "";
numbers.forEach(myFunction);

function myFunction(value, index, array) {
  txt += value + "<br>";
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_foreach" %}

E'tibor bering, funksiya 3 ta argument oladi:

* Element qiymati
* Element indeksi
* Massivning o'zi

Yuqoridagi misol faqat value parametridan foydalanadi. Misolni quyidagidek yozish ham mumkin:

```javascript
const numbers = [45, 4, 9, 16, 25];
let txt = "";
numbers.forEach(myFunction);

function myFunction(value) {
  txt += value + "<br>";
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_foreach" %}

### Massiv map()

`map()` metodi har bir array elementida funksiyani bajarish orqali yangi massiv yaratadi.

`map()` metodi array elementlari uchun funksiyani qiymatsiz ishga tushirmaydi.

`map()` metodi asl stringni o'zgartirmaydi.

Ushbu misolda har bir array qiymatini 2 ga ko'paytirish ko'rsatilgan.

```javascript
const numbers1 = [45, 4, 9, 16, 25];
const numbers2 = numbers1.map(myFunction);

function myFunction(value, index, array) {
  return value * 2;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_foreach" %}

E'tibor bering, funksiya 3 ta argument oladi:

* Element qiymati
* Element indeksi
* Massivning o'zi

Callback funksiyasi faqat value parametridan foydalansa, index va array parametrlarini kiritmasa ham bo'ladi:

```javascript
const numbers1 = [45, 4, 9, 16, 25];
const numbers2 = numbers1.map(myFunction);

function myFunction(value) {
  return value * 2;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_foreach_2" %}

### Massivda flatMap()

ES2019da Javascriptga `flatMap()` metodi qo'shildi

`flatMap()` metodi birinchi array elementlarini map qilib oladi va keyin arrayni tekislash orqali yangi massiv yaratadi.

```javascript
const myArr = [1, 2, 3, 4, 5, 6];
const newArr = myArr.flatMap((x) => x * 2);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_flatmap" %}

### Brauzer qo'llab quvvatlashi

`flatMap()` 2020 yil Yanvardan boshlab barcha zamonaviy brauzerlarda qo'llab quvvatlanadi.

| Chrome 69 | Edge 79  | Firefox 62 | Safari 12 | Opera 56 |
| --------- | -------- | ---------- | --------- | -------- |
| Sep 2018  | Jan 2020 | Sep 2018   | Sep 2018  | Sep 2018 |

### Massivda filter()

`filter()` metodi sinovdan o'tgan array elementlariga ega yangi array yaratadi.

Ushbu misolda qiymati 18 dan katta bo'lgan elementlardan yangi array yaratish ko'rsatilgan:

```javascript
const numbers = [45, 4, 9, 16, 25];
const over18 = numbers.filter(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_filter" %}

E'tibor bering, funksiya 3 ta argument oladi:

* Element qiymati
* Element indexi
* Massivning o'zi

Callback funksiya faqat value parametridan foydalansa, index va array parametrlarini kiritmasa ham bo'ladi:

```javascript
const numbers = [45, 4, 9, 16, 25];
const over18 = numbers.filter(myFunction);

function myFunction(value) {
  return value > 18;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_filter_2" %}

### Array reduce()

`reduce()` metodi har bir array elementida bitta qiymat kamaytirib chiqarish uchun funksiyani ishga tushiradi.

`reduce()` metodi massivda chapdan o'ngga qarab ishlaydi. Bundan tashqari  `reduceRight()`ga e'tibor qiling.

{% hint style="warning" %}
`reduce()` metodi asl stringni kamaytirmaydi.
{% endhint %}

Ushbu misolda massivdagi barcha raqamlarning yig'indisini topish ko'rsatilgan:

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduce(myFunction);

function myFunction(total, value, index, array) {
  return total + value;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_reduce" %}

E'tibor bering, funksiya 4 ta argument oladi:

* Jami (boshlang'ich qiymat / avvalgi qaytarilgan qiymat)
* Element qiymati
* Element indexi
* Massivning o'zi

Yuqoridagi misolda index va array parametlaridan foydalanilmagan. Misolni quyidagidek yozish ham mumkin:

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduce(myFunction);

function myFunction(total, value) {
  return total + value;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_reduce_2" %}

`reduce()` metodi boshlang'ich qiymatni qabul qilishi mumkin:

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduce(myFunction, 100);

function myFunction(total, value) {
  return total + value;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_reduce_initial" %}

### Array reduceRight()

`reduceRight()` metodi har bir array elementida bitta qiymat kamaytirish uchun funksiyani ishga tushiradi.

`reduceRight()` arrayda o'ngdan chapga qarab ishlaydi.

{% hint style="warning" %}
`reduceRight()` metodi asl stringni kamaytirmaydi.
{% endhint %}

Ushbu misol arraydagi barcha raqamlarning yig'indisini topadi:

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduceRight(myFunction);

function myFunction(total, value, index, array) {
  return total + value;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_reduce_right" %}

E'tibor bering, funksiya 4 ta argument oladi:

* Jami (boshlang'ich qiymat / avvalgi qaytarilgan qiymat)
* Element qiymati
* Element indeksi
* Massivning o'zi

Yuqoridagi misolda index va array parametlaridan foydalanilmagan. Misolni quyidagidek yozish ham mumkin:

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduceRight(myFunction);

function myFunction(total, value) {
  return total + value;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_reduce_right_2" %}

### Array every()

`every()` metodi barcha array qiymatlari sinovdan o'tganligini tekshiradi.

Ushbu misol barcha massiv qiymatlari 18 dan katta ekanligini tekshiradi:

```javascript
const numbers = [45, 4, 9, 16, 25];
let allOver18 = numbers.every(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_every" %}

E'tibor bering, funksiya 3 ta argument oladi:

* Element qiymati
* Element indeksi
* Massivning o'zi

Callback funksiyasi faqat birinchi parametrdan foydalanilganda, boshqa parametrlarni o'tkazib yuborish mumkin:

```javascript
const numbers = [45, 4, 9, 16, 25];
let allOver18 = numbers.every(myFunction);

function myFunction(value) {
  return value > 18;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_every_2" %}

### Massiv some()

`some()` metodi ba'zi massiv qiymatlari sinovdan o'tganligini tekshiradi.

Ushbu misol array qiymatlarining 18 dan kattaligini tekshiradi:

```javascript
const numbers = [45, 4, 9, 16, 25];
let someOver18 = numbers.some(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_some" %}

E'tibor bering, funktsiya 3 ta argument oladi:

* Element qiymati
* Element indeksi
* Massivning o'zi

### Massiv  indexOf()

`indexOf()` metodi arrayda element qiymatini qidiradi va uning joylashuvini qaytaradi.

{% hint style="warning" %}
**Eslatma:** Birinchi element 0 indexga ega, ikkinchi element 1 indexga ega va hokazo.
{% endhint %}

{% code title=""Apple" elementining massivini qidiring:" %}
```javascript
const fruits = ["Apple", "Orange", "Apple", "Mango"];
let position = fruits.indexOf("Apple") + 1;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_indexof" %}

#### Sintaksis

```javascript
array.indexOf(item, start)
```

| _item_  | Majburiy. Elementni qidirsh uchun                                                                                                                |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| _start_ | Ixtiyoriy. Qidiruvni qayerdan boshlash kerak. Manfiy qiymatlar oxiridan boshlab sanab berilgan pozitsiyadan boshlanadi va oxirigacha qidiriladi. |

Agar element topilmasa `Array.indexOf()` -1 qaytaradi.

Agar obyekt bir necha marta mavjud bo'lsa, u birinchi topilgan joyni qaytaradi.

### Array lastIndexOf()

`Array.lastIndexOf()` `Array.indexOf()` bilan bir xil, lekin belgilangan elementning oxirgi aniqlangan joyini  const fruits = \["Apple", "Orange", "Apple", "Mango"];

{% code title=""Apple" elementining massivini qidiring:" %}
```javascript
let position = fruits.lastIndexOf("Apple") + 1;
```
{% endcode %}

#### Sintaksis

```javascript
array.lastIndexOf(item, start)
```

| _item_  | Required. The item to search for                                                                                                         |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| _start_ | Optional. Where to start the search. Negative values will start at the given position counting from the end, and search to the beginning |

### Massiv find()

`find()` metodi tekshiruv funksiyasidan o'tgan birinchi array elementining qiymatini qaytaradi.

Ushbu misolda 18 dan katta bo'lgan birinchi elementni topish ko'rsatilgan:

```javascript
const numbers = [4, 9, 16, 25, 29];
let first = numbers.find(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

E'tibor bering, funksiya 3 ta argument oladi:

* Element qiymati
* Element indeksi
* Massivning o'zi

### Brauzerning qo'llab-quvvatlashi

`find()` ES6ning xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`find()` Internet Explorer-da qo'llab-quvvatlanmaydi.

### Massiv findIndex()

`findIndex()` metodi test funktsiyasidan o'tgan birinchi massiv elementining indeksini qaytaradi.

Ushbu misol 18 dan katta bo'lgan birinchi elementning indeksini topadi:

```javascript
const numbers = [4, 9, 16, 25, 29];
let first = numbers.findIndex(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

E'tibor bering, funksiya 3 ta argument oladi:

* Element qiymati
* Element indeksi
* Massivning o'zi

### Brauzerning qo'llab-quvvatlashi

`findIndex()` ES6ning xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge  | Firefox | Safari |       |
| ------ | ----- | ------- | ------ | ----- |
| Chrome | Edge  | Firefox | Safari | Opera |
| Yes    | Yes   | Yes     | Yes    | Yes   |

`findIndex()` Internet Explorer-da qo'llab-quvvatlanmaydi.

### Array.from()

`Array.from()` metodi length xususiyatiga ega har qanday obektdan yoki har qanday takrorlanadigan obektdan Array obektini qaytaradi.

{% code title="Stringdan massiv yarating:" %}
```javascript
Array.from("ABCDEFG");
```
{% endcode %}

### Brauzerning qo'llab-quvvatlashi

`from()` ES6ning xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`from()` Internet Explorer-da qo'llab-quvvatlanmaydi.

### Array.keys()

`Array.keys()` metodi massiv kalitlari bilan Array Iterator obyektini qaytaradi.

{% code title="Massiv kalitlarini o'z ichiga olgan Array Iterator obyektini yarating:" %}
```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const keys = fruits.keys();

for (let x of keys) {
  text += x + "<br>";
}
```
{% endcode %}

### Brauzerning qo'llab-quvvatlashi

`keys()` ES6 xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`keys()` Internet Explorer-da qo'llab-quvvatlanmaydi.

### Massiv entries()

{% code title="Massiv iteratorini yarating va keyin kalit/qiymat juftliklarini takrorlang:" %}
```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const f = fruits.entries();

for (let x of f) {
  document.getElementById("demo").innerHTML += x;
}
```
{% endcode %}

`entries()` metodi kalit/qiymat juftligi bilan Iterator obyektini qaytaradi:

\[0, "Banan"]\
\[1, "Apelsin"]\
\[2, "Olma"]\
\[3, "Mango"]

`entries()` metodi asl stringni o'zgartirmaydi.

### Brauzerning qo'llab-quvvatlashi

`entries()` ES6 xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`entries()` Internet Explorer-da qo'llab-quvvatlanmaydi.

### Massiv includes()

ECMAScript 2016 massivlarga `Array.includes()`ni taqdim qildi. Bu massivda element mavjudligini tekshirish imkonini beradi (indexOf dan farqli o'laroq, NaN ham kiradi).

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];

fruits.includes("Mango"); // is true
```

#### Sintaksis

```javascript
array.includes(search-item)
```

{% hint style="warning" %}
Array.includes()  Array.indexOf() dan farqli o'laroq NaN qiymatlarini ham tekshirish imkonini beradi.
{% endhint %}

### Brauzerning qo'llab-quvvatlashi

`includes()` ECMAScript 2016 xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`includes()` Internet Explorer-da qo'llab-quvvatlanmaydi.

### Spread (...)

... operatori takrorlanadigan ko'proq elementlarga kengaytiradi:

```javascript
const q1 = ["Jan", "Feb", "Mar"];
const q2 = ["Apr", "May", "Jun"];
const q3 = ["Jul", "Aug", "Sep"];
const q4 = ["Oct", "Nov", "May"];

const year = [...q1, ...q2, ...q3, ...q4];
```

### Brauzerning qo'llab-quvvatlashi

`...` ES6ning xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`...` Internet Explorer-da qo'llab-quvvatlanmaydi.

{% hint style="warning" %}
### Massiv haqida to'liq ma'lumotnoma

Massiv haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda massiv haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_array.asp)

Ma'lumotnomada massivning barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
