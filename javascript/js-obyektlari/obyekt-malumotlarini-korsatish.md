# Obyekt ma'lumotlarini ko'rsatish

### JavaScript obyektlarini ekranda qanday ko'rsatiladi ?

JavaScript obyektini ko'rsatish \[object Object] ni ko'rsatadi.

```
const person = {
  name: "John",
  age: 30,
  city: "New York"
};

document.getElementById("demo").innerHTML = person;
```

Obyektlarni ekranda chiqarish uchun ba'zi umumiy yechimlar:

* Obyekt xususiyatlarini nomi bo'yicha ko'rsatish
* Obyekt xususiyatlarini tsiklda ko'rsatish
* Obyektni Object.values() yordamida ko'rsatish
* `JSON.stringify()` yordamida obyektni ko'rsatish

### Obyekt xususiyatlarini ekranga chiqarish

Obyekt xususiyatlari string sifatida ko'rsatilishi mumkin:

```
const person = {
  name: "John",
  age: 30,
  city: "New York"
};

document.getElementById("demo").innerHTML =
person.name + "," + person.age + "," + person.city;
```

### Obyektni tsiklda ko'rsatish

Obyektning xususiyatlari tsiklda to'planishi mumkin:

```
const person = {
  name: "John",
  age: 30,
  city: "New York"
};

let txt = "";
for (let x in person) {
txt += person[x] + " ";
};

document.getElementById("demo").innerHTML = txt;
```

Tskilda **person\[x]** dan foydalanishingiz kerak .

**person.x** ishlamaydi (chunki x o'zgaruvchi).

### Object.values() dan foydalanish

Har qanday obyekt `Object.values()` yordamida massivga aylantirilishi mumkin:

```
const person = {
  name: "John",
  age: 30,
  city: "New York"
};

const myArray = Object.values(person);
```

`myArray` hozir massiv holatida va u ekranga chiqarishga tayyor:

```
const person = {
  name: "John",
  age: 30,
  city: "New York"
};

const myArray = Object.values(person);
document.getElementById("demo").innerHTML = myArray;
```

`Object.values()` 2016 yildan beri barcha asosiy brauzerlarda qo'llab-quvvatlanadi.

| Chrome    | Edge      | Firefox   | Safari    | Opera     |
| --------- | --------- | --------- | --------- | --------- |
| 54 (2016) | 14 (2016) | 47 (2016) | 10 (2016) | 41 (2016) |

### JSON.stringify() dan foydalanish

Har qanday obekt `JSON.stringify()` funktsiyasi bilan stringga aylantirilishi mumkin:

```
const person = {
  name: "John",
  age: 30,
  city: "New York"
};

let myString = JSON.stringify(person);
```

`myString` hozir string holatida boʻlib, ekranga chiqarishga tayyor:

```
const person = {
  name: "John",
  age: 30,
  city: "New York"
};

let myString = JSON.stringify(person);
document.getElementById("demo").innerHTML = myString;
```

{% hint style="warning" %}
Natija JSON dan keyingi metod yordamida string bo'ladi:

{"name":"John","age":50,"city":"New York"}
{% endhint %}

`JSON.stringify()` JavaScript-ga kiritilgan va u barcha asosiy brauzerlarda qo'llab-quvvatlanadi.

### Stringga aylantirilgan sanalar

`JSON.stringify` sanalarni stringga aylantiradi:

```
const person = {
  name: "John",
  today: new Date()
};

let myString = JSON.stringify(person);
document.getElementById("demo").innerHTML = myString;
```

### Funktsiyalarda stringify

`JSON.stringify` funksiyalarni stringga aylantirmaydi:

```
const person = {
  name: "John",
  age: function () {return 30;}
};

let myString = JSON.stringify(person);
document.getElementById("demo").innerHTML = myString;
```

Agar siz stringifydan oldin funktsiyani stringga aylantirsangiz, buni "tuzatish" mumkin.

```
const person = {
  name: "John",
  age: function () {return 30;}
};
person.age = person.age.toString();

let myString = JSON.stringify(person);
document.getElementById("demo").innerHTML = myString;
```

### Massivlarda stringify

JavaScript massivlarini ham stringga aylantirish mumkin:

```
const arr = ["John", "Peter", "Sally", "Jane"];

let myString = JSON.stringify(arr);
document.getElementById("demo").innerHTML = myString;
```

{% hint style="warning" %}
Natija JSON belgisidan keyingi qator bo'ladi:

\["Jon", "Piter", "Sally", "Jeyn"]
{% endhint %}
