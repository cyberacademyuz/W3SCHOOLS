# Funksiya parametrlari

Javascriptning `function` -ni parametr qiymatlari (argumentlari) bo'yicha hech qanday tekshiruvni amalga oshirmaydi.

### Funksiya parametrlari va argumentlari

Ushbu qo'llanmaning boshida funktsiyalar **parametrlarga** ega bo'lishi mumkinligini bilib oldingiz:

```
function functionName(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

Funksiya **parametrlari** funksiya taʼrifida keltirilgan **nomlardir**.

Funksiya **argumentlari** - bu funksiyaga berilgan **qiymatlar** hisoblanadi**.**

### Parametr qoidalari

Funksiya ta'riflari parametrlar uchun ma'lumot turlarini belgilamaydi.

Funksiyalar berilgan argumentlar turini tekshirishni amalga oshirmaydi.

Funktsiyalar qabul qilingan argumentlar sonini tekshirmaydi.

### Standart parametrlar

Agar funksiya unutib qoldirilgan (yetishmayotgan) argumentlar bilan chaqirilsa, yetishmayotgan paramet qiymatlari `undefined` bo'ladi.

Ba'zida bu ko'ngildagidek ishlaydi, lekin ba'zida parametrga standart qiymat berish yaxshiroq:

```
function myFunction(x, y) {
  if (y === undefined) {
    y = 2;
  }
}
```

### Standart parametr qiymatlari

ES6 funksiya parametrlariga standart qiymatlarga ega bo'lish imkonini beradi.

```
Agar y o'tkazilmasa yoki aniqlanmagan bo'lsa, u holda y = 10.

function myFunction(x, y = 10) {
  return x + y;
}
myFunction(5);
```

### Funksiyaning Rest parametri

Rest parametri (...) funktsiyaga cheksiz miqdordagi argumentlarni massiv sifatida ko'rib chiqishga imkon beradi:

```
function sum(...args) {
  let sum = 0;
  for (let arg of args) sum += arg;
  return sum;
}

let x = sum(4, 9, 16, 25, 29, 100, 66, 77);
```

### Argumentlar obyekti

JavaScript funktsiyalari argumentlar obyekti deb ataladigan built-in obyektga ega.

Argument obyekti funksiya chaqirilganda foydalaniladigan argumentlar massivini o‘z ichiga oladi.

Shunday qilib, raqamlar ro'yxatidagi eng katta qiymatni topish uchun funktsiyadan foydalanishingiz mumkin:

```
x = findMax(1, 123, 500, 115, 44, 88);

function findMax() {
  let max = -Infinity;
  for (let i = 0; i < arguments.length; i++) {
    if (arguments[i] > max) {
      max = arguments[i];
    }
  }
  return max;
}
```

Yoki barcha berilgan qiymatlarning umumiy qiymatini olish uchun funksiya yarating:

```
x = sumAll(1, 123, 500, 115, 44, 88);

function sumAll() {
  let sum = 0;
  for (let i = 0; i < arguments.length; i++) {
    sum += arguments[i];
  }
  return sum;
}
```

{% hint style="warning" %}
Agar funktsiya juda ko'p argumentlar bilan chaqirilsa (e'lon qilinganidan ko'ra ko'p), bu argumentlarga **argument obyekti** yordamida erishish mumkin.
{% endhint %}

### Argumentlar qiymat bo'yicha uzatiladi

Funksiya chaqirilgandagi parametrlar funksiya argumentlaridir.

Argumentlar qiymat bo'yicha uzatiladi: Funktsiya argumentning joylashuvini emas, balki faqat qiymatlarni bilib oladi.

Agar funktsiya argumentning qiymatini o'zgartirsa, u parametrning asl qiymatini o'zgartirmaydi.

**Argumentlardagi o'zgarishlar funksiyadan tashqarida ko'rinmaydi.**

### Obyektlar havola orqali uzatiladi

JavaScript-da obyekt havolalari qiymatlar hisoblanadi.

Shu sababli, obyektlar mos havola orqali uzatilgandek harakat qiladi:

Agar funksiya obyekt xususiyatini o'zgartirsa, u asl qiymatini o'zgartiradi.

**Obyekt xususiyatlariga kiritilgan o'zgarishlar funktsiyadan tashqarida ko'rinadi.**
