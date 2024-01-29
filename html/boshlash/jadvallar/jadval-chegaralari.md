---
description: HTML jadvallariga turli stil va shakldagi chegaralar berish mumkin.
---

# Jadval chegaralari

## Chegara qanday beriladi

Jadvalga chegara qo'shganingizda, har bir jadval katakchasining atrofida chegaralar ham qo'shgan bo'lasiz:

![](<../../../.gitbook/assets/image (324).png>)

Chegara qo'shish uchun, table, th va td elementlariga CSSning border xususiyatidan foydalaning.

```
table, th, td {
  border: 1px solid black;
}
```

## Collapsed jadaval chegaralari

Jadvallar yuqoridagi misoldek ikkitalik chegaralarga ega bo'lmasligi uchun CSSning `border-collapse`xususiyatiga `collapse` qiymatini bering.

Bu chegaralarni bittalik chegaraga aylantiradi:

![](<../../../.gitbook/assets/image (317).png>)

```
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
```

## Jadvallarga stil berish



![](<../../../.gitbook/assets/image (302).png>)

```
table, th, td {
  border: 1px solid white;
  border-collapse: collapse;
}
th, td {
  background-color: #96D4D4;
}
```

## Jadvalning aylana chegaralari

border-radius xususiyati yordamida chegaralar yumaloq burchaklarga ega bo'ladi:

![](<../../../.gitbook/assets/image (333).png>)

```
table, th, td {
  border: 1px solid black;
  border-radius: 10px;
}
```

CSS selektoridan **table**ni olib tashlab, jadval atrofidagi chegarani ham olib tashlang:

```
th, td {
  border: 1px solid black;
  border-radius: 10px;
}
```

## Nuqtali jadval chegaralari

border-style xususiyati bilan chegara ko'rinishini o'zgartirishingiz mumkin:

![](<../../../.gitbook/assets/image (295).png>)

border-styleda quyidagi qiymatlar mavjud:

* `dotted`    &#x20;
* `dashed`    &#x20;
* `solid`    &#x20;
* `double`    &#x20;
* `groove`    &#x20;
* `ridge`    &#x20;
* `inset`    &#x20;
* `outset`    &#x20;
* `none`    &#x20;
* `hidden`  &#x20;

```
th, td {
  border-style: dotted;
}
```

## Chegara ranggi

`border-color` xususiyati yordamida chegara ranglarini berishingiz mumkin:

```
th, td {
  border-color: #96D4D4;
}
```
