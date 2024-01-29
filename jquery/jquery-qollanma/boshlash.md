---
description: jQuery boshladik
---

# Boshlash

### jQueryni web sahifangizga ulash <a href="#jqueryni-web-sahifangizga-ulash" id="jqueryni-web-sahifangizga-ulash"></a>

jQuery ni web sahifangizga ulashning bir qancha usullari mavjud:

* jQuery.com saytidan kutubxonani yuklab olish orqali
* jQueryni CDN yordamida sahifangizga ulash orqali

### jQueryni yuklab olish <a href="#jqueryni-yuklab-olish" id="jqueryni-yuklab-olish"></a>

Yuklab olish uchun jQueryning ikki xil versiyasi mavjud:

* **Production** versiyasi - bu web sahifangiz uchun chunki bu versiya minified qilingan va kompresslangan.
* **Development** versiyasi - bu test uchun va ishlab chiqarish uchun (kompreslanmagan va o'qishga oson bo'lgan kod)

Ikkala versiya ham jQuery.com saytida mavjud.

jQuery kutubxonasi birgina faylning o'zi va uni HTML ga `<script>` tegi orqali ulashingiz mumkin (esda tutingki `<script>` tegi `<head>` tegi orasida yozilishi kerak):

```
<head>
<script src="jquery-3.6.0.min.js"></script>
</head>
```

**Maslahat:** jQuery fayllarini va siz ishlamoqchi bo'lgan sahifaning fayllarini bitta direktoriyada qilishga harakat qiling.

### jQuery CDN <a href="#jquery-cdn" id="jquery-cdn"></a>

Agar jQuery fayllarini lokal holatda ishlatishni xohlamasangiz, unda uning CDN (Content Delivery Network) idan foydalanishingiz mumkin.

Bunga misol qilib Google ni keltirishimiz mumkin:

#### Google CDN: <a href="#google-cdn" id="google-cdn"></a>

```
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
</head> 
```

{% hint style="info" %}
**Google ga yuklangan jQuery dan foydalnishning eng katta foydali tomoni:**

Ko'plab foydalanuvchilar boshqa saytga tashrif buyurishayotgan vaqtda allaqachon Google ga yuklangan jQuery yuklab olishgan bo'lishadi. Natijada, saytga tashrif buyurilayotgan vaqtda jQuery keshdan yuklanadi va saytga tezroq kiradi. Shuningdek, ko'plab CDN lar foydalanuvchining joylashuviga qarab fayllarni qaysi serverdan yuklanishi kerakligini belgilaydi.
{% endhint %}
