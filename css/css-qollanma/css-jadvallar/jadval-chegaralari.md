# Jadval chegaralari

HTML jadvallarning ko'rinishi CSS yordamida sezilarli darajada yaxshilash mumkin:

| Company                      | Contact            | Country |
| ---------------------------- | ------------------ | ------- |
| Alfreds Futterkiste          | Maria Anders       | Germany |
| Berglunds snabbköp           | Christina Berglund | Sweden  |
| Centro comercial Moctezuma   | Francisco Chang    | Mexico  |
| Ernst Handel                 | Roland Mendel      | Austria |
| Island Trading               | Helen Bennett      | UK      |
| Königlich Essen              | Philip Cramer      | Germany |
| Laughing Bacchus Winecellars | Yoshi Tannamuri    | Canada  |
| Magazzini Alimentari Riuniti | Giovanni Rovelli   | Italy   |

### Jadval chegaralari <a href="#jadval-chegaralari" id="jadval-chegaralari"></a>

Jadval chegaralarini CSS orqali belgilash uchun `border` xususiyatidan foydalanish mumkin.

Ushbu misolda `<table>`, `<th>` va `<td>` elementlariga chegara berish ko'rsatilgan.

![](<../../../.gitbook/assets/image (306).png>)

```
table, th, td {
  border: 1px solid;
}
```

### To'liq uzunlikdagi jadval <a href="#uzun-jadval" id="uzun-jadval"></a>

Yuqoridagi jadval ba'zi holatlarda kichkina ko'rinishi mumkin. Agar butun ekranni qamrab oladigan jadval kerak bo'lsa, `<table>` elementiga `width: 100%` qo'shing:

<figure><img src="../../../.gitbook/assets/image (646).png" alt=""><figcaption></figcaption></figure>

```
table {
  width: 100%;
}
```

{% hint style="warning" %}
### Ikkitalik chegaralar <a href="#ikki-tomonlama-chegaralar" id="ikki-tomonlama-chegaralar"></a>

E'tibor bering, yuqoridagi misollardagi jadval ikkita chegaraga ega. Buning sababi shundaki, jadval ham, `<th>` va `<td>` elementlari ham o'zining alohida chegaralariga ega.

Ikkitalik chegaralarni olib tashlash uchun quyidagi misolni ko'rib chiqing.
{% endhint %}

### Jadval chegaralarini olib tashlash <a href="#jadval-chegaralarini-olib-tashlash" id="jadval-chegaralarini-olib-tashlash"></a>

`border-collapse` xususiyati jadval chegaralarini bitta chegaraga yig'ish kerakligini belgilaydi:

<figure><img src="../../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

```
table {
  border-collapse: collapse;
}
```

Agar faqat jadvalning atrofida chegara bo'lishini istasangiz, faqat  `<table>` ga `border` xususiyatini bering:

<figure><img src="../../../.gitbook/assets/image (516).png" alt=""><figcaption></figcaption></figure>

```
table {
  border: 1px solid;
}
```
