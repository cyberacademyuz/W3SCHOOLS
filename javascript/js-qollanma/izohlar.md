---
description: >-
  Izohlar kodning vazifasini tushuntirish va yanada o'qishga osonlashtirish
  uchun ishlatiladi. Izohlardan kodlarni sinab ko'rayotganda boshqa bir kodning
  ishlashini oldini olish uchun ham foydalaniladi.
---

# Izohlar

## Bir qatorli izohlar

Bir qatorli izohlar `//` bilan boshlanadi.

Qatorning oxiri va `//` ning orasidagi har qanday matn JavaScript tomonidan amalga oshirilmaydi.

Ushbu misolda har bir kod qatoridan oldingi qatorda izohdan foydalanilgan:

{% code title="Misol" %}
```javascript
// Sarlavhani o'zgartirish:
document.getElementById("myH").innerHTML = "My First Page";

// Paragrafni o'zgartirish:
document.getElementById("myP").innerHTML = "My first paragraph.";
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_comments1" %}

Ushbu misolda, kodni tushuntirish uchun har bir qator oxirida bir qatorli izohdan foydalanilgan:

{% code title="Misol:" %}
```javascript
let x = 5;      // x o'zgaruvchisini e'lon qiling va unga 5 qiymatini bering
let y = x + 2;  // y o'zgaruvchisini e'lon qiling va unga x + 2 ning qiymatini bering
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_comments5" %}

### Ko'p qatorli izohlar

Ko‘p qatorli izohlar `/*` bilan boshlanadi va `*/` bilan tugaydi.

`/*` va `*/` orasidagi har qanday matn JavaScript tomonidan e'tiborga olinmaydi.

Ushbu misolda kodni tushuntirish uchun ko'p qatorli izohdan foydalanilgan

{% code title="Misol:" %}
```javascript
/*
The code below will change
the heading with id = "myH"
and the paragraph with id = "myP"
in my web page:
*/
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_comments2" %}

{% hint style="warning" %}
Bir qatorli izohlardan foydalanish keng tarqalgan.\
Ko'p qatorli izohlar ko'pincha rasmiy qo'llanmalar uchun ishlatiladi.
{% endhint %}

### Kod ishlashini oldini olish uchun izohlardan foydalanish

Kodning bajarilishini oldini olish uchun izohlardan foydalanish kodni tekshirish uchun juda qulay.

Kod qatorining boshiga `//`ni qo'shish orqali kod qatorini izohga aylantiriladi.

Ushbu misolda kod qatorlaridan birining bajarilishini oldini olish uchun `//`dan foydalanilgan:

```javascript
//document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_comments3" %}

Ushbu misolda esa bir nechta qatorli kodlarning bajarilishini oldini olish uchun ko'p qatorli izoh blokidan foydalilgan:

```javascript
/*
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
*/ 
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_comments4" %}
