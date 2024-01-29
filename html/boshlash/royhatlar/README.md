---
description: >-
  HTML ro'yxatlari veb dasturchilarga ro'yxatga tegishli elementlar to'plamini
  guruhlashga imkonini beradi.
---

# Ro'yhatlar

<figure><img src="../../../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure>

## Tartiblanmagan HTML ro'yhati

Tartiblanmagan ro'yhatlar `<ul>` tegi bilan yoziladi. Ro'yhatning har bir elementi `<li>` tegining ichida bo'ladi.

Ro'yhatning har bir elementining oldida kichik qora belgi bo'ladi.

```
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```

## Tartiblangan ro'yhat

Tartiblangan ro'yhatlar `<ol>` tegi bialn boshlanadi. Ro'yhatning har bir elementi `<li>` tegining ichida bo'ladi.

Ro'yhatning har bir elementining oldida tartib raqami bo'ladi.

```
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

## HTML Description list

HTML _**d**escription **l**ist_ni ham qo'llab quvvatlaydi.

Ta'riflar ro'yxati - bu har bir atamaning tarifi berilgan atamalar ro'yxati hisoblanadi.

`<dl>` tegi description list ni bildiradi, `<dt>` elementi atama nomini `<dd>` esa atamaning tarifini o'z ichiga oladi:

```
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```

| Teg   | Tarif                                            |
| ----- | ------------------------------------------------ |
| \<ul> | Tartiblanmagan ro'yhat yaratadi                  |
| \<ol> | Tartiblangan ro'yhat yaratadi                    |
| \<li> | Ro'yhat elementlarini belgilaydi                 |
| \<dl> | Tariflar ro'yhatini belgilaydi                   |
| \<dt> | Ta'riflar ro'yxatidagi atamani belgilaydi        |
| \<dd> | Ta'riflar ro'yxatidagi atama tarifini belgilaydi |

