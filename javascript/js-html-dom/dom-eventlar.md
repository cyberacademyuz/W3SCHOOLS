# DOM Eventlar

HTML DOM JavaScript-ga HTML hodisalariga munosabat bildirish imkonini beradi:

<figure><img src="../../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

### Hodisalarga munosabat bildirish

Foydalanuvchi HTML elementini bosishi kabi biror hodisa sodir bo'lganida ma'lum bir javascript kod bajarilishini belgilash mumkin.

Foydalanuvchi elementni bosganida kodni bajarish uchun HTMLning hodisa atributiga JavaScript kodini qo‘shing:

```
onclick=JavaScript
```

HTML hodisalariga misollar:

* Foydalanuvchi sichqonchani bosganda
* Veb-sahifa yuklanganda
* Rasm yuklanganda
* Sichqoncha element ustida harakat qilganda
* Input maydoni o'zgartirilganda
* HTML forma yuborilganda
* Foydalanuvchi kalitni bosganda

Ushbu misolda foydalanuvchi matnni bosganida `<h1>` elementining tarkibi o'zgaradi:

```
<!DOCTYPE html>
<html>
<body>

<h1 onclick="this.innerHTML = 'Ooops!'">Click on this text!</h1>

</body>
</html>
```

Ushbu misolda funksiya hodisa boshqaruvchisidan chaqiriladi:

```
<!DOCTYPE html>
<html>
<body>

<h1 onclick="changeText(this)">Click on this text!</h1>

<script>
function changeText(id) {
  id.innerHTML = "Ooops!";
}
</script>

</body>
</html>
```

### HTML hodisa atributlari

Hodisalarni HTML elementlariga belgilash uchun hodisa atributlaridan foydalanishingiz mumkin.

{% code title="Onclick hodisasini button elementiga tayinlang:" %}
```
<button onclick="displayDate()">Try it</button>
```
{% endcode %}

Yuqoridagi misolda tugma bosilganda `displayDate` nomli funksiya bajariladi.

### HTML DOM yordamida hodisalarni tayinlash

HTML DOM JavaScript yordamida HTML elementlariga hodisalarni belgilash imkonini beradi:

{% code title="Onclick hodisasini button elementiga tayinlash:" %}
```
<script>
document.getElementById("myBtn").onclick = displayDate;
</script>
```
{% endcode %}

Yuqoridagi misolda `id="myBtn"` orqali elementga `displayDate` nomli funksiya tayinlangan.

Tugma bosilganda funksiya ishga tushadi.

### onload va onunload hodisalari

`onload` va `onunload` hodisalari foydalanuvchi sahifaga kirganda yoki undan chiqqanda ishga tushadi.

`onload` hodisasi saytga tashrif buyuruvchining brauzer turini va brauzer versiyasini tekshirish va ma'lumotlar asosida veb-sahifaning tegishli versiyasini yuklash uchun ishlatilishi mumkin.

`onload` va `onunload` hodisalari cookie fayllar bilan ishlash uchun ishlatilishi mumkin.

```
<body onload="checkCookies()">
```

### Onchange hodisasi

`onchange` hodisasi ko'pincha input maydonlarini tekshirish bilan birgalikda ishlatiladi.

Quyida onchange dan qanday foydalanishga misol keltirilgan. `upperCase()` funktsiyasi foydalanuvchi input maydonining tarkibini o'zgartirganda chaqiriladi.

```
<input type="text" id="fname" onchange="upperCase()">
```

### Onmouseover va onmouseout hodisalari

`onmouseover` va `onmouseout` hodisalari foydalanuvchi sichqonchani HTML elementi ustiga olib kelganida yoki undan tashqariga surganida biror bir funksiyani ishga tushirish uchun ishlatilishi mumkin:

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

### onmousedown, onmouseup va onclick hodisalari

`onmousedown`, `onmouseup` va `onclick` hodisalari sichqonchani bosishning barcha usullari hisoblanadi. Avval sichqoncha tugmasi bosilganda `onmousedown` hodisasi ishga tushadi, so'ngra sichqoncha tugmasi qo'yib yuborilganda `onmouseup` hodisasi ishga tushadi, nihoyat, sichqonchani bosish tugagach, `onclick` hodisasi ishga tushadi.

### Ko'proq misol

[onmousedown va onmouseup](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_event\_onmousedown)\
Foydalanuvchi sichqoncha tugmasini bosib turganda tasvirni o'zgartirish.

[onload](https://www-w3schools-com.translate.goog/js/tryit.asp?filename=tryjs\_event\_onload&\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)\
Sahifani yuklash tugagach, ogohlantirish oynasini ko'rsatish.

[onfocus](https://www-w3schools-com.translate.goog/js/tryit.asp?filename=tryjs\_event\_onfocus&\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)\
Input maydoni diqqat markazida bo'lganda uning fon rangini o'zgartirish.

[Sichqoncha hodisalari](https://www-w3schools-com.translate.goog/js/tryit.asp?filename=tryjs\_event\_onmouse&\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)\
Kursor element ustida harakat qilganda uning rangini o'zgartirish.

### HTML DOM hodisasi obyektiga havola

Barcha HTML DOM hodisalarining roʻyxatini koʻrish uchun bizning HTML DOM hodisa obyekti haqida maʼlumotnoma sahifamizga o'ting.
