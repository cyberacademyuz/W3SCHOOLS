# Break

`break` steytmenti butun tskildan chiqadi va natijada tsikl to'xtaydi.

`continue` steytmenti tsikldagi bir iteratsiyani qoldirib ketadi.

### break steytmenti

Siz bu qo'llanmaning avvalgi bo'limida `break` steytmentini ko'rdingiz. U `switch()` steytmentidan "chiqish" uchun ishlatilgan.

`break` steytmentidan tskildan chiqish uchun ham foydalanish mumkin:

```
for (let i = 0; i < 10; i++) {
  if (i === 3) { break; }
  text += "The number is " + i + "<br>";
}
```

Yuqoridagi misolda, tsikl iteratori (i) 3 bo'lsa, `break`  steytmenti tsiklni to'xtatadi.

### Continue steytmenti

Agar shart to'g'ri bo'lsa, `continue` steytmenti bitta iteratsiyani tashlab ketadi va tsikldagi keyingi iteratsiya bilan davom etadi.

Ushbu misolda 3 qiymatini o'tkazib yuborish ko'rsatilgan:

```
for (let i = 0; i < 10; i++) {
  if (i === 3) { continue; }
  text += "The number is " + i + "<br>";
}
```

### JavaScript labellar

JavaScript iboralarini belgilash uchun steytmentlar oldiga label nomi va ikki nuqta qoʻyasiz:

```
label:
statements
```

`break` va `continue` steytmentlari kod blokidan "chiqish" uchun mo'ljallangan yagona steytmentlardir.

Sintaksis:

```
break labelname;

continue labelname;
```

`continue` steytmenti (label bilan yoki labelsiz) faqat bitta sikl iteratsiyasini o'tkazib yuborish uchun ishlatilishi mumkin.

Labeli bo'lmagan `break` steytmenti faqat tsikldan yoki switchdan chiqish uchun ishlatilishi mumkin.

Labeli bo'lgan  `break` steytmenti har qanday kod blokidan chiqish uchun ishlatilishi mumkin:

```
const cars = ["BMW", "Volvo", "Saab", "Ford"];
list: {
  text += cars[0] + "<br>";
  text += cars[1] + "<br>";
  break list;
  text += cars[2] + "<br>";
  text += cars[3] + "<br>";
}
```

{% hint style="warning" %}
Kod bloki bu { va } orasidagi kodlar to'plamidir.
{% endhint %}
