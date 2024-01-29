# Xatoliklar

## Throw va Try...Catch...Finally

`try` steytmenti bajarilishi kerak bo'lgan kod blokini o'z ichiga oladi (sinab ko'rish uchun).

`catch` steytmenti har qanday xatolikni bartaraf qilish uchun berilgan kod blokini o'z ichiga oladi.

`finally` steytmenti kodning natijasi qanday bo'lishidan qat'iy nazar bajariladigan kod blokini o'z ichiga oladi.

`throw` steytmenti maxsus xatoni belgilaydi.

### Xatolik sodir bo'lsa!

Kodingizni ishga tushirganingizda turli xil xatolar yuzaga kelishi mumkin.

Xatolar, dasturchi tomonidan yo'l qo'yilgan sintaksis xatolar,  noto'g'ri yozilgan kod natijasida yuzaga kelgan xatolar va oldindan aytib bo'lmaydigan boshqa xatoliklar bo'lishi mumkin.

{% code title="Ushbu misolda xatolik yuzaga kelishi uchun "alert" ni "adddlert" deb noto'g'ri yozdik:" %}
```html
<p id="demo"></p>

<script>
try {
  adddlert("Welcome guest!");
}
catch(err) {
  document.getElementById("demo").innerHTML = err.message;
}
</script>
```
{% endcode %}

{% hint style="warning" %}
JavaScript **adddlert-ni** xato sifatida oladi va uni boshqarish uchun catch kodini bajaradi.
{% endhint %}

### JavaScriptda try va catch+

Try steytmenti bajarilish vaqtida xatoliklarni tekshirish uchun kod blokini ifodalash imkonini beradi.

`catch` steymenti  `try` blokida xatolik yuzaga kelganda, bajariladigan kod blokini belgilash imkonini beradi.

JavaScriptning `try` va `catch` steytmentlari doim birga yoziladi:

```javascript
try {
  Block of code to try
}
catch(err) {
  Block of code to handle errors
}
```

### JavaScript Throw xatolari

Xatolik yuzaga kelganida, odatda kod to'xtaydi va xato xabari ko'rsatiladi.

Uning texnik nomi: JavaScript istisno yaratadi.

{% hint style="warning" %}
JavaScript aslida ikkita xususiyatga ega **Error obyektini** yaratadi: **name** va **message**.
{% endhint %}

### Throw steytmenti

`throw` steytmenti sizga maxsus xato yaratishga imkon beradi.

Texnik jihatdan siz **istisno holatini berishingiz mumkin**.

Istisno  `String`, `Number`, `Boolean` yoki `Object` bo'lishi mumkin:

```javascript
throw "Too big";    // throw a text
throw 500;          // throw a number
```

Agar `throw`ni `try` va `catch` bilan birga ishlatsangiz, dasturning bajarilish ketma-ketligini boshqarishingiz va maxsus xato xabarlarini yaratishingiz mumkin.

### Inputni tekshirishga misol

Ushbu misoldagi kod berilgan ma'lumotning to'g'ri ekanligini tekshiradi. Qiymat noto'g'ri bo'lsa, istisno (xato) tashlanadi.

Xato catch steytmenti tomonidan tutiladi va maxsus xato xabari ko'rsatiladi:

```html
<!DOCTYPE html>
<html>
<body>

<p>Please input a number between 5 and 10:</p>

<input id="demo" type="text">
<button type="button" onclick="myFunction()">Test Input</button>
<p id="p01"></p>

<script>
function myFunction() {
  const message = document.getElementById("p01");
  message.innerHTML = "";
  let x = document.getElementById("demo").value;
  try {
    if(x.trim() == "") throw "empty";
    if(isNaN(x)) throw "not a number";
    x = Number(x);
    if(x < 5) throw "too low";
    if(x > 10) throw "too high";
  }
  catch(err) {
    message.innerHTML = "Input is " + err;
  }
}
</script>

</body>
</html>
```

### HTMLni tekshirish

Yuqoridagi kod shunchaki bir misol.

Zamonaviy brauzerlar ko'pincha HTML atributlarida belgilab qo'ylgan predefined tekshirish qoidalaridan foydalangan holda JavaScript va built-in HTML tekshiruvi kombinatsiyasidan foydalanishadi:

```
<input id="demo" type="number" min="5" max="10" step="1">
```

Formalarni tekshirish haqida batafsil ma'lumotni keyingi bo'limda o'qishingiz mumkin.

### Finally steytmenti

`finally` steytmenti, kod natijasi qanday bo'lishidan qat'iy nazar, try va catch dan keyin bajariladigan kodni o'z ichiga oladi:

{% code title="Sintaksis:" %}
```
try {
  Block of code to try
}
catch(err) {
  Block of code to handle errors
}
finally {
  Block of code to be executed regardless of the try / catch result
} 
```
{% endcode %}

```
function myFunction() {
  const message = document.getElementById("p01");
  message.innerHTML = "";
  let x = document.getElementById("demo").value;
  try {
    if(x.trim() == "") throw "is empty";
    if(isNaN(x)) throw "is not a number";
    x = Number(x);
    if(x > 10) throw "is too high";
    if(x < 5) throw "is too low";
  }
  catch(err) {
    message.innerHTML = "Error: " + err + ".";
  }
  finally {
    document.getElementById("demo").value = "";
  }
}
```

### Error obyekti

JavaScript-da xatolik yuzaga kelganda xato haqida ma'lumot beruvchi maxsus Error obyekti mavjud.

Error obyekti ikkita foydali xususiyatni taqdim etadi: name va message.

### Error obyektining xususiyatlari

| Xususiyat | Tavsif                                                    |
| --------- | --------------------------------------------------------- |
| name      | Xato nomini belgilaydi yoki qaytaradi                     |
| xabar     | Xato xabarini belgilaydi yoki qaytaradi (string shaklida) |

### Error name qiymatlari

Errorning name xususiyati orqali olti xil qiymat qaytarilishi mumkin:

| Error name       | Tavsif                                |
| ---------------- | ------------------------------------- |
| EvalError        | Eval() funksiyasida xatolik yuz berdi |
| RangeError       | Raqam chegaradn oshib ketdi           |
| Referans error   | Noqonuniy havola yuz berdi            |
| Sintaksis xatosi | Sintaksis xatosi yuz berdi            |
| TypeError        | Tur xatosi yuz berdi                  |
| URIE xatosi      | encodeURI() da xatolik yuz berdi      |

Yuqoridagi olti xil qiymat haqida ma'lumotlar.

### Eval Error

`EvalError` eval() funktsiyasidagi xatoni bildiradi.

{% hint style="danger" %}
JavaScript-ning yangi versiyalari EvalError-ni tashlamaydi. Buning o'rniga SyntaxError dan foydalaning.
{% endhint %}

### Range Error

Agar belgilangan qiymatlar chegarasidan katta raqamdan foydalansangiz, `RangeError` yuzaga keladi.

Masalan: Siz raqamning muhim raqamlari sonini 500 ga o'rnatolmaysiz.

```
let num = 1;
try {
  num.toPrecision(500);   // A number cannot have 500 significant digits
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

### Reference Error

Agar e'lon qilinmagan o'zgaruvchidan foydalansangiz `ReferenceError` xatoligi yuzaga keladi:

```
let x = 5;
try {
  x = y + 1;   // y cannot be used (referenced)
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

### Syntax error

Sintaksis xatosi bilan kodni baholashga harakat qilsangiz, `SyntaxError` yuzaga keladi.

```
try {
  eval("alert('Hello)");   // Missing ' will produce an error
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

### Type Error

Agar kutilgan ma'lumot turidan tashqarida bo'lgan qiymatdan foydalansangiz, `TypeError` yuzga keladi:

```
let num = 1;
try {
  num.toUpperCase();   // You cannot convert a number to upper case
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

### URI (Uniform Resource Identifier) Error

URI funksiyasida noto'g'ri belgilardan foydalansangiz, `URIError` xatoligi yuzaga keladi:

```
try {
  decodeURI("%%%");   // You cannot URI decode percent signs
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

### Nostandart Error obyekti xususiyatlari

{% hint style="danger" %}
Mozilla va Microsoft ba'zi nostandart Error obekt xususiyatlarini belgilaydi:

fileName (Mozilla)\
lineNumber (Mozilla)\
columnNumber (Mozilla)\
stack (Mozilla)\
description (Microsoft)\
number (Microsoft)



Ushbu xususiyatlarni public veb-saytlarda ishlatmang. Ular barcha brauzerlarda ishlamaydi.
{% endhint %}

### Xato haqida toʻliq maʼlumotnoma

Xato haqida to'liq ma'lumotnomani ko'rish uchun bizning [Error obekti haqida to'liq ma'lumotnoma](https://www.w3schools.com/jsref/jsref\_obj\_error.asp) sahifamizga o'ting.
