# Classlar

{% hint style="success" %}
ES6 JavaScriptda classlarni taqdim qildi.

Classlar JavaScript obyektlari uchun shablon hisoblanadi.
{% endhint %}

## JavaScriptning class sintaksisi

Class yaratish uchun `class` kalit so'zidan foydalaning.

Har doim `constructor()` nomli metodni qo'shing:

{% code title="Sintaksis:" %}
```
class ClassName {
  constructor() { ... }
}
```
{% endcode %}

```
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
}
```

Yuqoridagi misol "Car" nomli Class yaratadi.

Class ikkita xususiyatga ega: "name" va "year".

{% hint style="warning" %}
JavaScript classi obyekt emas.

Bu obyektlar uchun shablon hisoblanadi.
{% endhint %}

### Classdan foydalanish

Agar sizda class mavjud bo'lsa, obyektlarni yaratish uchun class foydalanishingiz mumkin:

```
let myCar1 = new Car("Ford", 2014);
let myCar2 = new Car("Audi", 2019);
```

Yuqoridagi misol 2ta Car obyektlarini yaratish uchun Car classidan foydalanadi.

{% hint style="warning" %}
Yangi obyekt yaratilganida constructor metodi avtomatik tarzda chaqiriladi.
{% endhint %}

### Constructor metodi

Constructor metodi maxsus metod hisoblanadi:

* ‌Uning aniq nomi "constructor" bo'lishi kerak
* ‌Yangi obyekt yaratilganda u avtomatik tarzda bajariladi
* ‌U obyekt xususiyatlarini ishga tushirish uchun ishlatiladi

Agar constructor metodini yozmasangiz, JavaScript bo'sh constructor metod qo'shadi

### Class metodlari

Class metodlari obyekt metodlari bilan bir xil sintaksis bilan yaratiladi.

Class yaratish uchun `class` kalit soʻzidan foydalaning.

Har doim `constructor()` metodini qoʻshing.

Keyin istaganingizcha metod qoʻshing.

{% code title="Sintaksis:" %}
```
class ClassName {
  constructor() { ... }
  method_1() { ... }
  method_2() { ... }
  method_3() { ... }
}
```
{% endcode %}

Car-ning yoshini qaytaradigan "age" nomli class metodini yarating:

```
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
  age() {
    let date = new Date();
    return date.getFullYear() - this.year;
  }
}

let myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML =
"My car is " + myCar.age() + " years old.";
```

Parametrlarni Class metodlariga yuborishingiz mumkin.

```
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
  age(x) {
    return x - this.year;
  }
}

let date = new Date();
let year = date.getFullYear();

let myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML=
"My car is " + myCar.age(year) + " years old.";
```

### Brauzerning qo'llab-quvvatlashi

Quyidagi jadvalda brauzerlar qaysi versiyadan boshlab arrow funksiyalarni to'liq qo'llab-quvvatlashi ko'rsatilgan:

| Chrome 49 | Edge 12   | Firefox 45 | Safari 9  | Opera 36  |
| --------- | --------- | ---------- | --------- | --------- |
| Mar, 2016 | Jul, 2015 | Mar, 2016  | Oct, 2015 | Mar, 2016 |

{% hint style="warning" %}
Ushbu qo'llanmada keyinchalik classlar haqida batafsil bilib olasiz.
{% endhint %}
