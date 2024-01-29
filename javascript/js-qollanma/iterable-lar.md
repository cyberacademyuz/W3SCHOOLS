# Iterable-lar

{% hint style="success" %}
Iterablelar takrorlanadigan obektlar hisoblanadi (massivlar kabi).

Iterablelarga oddiy va samarali kod bilan kirish mumkin.

Takrorlanuvchilarni`for..of`tsikllari bilan takrorlash mumkin
{% endhint %}

### For Of Loop

`for..of` steymenti takrorlanadigan (iterable) obektning elementlari bo'ylab aylanadi.

{% code title="Sintaksis" %}
```
for (variable of iterable) {
  // code block to be executed
}
```
{% endcode %}

### Takrorlash

Iteratsiyani tushunib olish oson.

Bu shunchaki elementlar ketma-ketligi bo'ylab harakatlanishni anglatadi.

Mana bunga bir nechta sodda misollar:

* String bo'ylab hakatlanish
* Massiv bo'ylab hakatlanish

### String bo'ylab hakatlanish

Siz string elementlarini iteratsiya qilish uchun `for..of` tsiklidan foydalanishingiz mumkin:

```
const name = "W3Schools";

for (const x of name) {
  // code block to be executed
}
```

### Massiv bo'ylab hakatlanish

Massiv elementlarini iteratsiya qilish uchun `for..of` sikldan foydalanishingiz mumkin:

```
const letters = ["a","b","c"];

for (const x of letters) {
  // code block to be executed
}
```

{% hint style="warning" %}
Iterablelar haqida [JS Object Iterables](https://www.w3schools.com/js/js\_object\_iterables.asp) bo'limida ko'proq ma'lumot bilib olishingiz mumkin.
{% endhint %}

### To'plam bo'ylab harakatlanish

Toʻplam elementlarini iteratsiya qilish uchun `for..of` tsikldan foydalanishingiz mumkin:

```
const letters = new Set(["a","b","c"]);

for (const x of letters) {
  // code block to be executed
}
```

{% hint style="warning" %}
Setlar va Maplar-ni keyingi bo'limda ko'rib chiqamiz.
{% endhint %}

### Map-lar bo'ylab harakatlanish

Map elementlarini iteratsiya qilish uchun `for..of` tsikldan foydalanishingiz mumkin:

```
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);

for (const x of fruits) {
  // code block to be executed
}
```
