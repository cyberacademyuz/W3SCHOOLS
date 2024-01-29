---
description: Orqa fon rasmlar deyarli har qanday HTML elementlari uchun berilishi mumkin.
---

# Orqafon rasmlar

## HTML elementining orqafon rasmi

HTML elementiga orqa fon rasm berish uchun HTMLning `style` attributidan va CSSning `background-img` xususiyatidan foydalaniladi:

{% code title="Elementga orqa fon rasm qo'shish" %}
```
<p style="background-image: url('img_girl.jpg');"> 
```
{% endcode %}

Bundan tashqari, `<head>` qismida `<style>` elementi ichida berishingiz ham mumkin:

{% code title="<style> elementi bilan orqa fon rasm berish:" %}
```
<style>
p {
  background-image: url('img_girl.jpg');
}
</style> 
```
{% endcode %}

## Sahifaning orqafon rasmi

Agar butun sahifaning orqafoniga rasm qo'yishni hohlsangiz, rasmni `<body>` elementiga berishingiz kerak:

{% code title="Butun sahifa uchun orqafon rasm qo'shish:" %}
```
<style>
body {
  background-image: url('img_girl.jpg');
}
</style> 
```
{% endcode %}

## Background repeat

Agar rasm elementdan kichik bo'lsa, u elementning ohiriga borguncha gorizontal va vertikal shaklda takrorlanaveradi.

<figure><img src="../../../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure>

```
<style>
body {
  background-image: url('example_img_girl.jpg');
}
</style>
```

Orqafon rasm takrorlanmasligi uchun `background-repeat` xususiyatiga `no-repeat` qiymatini bering.

```
<style>
body {
  background-image: url('example_img_girl.jpg');
  background-repeat: no-repeat;
}
</style> 
```

## Background Cover

Agar orqafon rasmi butun elementni qamrab olishini istasangiz, `background-size` xususiyatiga `cover` qiymatini berishingiz mumkin.

Bundan tashqari, butun element har doim qamrab olingan holatda ekanligiga ishonchingiz komil bo'lishi uchun `background-attachment`xususiyatiga fixed qiymatini bering.

Shunday qilib, orqafon rasmi cho'zilmasdan butun elementni qamrab oladi (rasm asl holatini saqlab qoladi):

```
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
</style>
```

## Background Stretch

Agar fon rasmi butun elementga mos turishini xohlasangiz, `background-size` xususiyatiga  `100% 100%` qiymatlarini berishingiz mumkin.

<figure><img src="../../../.gitbook/assets/image (312).png" alt=""><figcaption></figcaption></figure>

Brauzer oynasining o'lchamini o'zgartirib ko'ring va rasmning cho'zilayotganiga guvoh bo'lasiz, lekin u har doim butun elementni qamrab turadi.

```
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 100% 100%;
}
</style>
```
