# Jadval moslashuvchanligi

### Moslashuvchan jadvalla <a href="#adaptiv-jadvallar" id="adaptiv-jadvallar"></a>

To'liq takibni ko'rsatish uchun ekran juda kichkinalik qilsa moslashuvchan jadvalda gorizontal scroll bar paydo bo'ladi

| Ism  | Familya | Ballar | Ballar | Ballar | Ballar | Ballar | Ballar | Ballar | Ballar | Ballar | Ballar | Ballar | Ballar |
| ---- | ------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| Jill | Smith   | 50     | 50     | 50     | 50     | 50     | 50     | 50     | 50     | 50     | 50     | 50     | 50     |
| Eve  | Jackson | 94     | 94     | 94     | 94     | 94     | 94     | 94     | 94     | 94     | 94     | 94     | 94     |
| Adam | Johnson | 67     | 67     | 67     | 67     | 67     | 67     | 67     | 67     | 67     | 67     | 67     | 67     |

Jadvalni moslashuvchan qilish uchun \<table>ni o'rab turuvchi konteyner (masalan \<div>) qo'shing va konteynerga `overflow-x:auto` bering.

```
<div style="overflow-x:auto;">

<table>
... table content ...
</table>

</div>
```

{% hint style="warning" %}
**Note:** OS X Lion-da (Mac-da) skroll barlar standart standart tarzda yashirin bo'ladi va faqat foydalanilganda ko'rsatiladi (garchi "`overflow: scroll`" berilgan bo'lsa ham).
{% endhint %}

### CSS Jadval Xususiyatlari <a href="#css-jadval-xususiyatlari" id="css-jadval-xususiyatlari"></a>

| Xususiyat                                                                   | Ta'rif                                                                                      |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| [border](https://www.w3schools.com/cssref/pr\_border.asp)                   | Barcha border xususiyatlarini bitta deklaratsiyada yozishga imkon beradi                    |
| [border-collapse](https://www.w3schools.com/cssref/pr\_border-collapse.asp) | Jadvaladagi borderlar bo'lishi kerakmi yoki yo'q belgilaydi                                 |
| [border-spacing](https://www.w3schools.com/cssref/pr\_border-spacing.asp)   | Jadvaldagi har bir elementlar orasidagi bo'sh joyni qanday bo'lishini belgilaydi            |
| [caption-side](https://www.w3schools.com/cssref/pr\_tab\_caption-side.asp)  | Jadval sarlavhasini joylashtirishni belgilaydi                                              |
| [empty-cells](https://www.w3schools.com/cssref/pr\_tab\_empty-cells.asp)    | Jadvalning bo'sh kataklarida chegaralar va fonni ko'rsatish yoki ko'rsatmaslikni belgilaydi |
| [table-layout](https://www.w3schools.com/cssref/pr\_tab\_table-layout.asp)  | Jadval uchun ishlatiladigan tartib algoritmini o'rnatadi                                    |
