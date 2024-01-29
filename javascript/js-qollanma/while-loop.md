# While loop

Berilgan shart rost bo'lsa, tsikllar kod blokini bajarishi mumkin.

### While tsikli

Berilgan shart rost bo'lsa, `while` tsikli kod bloki bo'ylab harakatlanadi .

#### Sintaksis

```
while (condition) {
  // code block to be executed
}
```

#### Misol

Quyidagi misolda, (i) o'zgaruvchisi 10 dan kichik bo'lsa, tsikldagi kod qayta-qayta ishlaydi:

```
while (i < 10) {
  text += "The number is " + i;
  i++;
}
```

{% hint style="warning" %}
Agar shartda o'zgaruvchi qiymatini oshirishni unutib qo'ysangiz, tsikl hech qachon tugamaydi. Bu brauzerni ishdan chiqaradi.
{% endhint %}

### Do while tsikli

`do while` tskili while siklining boshqa bir varianti hisoblanadi. Bu tsikl kod blokini shartning to'g'ri yoki noto'g'riligini tekshirishdan avval bir marta bajariladi, keyin shart to'g'ri bo'lsa, u tsiklni takrorlaydi.

#### Sintaksis

```
do {
  // code block to be executed
}
while (condition);
```

#### Misol

Quyidagi misolda `do while` tskilidan foydalanilgan. Shart noto'g'ri bo'lsa ham, tsikl har doim kamida bir marta bajariladi, chunki kod bloki shart tekshiruvidan oldin berilgan:

```
do {
  text += "The number is " + i;
  i++;
}
while (i < 10);
```

Shart ichida ishlatiladigan o'zgaruvchini oshirishni unutmang, aks holda tsikl hech qachon tugamaydi!

### For va while-ni taqqoslash

Agar siz for tsikli haqidagi oldingi bo'limni tugatgan bo'lsangiz, `while` sikli ham `for` tsikli bilan deyarli bir xil ekanligini, unga 1-steytment va 3-steytment berilmaganligini bilib olgandursiz.

Ushbu misoldagi tsikl cars massividan avtomobil nomlarini to'plash uchun for tsiklidan foydalanadi:

```
const cars = ["BMW", "Volvo", "Saab", "Ford"];
let i = 0;
let text = "";

for (;cars[i];) {
  text += cars[i];
  i++;
}
```

Ushbu misoldagi tsikl cars massividan avtomobil nomlarini to'plash uchun while tsiklidan foydalanadi:

```
const cars = ["BMW", "Volvo", "Saab", "Ford"];
let i = 0;
let text = "";

while (cars[i]) {
  text += cars[i];
  i++;
}
```
