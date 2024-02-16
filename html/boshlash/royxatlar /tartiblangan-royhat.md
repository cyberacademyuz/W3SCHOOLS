---
description: >-
  HTMLning <ol> tegi tartiblangan ro'yhat yaratadi. Tartiblangan ro'yhatlar
  tartib raqamlarga ega bo'ladi.
---

# Tartiblangan ro'yhat

## <mark style="color:green;">Tartiblangan ro'yxat</mark>

Tartiblangan ro'yxatlar <mark style="color:red;">`<ol>`</mark> tegi bilan boshlanadi. Ro'yxatning har bir elementi <mark style="color:red;">`<li>`</mark> tegi ichida bo'ladi.

Ro'yhatning har bir elementining oldida tartib raqami bo'ladi.

```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_ordered2" %}

## <mark style="color:green;">Tartiblangan ro'yhat -</mark> <mark style="color:green;"></mark><mark style="color:green;">`type`</mark> <mark style="color:green;"></mark><mark style="color:green;">attributi</mark>

<mark style="color:red;">`<ol>`</mark> tegining <mark style="color:red;">`type`</mark> attributi ro'yhat elementlaridagi belgi turini o'zgartiradi.

| Turi     | Tarif                                                      |
| -------- | ---------------------------------------------------------- |
| type="1" | Ro'yxat elementlari raqamlar bilan tartibanadi (standart)  |
| type="A" | Ro'yxat elementlari katta harflar bilan tartiblanadi       |
| type="a" | Ro'yxat elementlari kichik harflar bilan tartiblanadi      |
| type="I" | Ro'yxat elementlari katta rim raqamlari bilan tartiblanadi |
| type="i" | Ro'yxat elementlari kichik rim raqamlari bilan raqamlanadi |

{% code title="Raqamlar" %}
```html
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_ordered_numbers" %}

{% code title="Katta harflar" %}
```html
<ol type="A">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_ordered_ucase" %}

{% code title="Kichik harflar" %}
```html
<ol type="a">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_ordered_lcase" %}

{% code title="Katta rim raqamlari" %}
```html
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_ordered_roman_ucase" %}

{% code title="Kichik rim aqamlari" %}
```html
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_ordered_roman_lcase" %}

## <mark style="color:green;">Ro'yhatdagi sanoq tartibini boshqarish</mark>

Standart holatda tartiblangan raqamlar tartibi 1 raqamidan boshlanadi. Agar siz bu sanoqni o'zingiz istagan biror sondan boshlanishini hohlasangiz start attributidan foydalanishingiz mumkin.

```html
<ol start="50">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_start" %}

## <mark style="color:green;">HTMLdagi ichki ro'yhatlar</mark>

Ro'yhatlar ichma ich ham bo'lishi mumkin (ro'yhat ichida ro'yhat)

```html
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

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_nested_ol" %}

{% hint style="warning" %}
**Eslatma**: Roʻyxat elementi (<mark style="color:red;">`<li>`</mark>) yangi roʻyxatni hamda rasmlar va havolalar kabi boshqa HTML elementlarini ham oʻz ichiga olishi mumkin.
{% endhint %}

## <mark style="color:green;">Bo'lim xulosasi</mark>

* Tartiblangan ro'yhat yaratish uchun <mark style="color:red;">`<ol>`</mark> elementidan foydalaning
* Tartiblanish turini belgilash uchun <mark style="color:red;">`type`</mark> attributidan foydalaning
* Ro'yhat elementlarini yaratish uchun <mark style="color:red;">`<li>`</mark> elementidan foydalaning
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
