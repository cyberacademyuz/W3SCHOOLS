# For in loop

## For In tsikli

`for in` tskili obektning xususiyatlari bo'ylab harakatlanadi:

{% code title="Sintaksis" %}
```
for (key in object) {
  // code block to be executed
} 
```
{% endcode %}

```
const person = {fname:"John", lname:"Doe", age:25};

let text = "";
for (let x in person) {
  text += person[x];
}
```

### Misol orqali tushuntirish

* `for in` tsikli person obekti ustidan takrorlanadi
* Har bir iteratsiya (x) kalitini qaytaradi
* x kaliti obektning qiymatiga murojaat qilish uchun ishlatiladi
* Kalitning qiymati - person\[x]

### Massivlar ustida for in

`for in` steytmenti  massivning xossalari ustidan ham harakatlanishi mumkin:

{% code title="Sintaksis" %}
```
for (variable in array) {
  code
}
```
{% endcode %}

```
const numbers = [45, 4, 9, 16, 25];

let txt = "";
for (let x in numbers) {
  txt += numbers[x];
}
```

{% hint style="warning" %}
Agar indeks tartibi muhim bo'lsa, massivda for in dan foydalanmang.

Indeks tartibi amalga oshirishga bog'liq va massiv qiymatlariga siz hohlagandek tartibda murojaat qilish imkoni bo'lmasligi mumkin.

Tartib muhim bo'lsa, **for** tsikli, **for of** tskili yoki **Array.forEach()** dan foydalanish yaxshi.
{% endhint %}

### Array.forEach()

`forEach()` metodi har bir massiv elementi uchun bir marta funktsiyani (callback funktsiyasi) chaqiradi.

```
const numbers = [45, 4, 9, 16, 25];

let txt = "";
numbers.forEach(myFunction);

function myFunction(value, index, array) {
  txt += value;
}
```

E'tibor bering, funktsiya 3 ta argument qabul qiladi:

* Element qiymati
* Element indeksi
* Massivning o'zi

Yuqoridagi misodal faqat qiymat parametridan foydalanilgan. Uni quyidagicha qayta yozish mumkin:

```
const numbers = [45, 4, 9, 16, 25];

let txt = "";
numbers.forEach(myFunction);

function myFunction(value) {
  txt += value;
}
```
