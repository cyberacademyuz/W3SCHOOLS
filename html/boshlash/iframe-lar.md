---
description: >-
  HTMLning iframe-lari veb sahifa ichida boshqa bir veb sahifani ko'rsatish
  uchun ishlatiladi
---

# Iframe-lar

<figure><img src="../../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

## Iframe sintaksisi

HTMLning \<iframe> tegi inline ramka yaratadi.

Joriy sahifaga boshqa sahifani joylashtirish uchun inline ramka ishlatiladi.

{% code title="Sintaksis" %}
```
<iframe src="url" title="description"></iframe> 
```
{% endcode %}

Maslahat: \<iframe> elementi uchun title atributini berib ketish **good practice** hisoblanadi. Bu ekranni o'qib beruchi dasturlar tomonidan iframe nima haqida ekanligini o'qish uchun ishlatiladi.

## Iframe - kenglik va balanlikni berish

Iramega o'lcham berish uchun heighr va width atributlaridan foydalaning.

Width va height standart tarzda pikselda bo'ladi.

```
 <iframe src="demo_iframe.htm" height="200" width="300" title="Iframe Example"></iframe> 
```

Yoki siz style atributini qo'shishingiz va CSSning width va height xususiyatlaridan foydalanishingiz mumkin:

```
 <iframe src="demo_iframe.htm" style="height:200px;width:300px;" title="Iframe Example"></iframe> 
```

## Iframe - chegara chizig'i (border) ni olib tashlash

Standart holatda iframening chega chizig'i bo'ladi.

Uni olib tashlash uchun style atributini qo'shing va CSSning width va height xususiyatlaridan foydalaning:

```
<iframe src="demo_iframe.htm" style="border:none;" title="Iframe Example"></iframe> 
```

CSS orqali uning o'lchamini, stillarini va chegara chizig'ining ranglarini o'zgartira olasiz.

```
<iframe src="demo_iframe.htm" style="border:2px solid red;" title="Iframe Example"></iframe> 
```

## Iframe - Havola uchun target

Iframedan havolalar uchun ramka sifatida foydalanish mumkin.

Havolaning target atributi iframening name atributi bilan bo'glanishi qilishi kerak:

```
<iframe src="demo_iframe.htm" name="iframe_a" title="Iframe Example"></iframe>

<p><a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a></p>
```

## Xulosa

* HTMLning \<iframe> elementi inline ramka yaratadi
* src atributi ramkaga joylashtiriladigan sahifaning URL manzilini qabul qiladi
* Har doim title atributini qo'shing (ekranni o'quvchi dasturlar uchun)
* Iframening o'lchamini berish uchun width va height attributlaridan foydalaning
* Iframe atrofidagi chegara chiziqlarini olib tashlash uchun CSSning `border:none;` xususiyatidan foydalaning

### HTML iframe tegi

| Teg       | Ta'rif                 |
| --------- | ---------------------- |
| \<iframe> | Inline iframe yaratadi |
