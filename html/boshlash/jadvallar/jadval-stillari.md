---
description: Jadvallaringizni yaxshiroq qilish uchun CSS-dan foydalaning.
---

# Jadval stillari

## HTML jadvali - Zebra chiziqlari

Agar siz har bir qatordan keyingi qatorga fon rangini bersangiz zebra chiziqlari effektini hosil qilasiz.

![](<../../../.gitbook/assets/image (2).png>)

Har bir qatordan keyingi qator elementiga still berish uchun :nth-child(even) selektoridan quyidagi tarzda foydalaning:

```
tr:nth-child(even) {
  background-color: #D6EEEE;
}
```

{% hint style="warning" %}
**Eslatma**: Agar (even) o'rniga (odd) dan foydalansangiz, stillar 2,4,6 va boshqa juft qatorlar o'rniga 1,3,5 va boshqa toq qatorlarga tasir qiladi.
{% endhint %}

## HTML jadval - Vertikal zebra chiziqlari

Vertikal zebra chiziqlarini yasash uchun har bir ustundan keyingi ustunga still bering:

Jadvaldagi ma'lumotlarining elementlari uchun :nth-child(even) xususiyatini quyidagi tarzda bering:

```
td:nth-child(even), th:nth-child(even) {
  background-color: #D6EEEE;
}
```

{% hint style="warning" %}
Eslatma: Sarlavhalar va oddiy jadval kataklariga still berishni hohlasangiz :nth-child() selektorini th va td elementlarining ikkalasiga ham bering.
{% endhint %}

## Vertikal va gorizontal zebra chiziqlarini aralashtirish

Yuqoridagi ikkita misoldagi stillarni birlashtirishingiz mumkin va har bir qatordan keyingi qatorda va har bir ustundan keyin ustunda chiziqlar paydo bo'ladi.

Agar shaffof rangdan foydalansangiz, ranglar bir-birining ustiga chiqib olganligini ko'rastuvchi effekt hosil qilasiz.

![](<../../../.gitbook/assets/image (45).png>)

Rangning shaffoflik darajasini belgilash uchun rgba() rangidan foydalaning:

```
tr:nth-child(even) {
  background-color: rgba(150, 212, 212, 0.4);
}

th:nth-child(even),td:nth-child(even) {
  background-color: rgba(150, 212, 212, 0.4);
}
```

## Gorizontal ajratgichlar

<figure><img src="../../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

Agar chegaralarni har bir qatorining pastki qismigagina bersangiz, gorizontal bo'linuvchi jadvalga hosil qilasiz.

Gorizontal ajratgichlarni hozil qilish uchun barcha tr elementlariga `border-bottom` xususiyatini bering.

```
tr {
  border-bottom: 1px solid #ddd;
}
```

## Hoverli jadval

Jadval qatorlariga sichqoncha olib borilganida qatorlarini ajratib ko'rsatish uchun tr elementining :hover selektoridan foydalaning:

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

{% code title="Misol:" %}
```
tr:hover {background-color: #D6EEEE;} 
```
{% endcode %}

