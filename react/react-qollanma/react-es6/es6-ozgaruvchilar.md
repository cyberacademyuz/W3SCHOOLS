# ES6 O'zgaruvchilar

### O'zgaruvchilar

ES6 dan oldin o'zgaruvchilarni e'lon qilishning faqat bitta usuli bor edi: `var` kalit so'z bilan. Agar ularni e'lon qilmagan bo'lsangiz, ular global obyektga tayinlangan bo'lar edi. Agar strict mode-da bo'lmasangiz, o'zgaruvchilaringiz e'lon qilinmagan bo'lsa, xatolik yuzaga keladi.

Endi ES6da o'zgaruvchilaringizni e'lon qilishning uchta usuli mavjud: `var`, `let`, va `const`.

{% code title="var" %}
```jsx
var x = 5.6;
```
{% endcode %}

Agar `var`ni funksiyadan tashqarida foydalansangiz, u global o'zgaruvchi bo'ladi.

Agar `var`ni funksiya ichida foydalansangiz, u o'sha funktsiyaga tegishli.

Agar `var`ni blok ichida, masalan for tsiklida foydalansangiz, o'zgaruvchi bunda ham blokdan tashqarida mavjud bo'ladi.

{% hint style="warning" %}
`var`_blok_ doirasi emas, balki _funksiya_ doirasiga ega .
{% endhint %}

{% code title="let" %}
```jsx
let x = 5.6;
```
{% endcode %}

`let`, `var`ning blok doirasidagi ko'rinishi boʻlib, u berilgan blok (yoki ifoda) orqali chegaralanadi.

Agar `let`ni blok ichida, ya'ni for tsiklidan foydalansangiz, o'zgaruvchi faqat shu tsikl ichida mavjud bo'ladi.

{% hint style="warning" %}
`let`_blok_ scopega ega.
{% endhint %}

{% code title="const" %}
```jsx
const x = 5.6;
```
{% endcode %}

`const` ham o'zgaruvchi hisoblanib, u e'lon qilingandan keyin uning qiymati hech qachon o'zgarmaydi.

{% hint style="warning" %}
`const`_blok_ scopega ega.
{% endhint %}

`const` biroz chalg'itadi.

`const` o'zgarmas qiymatni bildirmaydi. U qiymatga bo'glab qo'yiladigan o'zgarmas nomni ifodalaydi.

Shu sababli siz bularni qila olmaysiz:

* O'zgarmasning qiymatini qayta tayinlash
* O'zgarmas massivni qayta tayinlash
* O'zgarmas obyektni qayta tayinlash

Lekin bularni qila olasiz:

* O'zgarmas massiv elementlarini o'zgartirish
* O'zgarmas obyektning xususiyatlarini o'zgartirish
