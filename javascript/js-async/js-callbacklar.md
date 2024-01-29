# JS Callbacklar

{% hint style="success" %}
_"Keyinroq  chqiraman!"_

Callback - bu boshqa funktsiyaga argument sifatida uzatiladigan funktsiyadir

Ushbu texnika funktsiyaga boshqa funktsiyani chaqirish imkonini beradi

Callback funktsiyasi boshqa funktsiya tugagandan keyin ishga tushishi mumkin
{% endhint %}

### Funktsiyalar ketma-ketligi

Funksiyalar chaqirilgan ketma-ketlikda bajariladi. Ular belgilangan ketma-ketlikda emas.

Ushbu misoldagi kod "Goodbye"ni ko'rsatish bilan tugaydi:

```
function myFirst() {
  myDisplayer("Hello");
}

function mySecond() {
  myDisplayer("Goodbye");
}

myFirst();
mySecond();
```

Ushbu misoldagi kod "Hello" ni ko'rsatish bilan tugaydi:

```
function myFirst() {
  myDisplayer("Hello");
}

function mySecond() {
  myDisplayer("Goodbye");
}

mySecond();
myFirst();
```

### Ketma-ketlikni boshqarish

Ba'zan siz funktsiyani qachon bajarilish kerakligini nazorat qilishni xohlaysiz.

Aytaylik, hisob-kitob qilishni xohlaysiz va natijani ko'rsatasiz.

Natijani ko'rsatish uchun kalkulyator funksiyasini ( `myCalculator`) chaqirishingiz, natijani saqlashingiz va keyin boshqa funktsiyani (`myDisplayer`) chaqirishingiz mumkin:

```
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}

function myCalculator(num1, num2) {
  let sum = num1 + num2;
  return sum;
}

let result = myCalculator(5, 5);
myDisplayer(result);
```

Yoki kalkulyator funksiyasini chaqirishingiz (`myCalculator`) va kalkulyator funksiyasi ma'lumotni ekranga ko'rsatuvchi funksiyani (`myDisplayer)` chaqirishi mumkin:

```
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}

function myCalculator(num1, num2) {
  let sum = num1 + num2;
  myDisplayer(sum);
}

myCalculator(5, 5);
```

Yuqoridagi birinchi misoldagi kod bilan bog'liq muammo shundaki, natijani ko'rsatish uchun ikkita funktsiya chaqirishingiz kerak.

Ikkinchi misoldagi muammo esa, kalkulyator funksiyasini natijani ko'rsatishiga to'sqinlik qila olmaysiz.

Endi callbackdan foydalanish vaqti keldi.

### JavaScript-da callback

{% hint style="warning" %}
Callback - bu boshqa funktsiyaga argument sifatida uzatiladigan funktsiya.
{% endhint %}

Callbackdan foydalanib, kalkulyator funksiyasini (`myCalculator`) callback ( `myCallback`) bilan chaqirishingiz mumkin va hisoblash tugagandan so'ng kalkulyator funksiyasiga callbackni ishga tushirishga ruxsat berishingiz mumkin:

```
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}

function myCalculator(num1, num2, myCallback) {
  let sum = num1 + num2;
  myCallback(sum);
}

myCalculator(5, 5, myDisplayer);
```

Yuqoridagi misolda callback funksiyasi `myDisplayer` hisoblanadi.

Bu `myCalculator()`ga argument sifatida uzatiladi.

{% hint style="warning" %}
### Eslatma

Funktsiyani argument sifatida topshirganingizda, qavs ishlatmaslik kerakligini unutmang.

To'g'ri: myCalculator(5, 5, myDisplayer);

Noto'g'ri: ~~myCalculator(5, 5, myDisplayer())~~;
{% endhint %}

```
// Create an Array
const myNumbers = [4, 1, -20, -7, 5, 9, -6];

// Call removeNeg with a callback
const posNumbers = removeNeg(myNumbers, (x) => x >= 0);

// Display Result
document.getElementById("demo").innerHTML = posNumbers;

// Keep only positive numbers
function removeNeg(numbers, callback) {
  const myArray = [];
  for (const x of numbers) {
    if (callback(x)) {
      myArray.push(x);
    }
  }
  return myArray;
}

```

Yuqoridagi misolda, `(x) => x >= 0`  callback funktsiyasi hisoblanadi.

Bu `removeNeg()` ga argument sifatida uzatiladi.

### Callbackni qachon ishlatish kerak ?

Yuqoridagi misollar qiziqarli emas.

Ular sizga callback sintaksisini o'rgatish uchun soddalashtirilgan.

Callbacklar haqiqatan ham asinxron funktsiyalarda juda qiziqarli, unda bir funktsiya boshqa funktsiyani kutishi kerak (masalan, fayl yuklanishini kutish).

Asinxron funksiyalar keyingi bo'limda o'rgariladi.
