# JSON Massivlar

Bu JSON stringgi:

```
'["Ford", "BMW", "Fiat"]'
```

JSON stringida JSON massiv literali mavjud:

```
["Ford", "BMW", "Fiat"]
```

JSON-dagi massivlar JavaScript-dagi massivlar bilan deyarli bir xil.

_JSON-da massiv qiymatlari string, raqam, obyekt, massiv, boolean yoki null_ turida bo'lishi kerak.

**JavaScript**da massiv qiymatlari yuqoridagi barcha qiymatlarni, va hatto boshqa har qanday JavaScript steytmentini (funksiyalar, sanalar, undefined) o'z ichiga ola oladi:

### JavaScript massivlari

Siz literaldan JavaScript stringini yaratishingiz mumkin:

```
myArray = ["Ford", "BMW", "Fiat"];
```

JSON stringini parse qilish orqali JavaScript massivini yaratishingiz mumkin:

```
myJSON = '["Ford", "BMW", "Fiat"]';
myArray = JSON.parse(myJSON);
```

### Massiv qiymatlariga murojaat qilish

Nassiv qiymatlariga indeks bo'yicha murojaat qilasiz:

```
myArray[0];
```

### Obyektlardagi massivlar

Obyektlar massivlarni o'z ichiga olishi mumkin:

```
{
"name":"John",
"age":30,
"cars":["Ford", "BMW", "Fiat"]
}
```

Massiv qiymatlariga indeks bo'yicha murojaat qilasiz:

```
myObj.cars[0];
```

### Massiv bo'ylab harakatlanish

Massiv qiymatlariga `for in` tsikli yordamida murojaat qilishingiz mumkin:

```
for (let i in myObj.cars) {
  x += myObj.cars[i];
}
```

Yoki `for` tsiklidan foydalanishingiz mumkin:

```
for (let i = 0; i < myObj.cars.length; i++) {
  x += myObj.cars[i];
}
```
