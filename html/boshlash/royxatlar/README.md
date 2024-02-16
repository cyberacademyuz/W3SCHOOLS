---
description: >-
  HTMLda ro'yxatlar dasturchilarga ro'yxatga tegishli elementlar to'plamini
  guruhlashga imkonini beradi.
---

# Ro'yxatlar

<figure><img src="../../../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_intro" %}

## <mark style="color:green;">Tartiblanmagan HTML ro'yhati</mark>

Tartiblanmagan ro'yxatlar <mark style="color:red;">`<ul>`</mark> tegi bilan yoziladi. Ro'yxatning har bir elementi <mark style="color:red;">`<li>`</mark> tegining ichida bo'ladi.

Ro'yhatning har bir elementining oldida kichik qora belgi bo'ladi.

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_unordered" %}

## <mark style="color:green;">Tartiblangan ro'yxat</mark>

Tartiblangan ro'yxatlar <mark style="color:red;">`<ol>`</mark> tegi bialn boshlanadi. Ro'yxatning har bir elementi <mark style="color:red;">`<li>`</mark> tegining ichida bo'ladi.

Ro'yxatning har bir elementining oldida tartib raqami bo'ladi.

```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_ordered" %}

## <mark style="color:green;">HTML Description list</mark>

HTML _**d**escription **l**ist_ni ham qo'llab quvvatlaydi.

Ta'riflar ro'yxati - bu har bir atamaning tarifi berilgan atamalar ro'yxati hisoblanadi.

<mark style="color:red;">`<dl>`</mark> tegi description list ni bildiradi, <mark style="color:red;">`<dt>`</mark> elementi atama nomini <mark style="color:red;">`<dd>`</mark> esa atamaning tarifini o'z ichiga oladi:

```html
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_description" %}

| Teg   | Tarif                                            |
| ----- | ------------------------------------------------ |
| \<ul> | Tartiblanmagan ro'yxat yaratadi                  |
| \<ol> | Tartiblangan ro'yxat yaratadi                    |
| \<li> | Ro'yxat elementlarini belgilaydi                 |
| \<dl> | Tariflar ro'yxatini belgilaydi                   |
| \<dt> | Ta'riflar ro'yxatidagi atamani belgilaydi        |
| \<dd> | Ta'riflar ro'yxatidagi atama tarifini belgilaydi |
