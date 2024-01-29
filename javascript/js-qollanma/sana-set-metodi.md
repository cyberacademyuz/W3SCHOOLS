# Sana SET metodi

Sanani oʻrnatish metodlari Date obyekti uchun sana qiymatlarini (yillar, oylar, kunlar, soatlar, daqiqalar, soniyalar, millisekundlar) oʻrnatish imkonini beradi.

### Sanani o'rnatish metodlari

Set Date metodlar sananing bir qismini belgilash uchun ishlatiladi:

| Metod             | Ta'rif                                                                  |
| ----------------- | ----------------------------------------------------------------------- |
| setDate()         | Kunni raqam sifatida o'rnatish (1-31)                                   |
| setFullYear()     | Yilni o'rnatish (oy va kun ixtiyoriy)                                   |
| setHours()        | Soatni o'rnatish (0-23)                                                 |
| setMilliseconds() | Millisekundni o'rnatish (0-999)                                         |
| setMinutes()      | Daqiqani o'rnatish (0-59)                                               |
| setMonth()        | Oyni o'rnatish (0-11)                                                   |
| setSeconds()      | Soniyani o'rnatish (0-59)                                               |
| setTime()         | Vaqtni o'rnatish (1970 yil 1 yanvardan boshlab millisekundlar hisobida) |

### setFullYear() metodi

`setFullYear()` metodi Date obektining yilini o'rnatadi. Ushbu misolda 2020 yil:

```
const d = new Date();
d.setFullYear(2020);
```

`setFullYear()` metodida istasangiz oy va kunni belgilashingiz mumkin:

```
const d = new Date();
d.setFullYear(2020, 11, 3);
```

### setMonth() metodi

`setMonth()` metodi Date obektining oyini o'rnatadi(0-11):

```
const d = new Date();
d.setMonth(11);
```

### setDate() metodi

`setDate()` metodi Date obektining kunini o'rnatadi(1-31):

```
const d = new Date();
d.setDate(15);
```

`setDate()` metodi sanaga kun qo'shish uchun ham ishlatilishi mumkin :

```
const d = new Date();
d.setDate(d.getDate() + 50);
```

{% hint style="warning" %}
Agar kunlarni qo'shish oy yoki yilni o'zgartirsa, o'zgarishlar Date obekti tomonidan avtomatik tarzda amalga oshiriladi.
{% endhint %}

### setHours() metodi

`setHours()` metodi Date obektining soatlarini o'rnatadi(0-23):

```
const d = new Date();
d.setHours(22);
```

### setMinutes() metodi

`setMinutes()` Date obektining daqiqalarini o'rnatadi (0-59):

```
const d = new Date();
d.setMinutes(30);
```

### setSeconds() usuli

`setSeconds()` metodi Date obektining soniyalarini o'rnatadi (0-59):

```
const d = new Date();
d.setSeconds(30);
```

### Sanalarni solishtirish

Sanalarni osongina solishtirish mumkin.

Quyidagi misolda bugungi sanani 2100 yil 14 yanvar bilan solishtirilgan:

```
let text = "";
const today = new Date();
const someday = new Date();
someday.setFullYear(2100, 0, 14);

if (someday > today) {
  text = "Today is before January 14, 2100.";
} else {
  text = "Today is after January 14, 2100.";
}
```

{% hint style="warning" %}
JavaScript oylarni 0 dan 11 gacha hisoblaydi. Yanvar 0. Dekabr 11.
{% endhint %}

{% hint style="warning" %}
### Date haqida to'liq ma'lumotnoma

Date haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda date haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_date.asp)

Ma'lumotnomada Datening barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
