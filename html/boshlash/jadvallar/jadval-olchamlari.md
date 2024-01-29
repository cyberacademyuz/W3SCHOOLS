---
description: >-
  HTML jadvallarida har bir ustun, qator yoki butun jadval turli o'lchamlarga
  ega bo'lishi mumkin.
---

# Jadval o'lchamlari

<figure><img src="../../../.gitbook/assets/image (292).png" alt=""><figcaption></figcaption></figure>

Jadval, qator yoki ustun o'lchamlarini berish uchun width yoki height xususiyatlariga ega style attributidan foydalaning.

## HTMLda jadval endi

Jadvalning enini berish uchun \<table> elementiga style attributini qo'shing:

{% code title="Jadval enini 100% qiling:" %}
```
<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table> 
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** En o'lchamini belgilash uchun foizdan foydalanish bu elementning ota elementi bo'lgan elementning o'lchamiga nisbatan taqqoslanishini bildiradi, hozirgi holatda \<table>ning ota elementi \<body> hisoblanadi.
{% endhint %}

## HTML jadvalidagi ustunning kengligi

![](<../../../.gitbook/assets/image (338).png>)

Ma'lum bir ustunga o'lcham berish uchun \<th> va \<td> elementlariga style attributini qo'shing:

{% code title="Birinchi ustunning kengligini 70% qiling::" %}
```
<table style="width:100%">
  <tr>
    <th style="width:70%">Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>
```
{% endcode %}

## HTML jadvalidagi qator balandligi

![](<../../../.gitbook/assets/image (771).png>)

Ma'lum bir qatorning balandligini belgilash uchun \<tr> elementiga style attributini qo'shing:

{% code title="Ikkinchi qatorning balandligini 200 piksel qilib belgilang:" %}
```
<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr style="height:200px">
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>
```
{% endcode %}

