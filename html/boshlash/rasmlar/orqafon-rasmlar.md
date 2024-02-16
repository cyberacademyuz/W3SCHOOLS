---
description: Orqa fon rasmlar deyarli har qanday HTML elementlari uchun berilishi mumkin.
---

# Orqafon rasmlar

## <mark style="color:green;">HTML elementining orqafon rasmi</mark>

HTML elementiga orqa fon rasm berish uchun HTMLning <mark style="color:red;">`style`</mark> attributidan va CSSning <mark style="color:red;">`background-img`</mark> xususiyatidan foydalaniladi:

{% code title="Elementga orqa fon rasm qo'shish" %}
```html
<p style="background-image: url('img_girl.jpg');"> 
```
{% endcode %}

Bundan tashqari, <mark style="color:red;">`<head>`</mark> qismida <mark style="color:red;">`<style>`</mark> elementi ichida berishingiz ham mumkin:

{% code title="<style> elementi bilan orqa fon rasm berish:" %}
```html
<style>
p {
  background-image: url('img_girl.jpg');
}
</style> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_background4" %}

## <mark style="color:green;">Sahifaning orqafon rasmi</mark>

Agar butun sahifaning orqafoniga rasm qo'yishni hohlsangiz, rasmni <mark style="color:red;">`<body>`</mark> elementiga berishingiz kerak:

{% code title="Butun sahifa uchun orqafon rasm qo'shish:" %}
```html
<style>
body {
  background-image: url('img_girl.jpg');
}
</style> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_background5" %}

## <mark style="color:green;">Background repeat</mark>

Agar rasm elementdan kichik bo'lsa, u elementning ohiriga borguncha gorizontal va vertikal shaklda takrorlanaveradi.

<figure><img src="../../../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure>

```html
<style>
body {
  background-image: url('example_img_girl.jpg');
}
</style>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_background6" %}

Orqafon rasm takrorlanmasligi uchun <mark style="color:red;">`background-repeat`</mark> xususiyatiga <mark style="color:red;">`no-repeat`</mark> qiymatini bering.

```html
<style>
body {
  background-image: url('example_img_girl.jpg');
  background-repeat: no-repeat;
}
</style> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_background6_1" %}

## <mark style="color:green;">Background cover</mark>

Agar orqafon rasmi butun elementni qamrab olishini istasangiz, <mark style="color:red;">`background-size`</mark> xususiyatiga <mark style="color:red;">`cover`</mark> qiymatini berishingiz mumkin.

Bundan tashqari, butun element har doim qamrab olingan holatda ekanligiga ishonchingiz komil bo'lishi uchun <mark style="color:red;">`background-attachment`</mark>xususiyatiga <mark style="color:red;">`fixed`</mark> qiymatini bering.

Shunday qilib, orqafon rasmi cho'ziln ketmasdan butun elementni qamrab oladi (rasm asl holatini saqlab qoladi):

```html
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
</style>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_background7" %}

## <mark style="color:green;">Background Stretch</mark>

Agar fon rasmi butun elementga mos turishini xohlasangiz, <mark style="color:red;">`background-size`</mark> xususiyatiga  <mark style="color:red;">`100% 100%`</mark> qiymatlarini berishingiz mumkin.

<figure><img src="../../../.gitbook/assets/image (312).png" alt=""><figcaption></figcaption></figure>

Brauzer oynasining o'lchamini o'zgartirib ko'ring va rasmning cho'zilayotganiga guvoh bo'lasiz, lekin u har doim butun elementni qamrab turadi.

```html
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 100% 100%;
}
</style>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_background8" %}
