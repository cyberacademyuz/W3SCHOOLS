# Obyekt xususiyatlari

Xususiyatlar har qanday obyektning eng muhim qismidir.

### Xususiyatlar

Xususiyatlar obyekt bilan bog'langan qiymatlardir.

Obyekt bu tartiblanmagan xususiyatlar to'plamidir.

Xususiyatlar odatda o'zgartirilishi, qo'shilishi va o'chirilishi mumkin, ammo ba'zilari faqat o'qilishi uchun bo'ladi.

### Xususiyatlarga murojaat qilish

Obyektning xususiyatiga murojaat qilish sintaksisi:

```
objectName.property      // person.age
```

yoki

```
objectName["property"]   // person["age"]
```

yoki

```
objectName[expression]   // x = "age"; person[x]
```

{% hint style="warning" %}
Expression xususiyat nomiga berilishi kerak.
{% endhint %}

#### 1-misol

```
person.firstname + " is " + person.age + " years old.";
```

#### 2-misol

```
person["firstname"] + " is " + person["age"] + " years old.";
```

### for... in tskili

`for...in` steytmenti obyektning xossalari bo'ylab harakatlanadi.

```
for (let variable in object) {
  // code to be executed
}
```

`for...in` tskili ichidagi kod blok har bir xususiyat uchun bir marta bajariladi.

Obyektning xususiyatlari bo'ylab harakatlanish:

```
const person = {
  fname:" John",
  lname:" Doe",
  age: 25
};

for (let x in person) {
  txt += person[x];
}
```

### Yangi xususiyatlar qo'shish

Siz shunchaki qiymat berish orqali mavjud obyektga yangi xususiyat qo'shishingiz mumkin.

Person obyekti allaqachon mavjud deb tasavvur qiling - va keyin unga yangi xususiyatlar berishingiz mumkin:

```
person.nationality = "English";
```

### Xususiyatlarni o'chirish

`delete` kalit so'zi obyektdan xususiyatni o'chiradi:

```
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};

delete person.age;

```

yoki `person["age"]`ni  o'chirish;

```
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};

delete person["age"];
```

`delete` kalit so'zi xususiyat qiymatini ham, xususiyatning o'zini ham o'chiradi.

O'chirilgandan keyin, xususiyatni yana qayta qo'shmasdan turib undan foydalanib bo'lmaydi.

`delete` operatori obyekt xususiyatlarida foydalanish uchun mo'ljallangan. Bu o'zgaruvchilar yoki funktsiyalarga ta'sir qilmaydi.

`delete` operatori JavaScriptning built-in obyekt xususiyatlarida ishlatilmasligi kerak. Bu dasturingizni buzishi mumkin.

### Built-in obyektlar

Obyektdagi qiymatlar boshqa yana bir obyekt bo'lishi ham mumkin:

```
myObj = {
  name:"John",
  age:30,
  cars: {
    car1:"Ford",
    car2:"BMW",
    car3:"Fiat"
  }
}
```

Nuqta yoki qavs yordamida ichki built-in obyektlarga murojaat qilishingiz mumkin:

```
myObj.cars.car2;
```

yoki:

```
myObj.cars["car2"];
```

yoki:

```
myObj["cars"]["car2"];
```

yoki:

```
let p1 = "cars";
let p2 = "car2";
myObj[p1][p2];
```

### Ichki massivlar va obyektlar

Obyektlardagi qiymatlar massivlar, massivlardagi qiymatlar esa obektlar bo'lishi mumkin:

```
const myObj = {
  name: "John",
  age: 30,
  cars: [
    {name:"Ford", models:["Fiesta", "Focus", "Mustang"]},
    {name:"BMW", models:["320", "X3", "X5"]},
    {name:"Fiat", models:["500", "Panda"]}
  ]
}
```

Massivlar ichidagi massivlarga murojaat qilish uchun har bir massiv uchun for-in tsiklidan foydalaning:

```
for (let i in myObj.cars) {
  x += "<h1>" + myObj.cars[i].name + "</h1>";
  for (let j in myObj.cars[i].models) {
    x += myObj.cars[i].models[j];
  }
}
```

### Xususiyat atributlari

Barcha xususiyatlarning o'z nomi bor. Bundan tashqari, ular ham qiymatga ega.

Qiymat xususiyatning atributlaridan biridir.

Boshqa atributlar: sanab o'tilishi, sozlanishi va yozilishi mumkin.

Ushbu atributlar xususiyatga qanday murojaat qilish mumkinligini belgilaydi (u o'qilishi mumkinmi?, yozilishi mumkinmi?)

JavaScript-da barcha atributlarni o'qish mumkin, lekin faqat qiymat atributini o'zgartirish mumkin (va faqat xususiyat yozish mumkin bo'lsagina).

(ECMAScript 5 da barcha xususiyat atributlarini olish va sozlash usullari mavjud)

### Prototip xususiyatlari

JavaScript obyektlari o'z prototipining xususiyatlarini meros qilib oladi.

`delete` kalit so'zi meros qilib olingan xususiyatlarni o'chirmaydi, lekin agar prototip xususiyatini o'chirsangiz, u prototipdan meros qolgan barcha obyektlarga ta'sir qiladi.
