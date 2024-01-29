---
description: >-
  <colgroup> elementi jadvalning alohida ustunlariga still berish uchun
  ishlatiladi.
---

# Jadval to'plami

## HTML jadvallar to'plami

Jadvalning birinchi ikkita ustuniga stil bermoqchi bo'lsangiz,`<colgroup>`va `<col>`elementlaridan foydalaning.

![](<../../../.gitbook/assets/image (211).png>)

\<colgroup> elementi o'ziga xos ustunlar uchun konteyner sifatida ishlatilishi kerak.

Har bir guruh element `<col>` bilan ifodalanadi.

span atributi, still nechta ustunga tasir qilsihi kerakligini belgilaydi.

style atributi ustunlarga still berishni ifodalaydi.

{% hint style="warning" %}

{% endhint %}

```
<table>
  <colgroup>
    <col span="2" style="background-color: #D6EEEE">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
... 
```

{% hint style="warning" %}
Eslatma: `<colgroup>` tegi \<table> elementining farzandi bo'lishi kerak va \<thead>, \<tr> \<td> va shu kabi boshqa jadval elementlaridan oldin joylashtirilishi kerak, ammo agar \<caption> elementi mavjud bo'lsa undan keyingina joylashtirish kerak.
{% endhint %}

## Foydalanish mumkin bo'lgan  CSS xususiyatlari

Colgrupda foydalanishga ruxsat berilgan CSS xususiyatlari juda kam:

`width` xususiyati\
`visibility` xususiyati\
`background` xususiyatlari\
`border` xususiyatlari

Bulardan boshqa xarqanday CSS xususiyatlari jadvalingizga tasir qilmaydi.

## Bir nechta Col elementi

Agar siz turlicha stilga ega ko'plab ustunlar yaratmoqchi bo'lsangiz, \<colgroup> elementi ichida ko'proq  `<col>`  elementlaridan foydalaning:

```
<table>
  <colgroup>
    <col span="2" style="background-color: #D6EEEE">
    <col span="3" style="background-color: pink">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
... 
```

## Bo'm bo'sh colgrouplar

Jadvalning o'rtasidagi ustunlarga still berishni xoxlasangiz jadvalning o'rtasigacha bo'lgan  ustunlar uchun "bo'sh" \<col> elementini (xech qanday stillarsiz) bering:

```
<table>
  <colgroup>
    <col span="3">
    <col span="2" style="background-color: pink">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
...
```

## Ustunlarni yashirish

CSSning `visibility: collapse` xususiyati orqali ustunlaringizni yashirishingiz ham mumkin:

```
<table>
  <colgroup>
    <col span="2">
    <col span="3" style="visibility: collapse">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
...
```

