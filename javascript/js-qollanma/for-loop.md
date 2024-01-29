---
description: Looplar kod blokini bir necha marta bajarishi mumkin.
---

# For loop

### JavaScript sikllari

Agar siz biror kodni har safar boshqa qiymat bilan qayta-qayta ishlatmoqchi bo'lsangiz, tsikllar dan foydalanish qulaylik yaratadi.

Massivlar bilan ishlashda  ko'pincha shunday bo'ladi:

{% code title="Bunday yozish o'rniga:" %}
```
text += cars[0] + "<br>";
text += cars[1] + "<br>";
text += cars[2] + "<br>";
text += cars[3] + "<br>";
text += cars[4] + "<br>";
text += cars[5] + "<br>";
```
{% endcode %}

{% code title="Bunday yozishingiz mumkin:" %}
```
for (let i = 0; i < cars.length; i++) {
  text += cars[i] + "<br>";
}
```
{% endcode %}

### Turli xil looplar

JavaScript turli xil tsikllarni qo'llab-quvvatlaydi:

* `for`- kod blokini bir necha marta ishlatadi
* `for/in`- obektning xossalari bo'ylab harakatlanish
* `for/of`- takrorlanuvchi obektning qiymatlari bo'ylab harakatlanish
* `while`- belgilangan shart to'g'ri bo'lganda kod bloki bo'ylab harakatlanish
* `do/while`- da ham belgilangan shart rost bo'lganda kod bloki orqali harakatlanadi

### For Loop

`for` steytmenti 3 ta ixtiyoriy ifodadan iborat tsikl yaratadi:

```
for (expression 1; expression 2; expression 3) {
  // code block to be executed
}
```

**1-ifoda** kod blokining bajarilishidan oldin (bir marta) bajariladi.

**2-ifoda** kod blokini bajarish shartini belgilaydi.

**3-ifoda** (har safar) kod bloki bajarilgandan keyin bajariladi.

```
for (let i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}
```

Yuqoridagi misolni quyidagidek tushunishingiz mumkin:

1 ifoda tsikl boshlanishidan oldin i nomli o'zgaruvchi e'lon qiladi (i = 0 bo'lsin).

2-ifoda tsiklning ishlashi uchun shartni belgilaydi (i 5 dan kichik bo'lishi kerak).

3-ifoda har safar tsikldagi kod bloki bajarilganda i o'zgaruvchisining qiymatini oshiradi (i++).

### 1-Steytment

Odatda tsiklda ishlatiladigan o'zgaruvchini ishga tushirish uchun 1-ifodadan foydalanasiz (i = 0 bo'lsin).

Buni har doim ham berish shart emas, javascript bunga e'tibr bermadydi. 1 ifodani berish ixtiyoriy hisoblanadi.

1-ifodada vergul bilan ajratish orqali bir necha qiymatlar berishingiz mumkin:

```
for (let i = 0, len = cars.length, text = ""; i < len; i++) {
  text += cars[i] + "<br>";
}
```

Va steytmentni bermasangiz ham bo'ladi (masalan, tsikl ishlashidan avval uning qiymatlarini bergan bo'lsangiz):

```
let i = 2;
let len = cars.length;
let text = "";
for (; i < len; i++) {
  text += cars[i] + "<br>";
}
```

### 2-Steytment

Ko'pincha 2 steytment boshlang'ich o'zgaruvchining holatini taqqoslash uchun ishlatiladi.

Buni har doim ham berish shart emas, javascript bunga e'tibr bermadydi. 2 steytment ham ixtiyoriy hisoblanadi.

Agar 2 steytment rost bo'lsa, tsikl qaytadan boshlanadi. Agar u noto'g'ri bo'lsa, tsikl tugaydi.

{% hint style="warning" %}
Agar siz 2-steytmentni bermasangiz, tsikl ichida break berishingiz kerak  Aks holda, tsikl hech qachon tugamaydi. Bu brauzerni ishdan chiqaradi. Break-lar haqida ushbu qo‘llanmaning keyingi bo'limida o'rganing.
{% endhint %}

### 3-steytment

Ko'pincha 3-steytment boshlang'ich o'zgaruvchining qiymatini oshiradi.

Uni har doim ham berish shart emas, javascript bunga e'tibr bermadydi. 3 steytment ham ixtiyoriy hisoblanadi.

3 steytment  kamaytirish (i--), orttirish (i = i + 15) kabi  har qanday narsani bajarishi mumkin.

3-steytmentni ham kiritmasangiz bo'ladi (masalan, qiymatni tsikl ichida oshirganingizda):

```
let i = 0;
let len = cars.length;
let text = "";
for (; i < len; ) {
  text += cars[i] + "<br>";
  i++;
}
```

### Loop scopi

Loopda `var`dan foydalanish:

```
var i = 5;

for (var i = 0; i < 10; i++) {
  // some code
}

// Here i is 10
```

Loopda `let`dan foydalanish:

```
let i = 5;

for (let i = 0; i < 10; i++) {
  // some code
}

// Here i is 5
```

Birinchi misolda var yordamida siklda e'lon qilingan o'zgaruvchi tsikldan tashqaridagi o'zgaruvchini qayta e'lon qiladi.

Ikkinchi misolda, let dan foydalangan holda, tsiklda e'lon qilingan o'zgaruvchi tsikldan tashqaridagi o'zgaruvchini qayta e'lon qilmaydi.

i o'zgaruvchisini siklda e'lon qilish uchun let ishlatilsa, i o'zgaruvchisi faqat tsikl ichida ishlaydi.

### For/Of va For/In tsikllari

`for/in` va `for/of` tsikllari haqida keyingi bo'limda tushuntiriladi.

### While Loop-lari

`while` va `do/while` looplari keyingi bo'limda tushuntiriladi.
