---
description: >-
  HTMLning class atributi HTML elementlarini sinflarga ajratish uchun
  ishlatiladi. Bir nechta elementlar bir xil class nomga ega bo'lishi mumkin.
---

# Klasslar

{% hint style="warning" %}
Class ni sinf deb atash o'zbek dasturchilar o'rtasida tarqalmagani va o'zbek auditoriyasida ham class deb tanilgani sababli mavzularni tarjima qilishda sinf so'zi ishlatimaydi.
{% endhint %}

## <mark style="color:green;">`class`</mark> <mark style="color:green;"></mark><mark style="color:green;">attributidan foydalanish</mark>

Class atributi ko'pincha CSS-da class nomini ko'rsatish uchun ishlatiladi. Bundan tashqari, u class-ga ega elementlarga JavaScript orqali tasir qilish va ularni boshqarish uchun ishlatilishi mumkin.

Quyida "<mark style="color:red;">`city`</mark>" nomli class atributlari mavjud bo'lgan 3ta <mark style="color:red;">`<div>`</mark> elementini  misol qilib keltirdik. Barcha 3-ta <mark style="color:red;">`<div>`</mark> elementlarining stillari <mark style="color:red;">`<head>`</mark> qismdagi <mark style="color:red;">`city`</mark> ga berilgan stillarga teng bo'ladi.

```html
<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  border: 2px solid black;
  margin: 20px;
  padding: 20px;
}
</style>
</head>
<body>

<div class="city">
  <h2>London</h2>
  <p>London is the capital of England.</p>
</div>

<div class="city">
  <h2>Paris</h2>
  <p>Paris is the capital of France.</p>
</div>

<div class="city">
  <h2>Tokyo</h2>
  <p>Tokyo is the capital of Japan.</p>
</div>

</body>
</html> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_classes_capitals" %}

Quyida "note" nomli class atributlari mavjud bo'lgan 2ta <mark style="color:red;">`<span>`</mark> elementini  misol qilib keltirdik. Barcha 2-ta <mark style="color:red;">`<span>`</mark> elementlarining stillari \<head> qismdagi <mark style="color:red;">`.note`</mark> ga berilgan stillarga teng bo'ladi.

```html
<!DOCTYPE html>
<html>
<head>
<style>
.note {
  font-size: 120%;
  color: red;
}
</style>
</head>
<body>

<h1>My <span class="note">Important</span> Heading</h1>
<p>This is some <span class="note">important</span> text.</p>

</body>
</html> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_classes_span" %}

{% hint style="warning" %}
**Maslahat:** <mark style="color:red;">`class`</mark> atributidan har qanday HTML elementida foydalanish mumkin.

**Eslatma:** Class nomi katta kichik harfga qarab farq qiladi

**Maslahat:** Bizning CSS o'quv qo'llanmamiz orqali CSS hqida ko'proq narsa o'rganishingiz mumkin
{% endhint %}

## <mark style="color:green;">Class uchun sintaksis</mark>

CSS orqali <mark style="color:red;">`class`</mark> ga murojaat qilish uchun (.) nuqtadan keyin **class nomini** yozing keyin jingalak {} qavslar ichida CSS xususiyatlarini berishingiz mumkin.

{% code title=""city" nomli class yaratish" %}
```html
<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
}
</style>
</head>
<body>

<h2 class="city">London</h2>
<p>London is the capital of England.</p>

<h2 class="city">Paris</h2>
<p>Paris is the capital of France.</p>

<h2 class="city">Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>

</body>
</html>
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_classes_css" %}

## <mark style="color:green;">Bir nechta classlar</mark>

HTML elementlari bir nechta classlarga ega bo'lishi mumkin.

Bir nechta class berish uchun class nomlarini bo'sh joy bilan ajratib yozing, misol uchun <mark style="color:red;">`<div class="city main">`</mark>. Element o'ziga berilgan barcha classlarga tegishli stillarni oladi.

Ushbu misoldagi bitinchi <mark style="color:red;">`<h2>`</mark> elementi <mark style="color:red;">`city`</mark> hamda <mark style="color:red;">`main`</mark> classlariga ega va u ikkala classga berilgan stillarni ham oladi:

```html
<h2 class="city main">London</h2>
<h2 class="city">Paris</h2>
<h2 class="city">Tokyo</h2>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_classes_multiple" %}

## <mark style="color:green;">Turli elementlar bir xil classga ega bo'la oladi</mark>

Ushbu misoldagi <mark style="color:red;">`<h2>`</mark> va <mark style="color:red;">`<p>`</mark> elementlari **"city"** nomli bir xil class-ga va bir xil stillga ega bo'lishadi:

```html
<h2 class="city">Paris</h2>
<p class="city">Paris is the capital of France</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_classes_tags" %}

## <mark style="color:green;">Javascriptda class atributidan foydalanish</mark>

Class nomlari JavaScript orqali ma'lum bir elementlar ustida turli vazifalarni amalga oshirish uchun ham ishlatilishi mumkin.

JavaScriptning <mark style="color:red;">`getElementsByClassName()`</mark> metodi orqali ma'lum bir classga ega elementlarga tasir o'tkazishi mumkin:

{% code title=""city" classiga ega barcha elementlarni yashirish uchun tugmani bosing:" %}
```html
<script>
function myFunction() {
  var x = document.getElementsByClassName("city");
  for (var i = 0; i < x.length; i++) {
    x[i].style.display = "none";
  }
}
</script> 
```
{% endcode %}

## Xulosa

* HTMLning <mark style="color:red;">`class`</mark> atributi element uchun bir yoki bir nechta class nomini belgilaydi
* Classlar CSS va Javascript orqali elementlarni tanlash va ularni boshqarish uchun ishlatiladi
* Istalgan HTML elementda <mark style="color:red;">`class`</mark> atributidan foydalanish mumkin
* Class nomi, harfning katta kichikligiga qarab farq qiladi
* Turli HTML elementlari bir xil class nomiga ega bo'lishi mumkin
* JavaScriptning <mark style="color:red;">`getElementsByClassName()`</mark> metodi orqali ma'lum bir classga ega elementlarga murojaat qilish mumkin
