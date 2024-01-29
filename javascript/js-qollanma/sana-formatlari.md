# Sana formatlari

### JavaScriptda sanlarni kiritish

Odatda JavaScriptda sana kiritish formatlarining 3 turi mavjud:

| Turi         | Misol                                      |
| ------------ | ------------------------------------------ |
| ISO Date     | "25-03-2015" (Xalqaro standart)            |
| Qisqa sana   | "25.03.2015"                               |
| Uzunroq sana | "2015 yil 25 mart" yoki "2015 yil 25 mart" |

{% hint style="warning" %}
ISO formati JavaScript-da qat'iy standartga amal qiladi.

Boshqa formatlar unchalik aniq ifodalanmagan va brauzerga xos bo'lishi mumkin.
{% endhint %}

### Sanani ko'rsatish

Kiritilgan formatdan qat'iy nazar, JavaScript sanalarni (default) to'liq matnli string formatida chiqaradi:

```
Mon Mar 13 2023 13:11:07 GMT+0500 (Pakistan Standard Time)
```

### ISO sanalari

ISO 8601 sana va vaqtni ko'rsatish uchun xalqaro standart hisoblanadi.

ISO 8601-ning sintaksisi (YYYY-AA-KK) ham JavaScriptda afzal ko'rilgan sana formati hisoblanadi:

```
const d = new Date("2015-03-25");
```

{% hint style="warning" %}
Hisoblangan sana sizning vaqt mintaqangizga nisbatan bo'ladi.

Vaqt mintaqangizga qarab, yuqoridagi natija 24 martdan 25 martgacha o'zgaradi.
{% endhint %}

### ISO sanalari (yil va oy)

ISO sanalarini kun sanasi ko'rsatilmagan formatda yozish mumkin (YYYY-MM):

```
const d = new Date("2015-03");
```

{% hint style="warning" %}
Vaqt mintaqalarida yuqoridagi natija 28 fevraldan 01 mart oralig'ida farq qilishi mumkin.
{% endhint %}

### ISO sanalari (faqat yil)

ISO sanalarini oy va kun sanasi ko'rsatilmagan formatda yozish mumkin (YYYY):

```
const d = new Date("2015")
```

{% hint style="warning" %}
Vaqt zonalarida yuqoridagi natijani 2014-yil 31-dekabrdan bilan 2015-yil 01-yanvar oralig'ida farq qiladi.
{% endhint %}

### ISO sanalari (sana-vaqt)

ISO sanalari soatlar, daqiqalar va soniyalar bilan yozilishi mumkin (YYYY-AA-DDTH:MM:SSZ):

```
const d = new Date("2015-03-25T12:00:00Z");
```

Sana va vaqt T harfi bilan ajratiladi.

UTC vaqti Z harfi bilan belgilanadi.

Agar siz vaqtni UTC ga nisbatan o'zgartirmoqchi bo'lsangiz, Z belgisini olib tashlang va o'rniga +HH:MM yoki -SH:MM dan foydalaning:

```
const d = new Date("2015-03-25T12:00:00-06:30");
```

{% hint style="warning" %}
UTC (Universal Time Coordinated) GMT (Greenwich Mean Time) bilan bir xil.
{% endhint %}

{% hint style="danger" %}
Sana stringgida T yoki Z ni kiritmaslik turli brauzerlarda turli natijalar berishi mumkin.
{% endhint %}

### Vaqt zonalari

Sanani vaqt mintaqasini ko'rsatmasdan sozlanganda, JavaScript brauzerning vaqt mintaqasidan foydalanadi.

Vaqt mintaqasisiz sanani aniqlashda natija brauzerning vaqt mintaqasiga o'tkaziladi.

Boshqacha qilib aytganda: Agar sana GMTda yaratilgan bo'lsayu lekin foydalanuvchi AQShda turib  ko'rayotgan bo'lsa, sana CDT (AQShning markaziy kunduzi vaqti) ga o'zgartiriladi.

### Qisqa sanalar.

Qisqa sanalar "MM/DD/YYYY" sintaksisi bilan quyidagicha yoziladi:

```
const d = new Date("03/25/2015");
```

### Ogohlantirishlar!

Ba'zi brauzerlarda 0 bilan yozilmagan oylar yoki kunlar xatoga olib kelishi mumkin:

```
const d = new Date("2015-3-25");
```

“YYYY/OO/KK” harakati aniqlanmagan.\
Ba'zi brauzerlar sana formatini taxmin qilishga harakat qilishadi. Ba'zilari esa NaNni qaytaradi.

```
const d = new Date("2015/03/25");
```

“DD-MM-YYYY” harakati ham aniqlanmagan.\
Ba'zi brauzerlar sana formatini taxmin qilishga harakat qilishadi. Ba'zilai esa  NaNni qaytaradi.

```
const d = new Date("25-03-2015");
```

***

### Uzun sanalar.

Uzunroq sanalar ko'pincha "MMD DD YYYY" sintaksisi sifatida quyidagicha yoziladi:

```
const d = new Date("Mar 25 2015");
```

Oy va kun har qanday tartibda bo'lishi mumkin:

```
const d = new Date("25 Mar 2015");
```

Va oynomi  to'liq (yanvar) shaklda yoki qisqartirilgan (yan) shaklda yozilishi mumkin:

```
const d = new Date("January 25 2015");
```

```
const d = new Date("Jan 25 2015");
```

Vergullar e'tiborga olinmaydi. Nomlar katta-kichik harfligiga qarab farqlanmaydi.

```
const d = new Date("JANUARY, 25, 2015")
```

### Sanani kiritish - Sanalarni parse  qilish

Agar sizda to'g'ri ko'rinishdagi sana stringgi bo'lsa, uni millisekundlarga aylantirish uchun `Date.parse()` metodidan foydalanishingiz mumkin&#x20;

`Date.parse()` sana va 1970 yil 1 yanvar o'rtasidagi millisekund miqdorini qaytaradi:

```
let msec = Date.parse("March 21, 2012");
```

Keyin uni sana obektiga aylantirish uchun millisekundlar miqdoridan foydalanishingiz mumkin:

```
let msec = Date.parse("March 21, 2012");
const d = new Date(msec);
```

{% hint style="warning" %}
### Date haqida to'liq ma'lumotnoma

Date haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda date haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_date.asp)

Ma'lumotnomada Datening barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
