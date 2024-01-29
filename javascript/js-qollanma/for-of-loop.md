# For of loop

### For Of Loop

`for of` tskil takrorlanuvchi obektning qiymatlari bo'ylab harakatlanadi.

Bu sizga massivlar, stringlar, maplar, NodeLists va boshqa shu kabi takrorlanuvchi maʼlumot tuzilmalari ustidan harakatlanish imkonini beradi:

{% code title="Sintaksis" %}
```
for (variable of iterable) {
  // code block to be executed
}
```
{% endcode %}

O'zgaruvchi - har bir iteratsiya uchun o'zgaruvchiga keyingi xususiyatning qiymati tayinlanadi. _O'zgaruvchi_ `const` , `let`yoki `var` bilan e'lon qilinishi mumkin.

iterable - takrorlanadigan xususiyatlarga ega bo'lgan obekt.

### Brauzerning qo'llab-quvvatlashi

For/of JavaScript-ga 2015 yilda qo'shilgan ([ES](https://www.w3schools.com/js/js\_es6.asp)6)

Safari 7 quyidagini qo'llab-quvvatlaydigan birinchi brauzer edi:

| Chrome    | Edge     | Firefox    | Safari   |          |
| --------- | -------- | ---------- | -------- | -------- |
| Chrome 38 | Edge 12  | Firefox 51 | Safari 7 | Opera 25 |
| Oct 2014  | Jul 2015 | Oct 2016   | Oct 2013 | Oct 2014 |

**For/of** Internet Explorer-da qo'llab-quvvatlanmaydi.

### Massiv bo'ylab harakatlanish

```
const cars = ["BMW", "Volvo", "Mini"];

let text = "";
for (let x of cars) {
  text += x;
}
```

### String boy'lab harakatlanish

```
let language = "JavaScript";

let text = "";
for (let x of language) {
text += x;
}
```

### While tsikli

`while` va `do/while` tskil haqida keyingi bo'limda tushuntiriladi.
