# Random

### Math.random()

`Math.random()` 0 va 1 orasidagi tasodifiy sonni qaytaradi:

```
// Returns a random number:
Math.random();
```

{% hint style="warning" %}
`Math.random()`har doim 1 dan kichik raqam qaytaradi.
{% endhint %}

### Tasodifiy butun sonlar

`Math.floor()` bilan ishlatiladigan `Math.random()` tasodifiy butun sonlarni qaytarish uchun ishlatilishi mumkin.

{% hint style="warning" %}
JavaScript butun sonlari kabi narsa yo'q.

Bu yerda biz o'nli kasrsiz raqamlar haqida gapiramiz.
{% endhint %}

```
// Returns a random integer from 0 to 9:
Math.floor(Math.random() * 10);
```

```
// Returns a random integer from 0 to 10:
Math.floor(Math.random() * 11);
```

```
// Returns a random integer from 0 to 99:
Math.floor(Math.random() * 100);
```

```
// Returns a random integer from 0 to 100:
Math.floor(Math.random() * 101);
```

```
// Returns a random integer from 1 to 10:
Math.floor(Math.random() * 10) + 1;
```

```
// Returns a random integer from 1 to 100:
Math.floor(Math.random() * 100) + 1;
```

### To'g'ri tasodifiy funktsiya

Yuqoridagi misollardan ko'rinib turibdiki, barcha tasodifiy butun sonlar uchun to'g'ri tasodifiy funktsiyani yaratish yaxshi fikr bo'lishi mumkin.

Ushbu JavaScript funksiyasi har doim minimal va maksimal raqam o'rtasidagi tasodifiy sonni qaytaradi:

```
function getRndInteger(min, max) {
  return Math.floor(Math.random() * (max - min) ) + min;
}
```

Ushbu JavaScript funksiyasi har doim minimal va maksimal raqam o'rtasidagi tasodifiy sonni qaytaradi:

```
function getRndInteger(min, max) {
  return Math.floor(Math.random() * (max - min + 1) ) + min;
}
```
