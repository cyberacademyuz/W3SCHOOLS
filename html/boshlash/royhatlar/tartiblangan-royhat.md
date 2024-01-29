---
description: >-
  HTMLning <ol> tegi tartiblangan ro'yhat yaratadi. Tartiblangan ro'yhatlar
  tartib raqamlarga ega bo'ladi.
---

# Tartiblangan ro'yhat

## Tartiblangan ro'yhat

Tartiblangan ro'yhatlar `<ol>` tegi bialn boshlanadi. Ro'yhatning har bir elementi `<li>` tegi ichida bo'ladi.

Ro'yhatning har bir elementining oldida tartib raqami bo'ladi.

```
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```

## Tartiblangan ro'yhat - type attributi

`<ol>` tegining `type` attributi ro'yhat elementlaridagi belgi turini o'zgartiradi.

| Turi     | Tarif                                                      |
| -------- | ---------------------------------------------------------- |
| type="1" | Ro'yxat elementlari raqamlar bilan tartibanadi (standart)  |
| type="A" | Ro'yxat elementlari katta harflar bilan tartiblanadi       |
| type="a" | Ro'yxat elementlari kichik harflar bilan tartiblanadi      |
| type="I" | Ro'yxat elementlari katta rim raqamlari bilan tartiblanadi |
| type="i" | Ro'yxat elementlari kichik rim raqamlari bilan raqamlanadi |

{% code title="Raqamlar" %}
```
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% code title="Katta harflar" %}
```
<ol type="A">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% code title="Kichik harflar" %}
```
<ol type="a">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% code title="Katta rim raqamlari" %}
```
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% code title="Kichik rim aqamlari" %}
```
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

## Ro'yhatdagi sanoq tartibini boshqarish

Standart holatda tartiblangan raqamlar tartibi 1 raqamidan boshlanadi. Agar siz bu sanoqni o'zingiz istagan biror sondan boshlanishini hohlasangiz start attributidan foydalanishingiz mumkin.

```
<ol start="50">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```

## HTMLdagi ichki ro'yhatlar

Ro'yhatlar ichma ich ham bo'lishi mumkin (ro'yhat ichida ro'yhat)

```
<ol>
  <li>Coffee</li>
  <li>Tea
    <ol>
      <li>Black tea</li>
      <li>Green tea</li>
    </ol>
  </li>
  <li>Milk</li>
</ol> 
```

{% hint style="warning" %}
**Eslatma**: Roʻyxat elementi ( `<li>`) yangi roʻyxatni hamda rasmlar va havolalar kabi boshqa HTML elementlarini ham oʻz ichiga olishi mumkin.
{% endhint %}

## Bo'lim xulosasi

* Tartiblangan ro'yhat yaratish uchun \<ol> elementidan foydalaning
* Tartiblanish turini belgilash uchun type attributidan foydalaning
* Ro'yhat elementlarini yaratish uchun \<li> elementidan foydalaning
* Ro;yhatlar ichma ich bo'lishi mumkin
* Ro'yhatlar boshqa HTML elementlarini ham o'z ichiga olishi mumkin

| Teg   | Tarif                                            |
| ----- | ------------------------------------------------ |
| \<ul> | Tartiblanmagan ro'yhat yaratadi                  |
| \<ol> | Tartiblangan ro'yhat yaratadi                    |
| \<li> | Ro'yhat elementlarini belgilaydi                 |
| \<dl> | Tariflar ro'yhatini belgilaydi                   |
| \<dt> | Ta'riflar ro'yxatidagi atamani belgilaydi        |
| \<dd> | Ta'riflar ro'yxatidagi atama tarifini belgilaydi |
