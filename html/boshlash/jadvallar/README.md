---
description: >-
  HTML jadvallari veb-dasturchilarga ma'lumotlarni qatorlar va ustunlarga
  ajratish imkonini beradi.
---

# Jadvallar

| Kompaniya                    | Kontakt          | Davlat    |
| ---------------------------- | ---------------- | --------- |
| Alfreds Futterkiste          | Maria Anders     | Germaniya |
| Centro comercial Moctezuma   | Francisco Chang  | Meksika   |
| Ernst Handel                 | Roland Mendel    | Avstriya  |
| Island Trading               | Helen Bennett    | UK        |
| Laughing Bacchus Winecellars | Yoshi Tannamuri  | Kanada    |
| Magazzini Alimentari Riuniti | Giovanni Rovelli | Italiya   |

## HTMLda jadval yaratish

HTMLdagi jadval, qatorlar va ustunlar ichidagi jadval kataklaridan iborat.

{% code title="Oddiy jadval" %}
```
<table>
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table> 
```
{% endcode %}

## Jadval kataklari

Har bir jadval katakchasi \<td> va \</td> tegi bilan o'raladi.

{% hint style="warning" %}
`td table data (`jadval ma'lumotlari)ni anglatadi.
{% endhint %}

`<td>`va  `</td>` orasidagi hamma narsa jadval katakchalarining tarkibi hisoblanadi.

```
<table>
  <tr>
    <td>Emil</td>
    <td>Tobias</td>
    <td>Linus</td>
  </tr>
</table> 
```

{% hint style="warning" %}
Jadval kataklari barcha turdagi HTML elementlarini qabul qiladi: matnlar, rasmlar, ro'yhatlar, havolalar va boshqalar
{% endhint %}

## Jadval qatorlari

Har bir jadval qatori  `<tr>` bilan boshlanadi va `</tr>` tegi bilan tugaydi.

{% hint style="warning" %}
tr jadval qatorini bildiradi
{% endhint %}

```
<table>
  <tr>
    <td>Emil</td>
    <td>Tobias</td>
    <td>Linus</td>
  </tr>
  <tr>
    <td>16</td>
    <td>14</td>
    <td>10</td>
  </tr>
</table>
```

Jadvalda xohlaganingizcha qatorga ega bo'lishingiz mumkin; faqat kataklar soni ham har bir qator bilan bir xil ekanligiga ishonch hosil qiling.

{% hint style="warning" %}
**Eslatma:** Ba'zida qatorlarda boshqasiga qaraganda kamroq yoki ko'proq kataklar bo'lishi mumkin. Bu haqda keyingi bo'limda bilib olasiz.
{% endhint %}

## Jadval sarlavhalari

Ba'zan kataklaringizda jadvalning sarlavha kataklari bo'lishini xohlaysiz. Bunday hollatda `<td>` tegi o'rniga `<th>` tegidan foydalaning:

{% hint style="warning" %}
`th -` jadval sarlavhasini anglatadi.
{% endhint %}

{% code title="Birinchi qator jadval sarlavhasining kataklari hisoblanadi:" %}
```
<table>
  <tr>
    <th>Person 1</th>
    <th>Person 2</th>
    <th>Person 3</th>
  </tr>
  <tr>
    <td>Emil</td>
    <td>Tobias</td>
    <td>Linus</td>
  </tr>
  <tr>
    <td>16</td>
    <td>14</td>
    <td>10</td>
  </tr>
</table>
```
{% endcode %}

Odatda \<th> elementi ichidagi matn qalin va markazda joylashgan bo'ladi ammo siz uni CSS orqali o'zgartirishingiz mumkin.

## HTMLdagi jadval teglari

| Teg                                                             | Tavsif                                                                        |
| --------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [\<table>](https://www.w3schools.com/tags/tag\_table.asp)       | Jadval yaratish                                                               |
| [\<th>](https://www.w3schools.com/tags/tag\_th.asp)             | Jadval ichida sarlavha katagini yaratish                                      |
| [\<tr>](https://www.w3schools.com/tags/tag\_tr.asp)             | Jadvalning qatorini belgilash                                                 |
| [\<td>](https://www.w3schools.com/tags/tag\_td.asp)             | Jadval katagini yaratish                                                      |
| [\<caption>](https://www.w3schools.com/tags/tag\_caption.asp)   | Jadval sarlavhasi                                                             |
| [\<colgroup>](https://www.w3schools.com/tags/tag\_colgroup.asp) | Formatlash uchun jadvaldagi bir yoki bir nechta ustunlar guruhini belgilaydi  |
| [\<col>](https://www.w3schools.com/tags/tag\_col.asp)           | \<colgroup> elementidagi har bir ustun uchun ustun xususiyatlarini ifodalaydi |
| [\<thead>](https://www.w3schools.com/tags/tag\_thead.asp)       |  Jadvaldagi sarlavha tarkibini guruhlarga ajratadi                            |
| [\<tbody>](https://www.w3schools.com/tags/tag\_tbody.asp)       | Jadvaldagi asosiy qismlarini guruhlarga ajratadi                              |
| [\<tfoot>](https://www.w3schools.com/tags/tag\_tfoot.asp)       | Jadvalning footer qismidagilarni guruhlaydi                                   |
