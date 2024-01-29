---
description: >-
  HTML ranglari rang nomlari yoki RGB, HEX, HSL, RGBA va HSLA qiymatlari bilan
  ifodalanadi.
---

# Ranglar

## Rang nomlari

HTMLda rangni uning nomi bilan belgilash mumkin.

<figure><img src="../../../.gitbook/assets/image (322).png" alt=""><figcaption><p>HTML 140 ta standart rang nomlarini qo''llab quvvatlaydi</p></figcaption></figure>

## Orqa fon ranggi

Siz HTML elementi uchun orqa fon rangini belgilashingiz mumkin.

&#x20;                                                                          <mark style="background-color:blue;">SALOM DUNYO</mark>                                                                          &#x20;

<mark style="background-color:red;">Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</mark>

```
<h1 style="background-color:DodgerBlue;">Hello World</h1>
<p style="background-color:Tomato;">Lorem ipsum...</p>
```

## Matn ranggi

Siz matnning ranggini belgilashingiz mumkin:

<mark style="color:red;">SALOM DUNYO</mark>

<mark style="color:blue;">Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</mark>

<mark style="color:green;">Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</mark>

```
<h1 style="color:Tomato;">Hello World</h1>
<p style="color:DodgerBlue;">Lorem ipsum...</p>
<p style="color:MediumSeaGreen;">Ut wisi enim...</p>
```

## Chegara ranggi

Chegaralar rangini belgilashingiz mumkin:

<figure><img src="../../../.gitbook/assets/image (320).png" alt=""><figcaption></figcaption></figure>

```
<h1 style="border:2px solid Tomato;">Hello World</h1>
<h1 style="border:2px solid DodgerBlue;">Hello World</h1>
<h1 style="border:2px solid Violet;">Hello World</h1>
```

## Rang qiymatlari

HTMLda ranglar RGB, HEX, HSL, RGBA va HSLA qiymatlari yordamida ham belgilanishi mumkin.

Quyidagi uchta `<div>` elementi RGB, HEX va HSL qiymatlari bilan berilgan fon rangiga ega:

<figure><img src="../../../.gitbook/assets/image (323).png" alt=""><figcaption></figcaption></figure>

Quyidagi ikkita \<div> elementining fon rangi RGBA va HSLA qiymatlari bilan berilgan boʻlib, ular rangga Alfa xususiyatini qoʻshadi (bu yerda 50% shaffoflik mavjud):

<figure><img src="../../../.gitbook/assets/image (362).png" alt=""><figcaption></figcaption></figure>

```
<h1 style="background-color:rgb(255, 99, 71);">...</h1>
<h1 style="background-color:#ff6347;">...</h1>
<h1 style="background-color:hsl(9, 100%, 64%);">...</h1>

<h1 style="background-color:rgba(255, 99, 71, 0.5);">...</h1>
<h1 style="background-color:hsla(9, 100%, 64%, 0.5);">...</h1>
```
