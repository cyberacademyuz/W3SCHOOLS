# JS Asynchronous

{% hint style="success" %}
_"Keyinroq tugataman!"_

Boshqa funktsiyalar bilan parallel ravishda ishlaydigan funksiyalar asinxron deyiladi

JavaScriptdagi setTimeout() bunga misol bo'la oladi.
{% endhint %}

### Asinxron JavaScript

Oldingi bo'limda ishlatilgan misollar juda soddalashtirilgan misollar edi.

Misollarning maqsadi callback funktsiyalarining sintaksisini ko'rsatib berish edi holos:

```
function myDisplayer(something) {
  document.getElementById("demo").innerHTML = something;
}

function myCalculator(num1, num2, myCallback) {
  let sum = num1 + num2;
  myCallback(sum);
}

myCalculator(5, 5, myDisplayer);
```

Yuqoridagi misolda `myDisplayer` funksiyaning nomi.

U `myCalculator()` ga argument sifatida uzatiladi.

{% hint style="warning" %}
Real hayotda callback ko'pincha asinxron funktsiyalar bilan qo'llaniladi.

Bunga oddiy misol - JavaScriptdagi `setTimeout()`.
{% endhint %}

### Vaqt tugashini kutish

`setTimeout()` funksiyasidan foydalanilganda, berilgan vaqt tugashi bilan bajarilishi kerak bo'lgan  callback funksiyani belgilashingiz mumkin:

```
setTimeout(myFunction, 3000);

function myFunction() {
  document.getElementById("demo").innerHTML = "I love You !!";
}
```

Yuqoridagi misolda `myFunction` callback sifatida ishlatiladi.

`myFunction` `setTimeout()`ga argument sifatida uzatiladi.

3000 - berilgan vaqtning millisekundlardagi ko'rinishi, shuning uchun `myFunction()`3 soniyadan keyin chaqiriladi.

{% hint style="warning" %}
### Eslatma

Funktsiyani argument sifatida berganingida, qavs ishlatmaslik kerakligini unutmang.

To'g'ri: setTimeout (myFunction, 3000);

Noto'g'ri: ~~setTimeout(myFunction(), 3000)~~;
{% endhint %}

Funktsiya nomini boshqa funktsiyaga argument sifatida berish o'rniga, har doim butun funktsiyani berishingiz mumkin:

```
setTimeout(function() { myFunction("I love You !!!"); }, 3000);

function myFunction(value) {
  document.getElementById("demo").innerHTML = value;
}
```

Yuqoridagi misolda `function(){ myFunction("I love You !!!"); }` callback sifatida ishlatiladi. U to'liq funktsiyadir. To'liq funktsiya argument sifatida setTimeout() ga uzatiladi.

3000 - berilgan vaqtning millisekundlardagi ko'rinishi, shuning uchun `myFunction()`3 soniyadan keyin chaqiriladi.

### Intervallarni kutish:

`setInterval()` funktsiyasidan foydalanganda, har bir interval uchun bajarilishi kerak bo'lgan callback funksiyasi belgilashingiz mumkin:

```
setInterval(myFunction, 1000);

function myFunction() {
  let d = new Date();
  document.getElementById("demo").innerHTML=
  d.getHours() + ":" +
  d.getMinutes() + ":" +
  d.getSeconds();
}
```

Yuqoridagi misolda `myFunction` callback sifatida ishlatiladi.

`myFunctionsetInterval()`ga argument sifatida uzatiladi.

1000 - intervallar orasidagi millisekundlar soni, shuning uchun `myFunction()` har soniyada chaqiriladi.

### Callback uchun alternativalar

Asinxron dasturlash yordamida JavaScript dasturlari uzoq muddatli vazifalarni boshlashi va boshqa vazifalarni parallel ravishda bajarishni davom ettirishi mumkin.

Biroq, asinxron dasturlarni yozish va debugging qilish qiyin.

Shu sababli, ko'pgina zamonaviy asinxron metodlari callbacklardan foydalanmaydi. JavaScript-da asinxron dasturlashda callbacklar o'rniga Promises dan foydalaniladi.

{% hint style="warning" %}
### Eslatma

Siz promise haqida keyingi bo'limda bilib olasiz.
{% endhint %}
