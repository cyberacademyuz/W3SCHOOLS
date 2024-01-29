---
description: >-
  HTMLning id atributi element uchun takrorlanmas identifikator berish uchun
  ishlatiladi. HTMLda bir xil id-ega ega bir nechta elementdan foydalana
  olmaysiz.
---

# ID

## Id atributidan foydalanish

`id` attributi HTML elementlariga takrorlanmas id berish uchun ishlatiladi. Id atributining qiymati HTMLda bitta bo'lishi kerak.

Id atributi CSS orqali maxsus stillarni berish uchun ishlatiladi. Bundan tashqari ma'lum id-ga ega elementga JavaScript orqali murojaat qilish va uni  boshqarish uchun ishlatilishi mumkin.

Id ning sintaksisi: CSS orqali id ga murojaat qilish uchun (#) panjara belgisidan keyin id nomini yozing, keyin jingalak {} qavslar ichida CSS xususiyatlarini berishingiz mumkin.

Quyidagi misolda "**myHeader**" nomli id-ga ega `<h1>` elementi bor. Ushbu `<h1>` elementi `<header>` qismdagi **#myHeader** ga berilgan stillar bilan o'zgaradi.

```
<!DOCTYPE html>
<html>
<head>
<style>
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
}
</style>
</head>
<body>

<h1 id="myHeader">My Header</h1>

</body>
</html> 
```

{% hint style="warning" %}
**Eslatma**: id nomi katta kichik harflarga qarab farq qiladi

**Eslatma**: Id nomi kamida bitta belgidan iborat boʻlishi, raqam bilan boshlanmasligi va unda bo'sh joylar boʻlmasligi kerak.
{% endhint %}

## Class va ID o'rtasidagi farq

Class nomlari bir nechta HTML elementlarda qo'llanilishi mumkin ammo id esa sahifadagi faqat bitta HTML elementi tomonidan ishlatilishi kerak:

```
<style>
/* Style the element with the id "myHeader" */
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
}

/* Style all elements with the class name "city" */
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
}
</style>

<!-- An element with a unique id -->
<h1 id="myHeader">My Cities</h1>

<!-- Multiple elements with same class -->
<h2 class="city">London</h2>
<p>London is the capital of England.</p>

<h2 class="city">Paris</h2>
<p>Paris is the capital of France.</p>

<h2 class="city">Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>
```

## ID yordamida bookmarklar va havolalar

HTMLda bookmarklardan, foydalanuvchilarga veb-sahifaning muayyan qismlariga o'tish imkonini berish uchun foydalaniladi.

Agar sahifangiz juda uzun bo'lsa, bookmarklar sizga foyda berishi mumkin.

Bookmarkdan foydalanish uchun avval uni yaratishingiz, so‘ngra unga havola qo‘shishingiz kerak.

So'ngra, havola bosilganida sahifa bookmark joylashgan joyga o'tadi.

## Misol

Birinchi navbatda `id` attributi yordamida bookmark yarating:

```
<h2 id="C4">Chapter 4</h2>
```

Keyin, xuddi shu sahifadan bookmarkga o'tuvchi ("4-bo'limga o'tish") havola qo'shing:

{% code title="Misol" %}
```
<a href="#C4">Jump to Chapter 4</a>
```
{% endcode %}

Bundan tashqari, boshqa sahifadagi bookmarkga o'tuvchi havola ham qo'shishingiz mumkin:

```
<a href="html_demo.html#C4">Jump to Chapter 4</a>
```

## JavaScript-da id atributidan foydalanish

`id` atributi JavaScript orqali ma'lum bir elementlar ustida turli vazifalarni amalga oshirish uchun ishlatilishi mumkin.

JavaScriptning `getElementsById()` metodi orqali ma'lum bir id-ga ega elementga ta'sir o'tkazish mumkin:

{% code title="JavaScript orqali matnni boshqarish uchun id atributidan foydalaning:" %}
```
<script>
function displayResult() {
  document.getElementById("myHeader").innerHTML = "Have a nice day!";
}
</script> 
```
{% endcode %}

## Xulosa

* id atributidan elementga takrorlanmas identifikator berish uchun foydalaniladi
* Id atributining qiymati HTMLda bitta bo'lishi kerak.
* Id atributi CSS va JavaScript orqali biror elementni tanlash yoki unga still berish uchun ishlatiladi
* &#x20;id atributining nomi katta kichik harflarga qarab farq qiladi
* id attributi orqali HTMLda bookmarklar yaratish ham mumkin
* JavaScriptning `getElementsById()` metodi orqali id-ga ega elementga ta'sir o'tkazish mumkin
