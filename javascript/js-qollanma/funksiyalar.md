# Funksiyalar

{% hint style="success" %}
JavaScriptda funktsiyalar ma'lum bir vazifani bajarish uchun mo'ljallangan kod bloki hisoblanadi.

Funksiya "birornima" uni chaqirganida bajariladi.
{% endhint %}

```javascript
// p1 va p2 ko'paytmasini hisoblovchi funktsiya
function myFunction(p1, p2) {
  return p1 * p2;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_functions" %}

### Javsacriptda funksiya sintaksisi

JavaScriptda funksiya `function` kalit so'zi va undan keyin uning nomi va keyin qavs **()** bilan yoziladi.

Funksiya nomlarida harflar, raqamlar, pastki chiziq va dollar belgilari bo'lishi mumkin (o'zgaruvchilar kabi).

Qavs ichida qavslar yordamida bir nechta parametr kiritish mumkin: **( **_**parametr1, parametr2, ...**_** )**

Funksiya tomonidan bajariladigan kod jingalak **{ }** qavslar ichiga yoziladi:

```javascript
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

Funksiya **parametrlari** funksiyaning qavslar () ichida berilgan.

Funksiya **argumentlari** funksiya chaqirilganda qabul qiladigan **qiymatlar**dir.

Funksiya ichida argumentlar (parametrlar) local o'zgaruvchilar sifatida ishlaydi.

### Funksiyani chaqirish

Funksiya ichidagi kod "birornima" uni chaqirganida bajariladi.

* Hodisa sodir bo'lganda (foydalanuvchi tugmani bosganda)
* JavaScript kodda chaqirilganda.
* Avtomatik (o'z-o'zidan chaqiriladi)

Funksiyani chaqirish haqida keyinroq batafsil bilib olasiz.

### Funksiyani qaytarish

Steytment tugaganida `return` funksiya bajarilishini to'xtatadi.

Agar funksiya steytment tomonidan chaqirilgan bo'lsa, Javascript chaqiruvchi steytmentdan keyin kodni bajarish uchun "return" qiladi.

Funksiyalar ko'pincha **return qiymatini** hisoblashadi. Return qiymati "chaqiruvchiga" ga "return" qilinadi:

{% code title="Ikki raqamning qiymatini hisoblang va natijani qaytaring:" %}
```javascript
let x = myFunction(4, 3); // Funksiya chaqiriladi, qaytariladigan qiymat x bilan tugaydi

function myFunction(a, b) {
  return a * b; // Funksiya a va b ko'paytmasini qaytaradi
}

// x dagi natija quyidagicha bo'ladi:
12
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_function_return" %}

{% hint style="warning" %}
### Nima uchun funksiyalar ?

Siz kodni qayta ishlatishingiz mumkin.

Kodni bir marta yaratb undan ko'p marta foydalana olasiz.

Turli natijalarga erishish uchun siz bir xil kodni turli argementlar bilan bir necha marta ishlatishingiz mumkin.
{% endhint %}

### () operatori&#x20;

() operatori funksiyani chaqiradi (call):

{% code title="Farengeytni Selsiyga aylantiring:" %}
```javascript
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
let value = toCelsius(77);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_farenheit_to_celsius" %}

Funksiyaga noto'g'ri parametrlar bilan murojaat qilish noto'g'ri javob qaytarishi mumkin:

```javascript
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}

let value = toCelsius(); 
```

Funksiyani () belgisiz chaqirish funksiya natijasini emas, funksiya obyektini qaytaradi.

```javascript
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
let value = toCelsius;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_farenheit_to_celsius_2" %}

{% hint style="warning" %}
### Eslatma

Yuqoridagi misolda, `toCelsius` funksiya obyektiga murojaat qiladi va `toCelsius()` esa funksiya natijasiga murojaat qiladi.
{% endhint %}

### O'zgaruvchining qiymati sifatida ishlatiladigan funksiyalar

Funksiyalardan o'zgaruvchilardan foydalanganingizdek, barcha turdagi formulalar, topshiriqlar va hisob-kitoblarda foydalanish mumkin.

{% code title="Misol:" %}
```javascript
// Funksiyandan qaytadigan qiymatni saqlash uchun o'zgaruvchidan foydalanish o'rniga:
let x = toCelsius(77);
let text = "The temperature is " + x + " Celsius";

// Funktsiyani to'g'ridan-to'g'ri o'zgaruvchi qiymati sifatida foydalanishingiz mumkin:
let text = "The temperature is " + toCelsius(77) + " Celsius";
```
{% endcode %}

{% hint style="warning" %}
Funksiyalar haqida keyinroq batafsil bilib olasiz.
{% endhint %}

### Local o'zgaruvchilar

JavaScriptda funksiya ichida e'lon qilingan o'zgaruvchilar funksiya uchun **local** o'zgaruvchi hisoblanadi.

Local o'zgaruvchilardan faqat funksiya ichida foydalanish mumkin.

```javascript
// Bu yerda carName dan foydalanib bo'lmaydi

function myFunction() {
  let carName = "Volvo";
  // Bu yerda carName dan foydalanish mumkin.
}

// Bu yerda carName dan foydalanib bo'lmaydi
```

Local o'zgaruvchilar faqat ularning funksiyalari ichida ishlagani uchun bir xil nomga ega o'zgaruvchilar turli funksiyalarda ishlatilishi mumkin.

Local o'zgaruvchilar funksiya ishga tushganda yaratiladi va funksiya tugaganidan keyin o'chiriladi.
