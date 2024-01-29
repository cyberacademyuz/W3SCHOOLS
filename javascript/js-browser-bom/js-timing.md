# JS Timing

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

### Vaqt hodisalari

`window` obyekti belgilangan vaqt oralig'ida kodni bajarishga imkon beradi.

Bu vaqt oraliqlari vaqt hodisalari deb ataladi.

JavaScript-dan foydalanishning ikkita asosiy usuli:

* `setTimeout(`_`function, milliseconds`_)\
  Belgilangan millisekundlar tugagandan keyin, funktsiyani bajaradi.\

* `setInterval(`_`function, milliseconds`_)\
  setTimeout() bilan bir xil, lekin funksiyaning bajarilishini doimiy ravishda takrorlaydi.

{% hint style="warning" %}
`setTimeout()` va `setInterval()` ikkalasi ham HTML DOM Window obyektining metodlari hisoblanadi.
{% endhint %}

### setTimeout() metodii

```
window.setTimeout(function, milliseconds);
```

`window.setTimeout()` metodi window qo'shimchasisiz ham yozilishi mumkin.

Birinchi parametr bajariladigan funksiya hisoblanadi.

Ikkinchi parametr esa funksiyani necha millisekunddan keyin bajarilish kerakligini bildiradi.

{% code title="Tugmani bosing. 3 soniya kuting va sahifa "Salom" deb ogohlantiradi:" %}
```
<button onclick="setTimeout(myFunction, 3000)">Try it</button>

<script>
function myFunction() {
  alert('Hello');
}
</script>
```
{% endcode %}

### Kod ishga tushishini qanday to'xtatish kerak ?

`clearTimeout()` metodi setTimeout() ga berilgan funksiyaning bajarilishini to'xtatadi.

```
window.clearTimeout(timeoutVariable)
```

`window.clearTimeout()` metodi window qo'shimchasisiz yozilishi mumkin.

`clearTimeout()` metodi `setTimeout()`dan qaytarilgan o'zgaruvchidan foydalanadi:

```
myVar = setTimeout(function, milliseconds);
clearTimeout(myVar);
```

Agar funksiya hali bajarilmagan bo'lsa, `clearTimeout()` metodini chaqirish orqali kod ishlashini to'xtatishingiz mumkin:

{% code title="Yuqoridagi misol, lekin qo'shilgan "To'xtatish" tugmasi bilan:" %}
```
<button onclick="myVar = setTimeout(myFunction, 3000)">Try it</button>

<button onclick="clearTimeout(myVar)">Stop it</button>
```
{% endcode %}

### setInterval() metodi

`setInterval()` metodi berilgan  har bir vaqt oralig'ida berilgan funksiyani takrorlaydi.

```
window.setInterval(function, milliseconds);
```

`window.setInterval()` metodi window qo'shimchasisiz yozilishi mumkin.

Birinchi parametr bajariladigan funksiya hisoblanadi.

Ikkinchi parametr har bir bajarilish orasidagi vaqt oralig'ining uzunligini ko'rsatadi.

Ushbu misol har soniyada bir marta "myTimer" nomli funktsiyani bajaradi.

{% code title="Joriy vaqtni ko'rsatish:" %}
```
setInterval(myTimer, 1000);

function myTimer() {
  const d = new Date();
  document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}
```
{% endcode %}

{% hint style="warning" %}
Bir soniyada 1000 millisekund bor.
{% endhint %}

### Kod ishga tushishini qanday to'xtatish kerak ?

`clearInterval()` metodi `setInterval()` metodida ko'rsatilgan funksiyaning bajarilishini to'xtatadi.

```
window.clearInterval(timerVariable)
```

`window.clearInterval()` metodi window qo'shimchasisiz yozilishi mumkin.

`clearInterval()` metodi `setInterval()`dan qaytarilgan o'zgaruvchidan foydalanadi:

```
let myVar = setInterval(function, milliseconds);
clearInterval(myVar);
```

{% code title="Yuqoridagi misol, lekin biz "Vaqtni to'xtatish" tugmasini qo'shdik:" %}
```
<p id="demo"></p>

<button onclick="clearInterval(myVar)">Stop time</button>

<script>
let myVar = setInterval(myTimer, 1000);
function myTimer() {
  const d = new Date();
  document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}
</script>
```
{% endcode %}

### Ko'proq misol

[Yana bir oddiy vaqt](https://www-w3schools-com.translate.goog/js/tryit.asp?filename=tryjs\_timing2&\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)

[Vaqtni belgilash hodisasi bilan yaratilgan soat](https://www-w3schools-com.translate.goog/js/tryit.asp?filename=tryjs\_timing\_clock&\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)
