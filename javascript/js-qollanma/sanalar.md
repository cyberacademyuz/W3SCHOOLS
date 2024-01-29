# Sanalar

JavaScriptning **Date** obektlari sanalar bilan ishlashimizga imkon beradi:

**2023 yil 13-mart dushanba, 08:47:50 GMT+0500 (Pokiston standart vaqti)**

<figure><img src="../../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure>

```
const d = new Date();
```

```
const d = new Date("2022-03-25");
```

{% hint style="warning" %}
### Eslatma

Date obektlari statik bo'ladi. "Clock" "ishlamaydi".

Kompyuter soati tiqillayapti, sana obektlari esa yo'q.
{% endhint %}

### Sanani ko'rsatish&#x20;

Odatda, JavaScript brauzerning vaqt mintaqasidan foydalanadi va sanani to'liq shaklda matnli string sifatida ko'rsatadi:

**2023 yil 13-mart dushanba, 08:47:50 GMT+0500 (Pokiston standart vaqti)**

Sanalarni qanday ko'rsatish haqida keyinroq batafsil bilib olasiz.

### Date obyektlarini yaratish

Sana obyektlari `new Date()` konstruktori yordamida yaratiladi.

Yangi date obyektini yaratishning **9 ta usuli** bor.

```
new Date()
new Date(date string)

new Date(year,month)
new Date(year,month,day)
new Date(year,month,day,hours)
new Date(year,month,day,hours,minutes)
new Date(year,month,day,hours,minutes,seconds)
new Date(year,month,day,hours,minutes,seconds,ms)

new Date(milliseconds)
```

## new date(D

`new Date()` **joriy sana va vaqtni** ko'rsatadigan sana obyektini yaratadi:

```
const d = new Date();
```

### new Date (_date string_)

`new Date(`_`date string`_`)`  **string sifatida berilgan sana** yordamida  sana obyektini yaratadi:

```
const d = new Date("October 13, 2014 11:13:00");
```

```
const d = new Date("2022-03-25");
```

{% hint style="warning" %}
Sana stringining formatlari keyingi bo'limda tushuntirilgan.
{% endhint %}

### new date( _yil, oy, ..._ )

`new Date(`_`yil, oy, ...`_`)`**belgilangan sana va vaqt** ni o'z ichiga olgan sana obektini yaratadi.

Quyidagi misoda ko'rsatilgan 7 ta raqam yil, oy, kun, soat, daqiqa, soniya va millisekundni bildiradi (shu tartibda):

```
const d = new Date(2018, 11, 24, 10, 33, 30, 0);
```

{% hint style="warning" %}
### Eslatma

JavaScript oylarni 0 dan 11 gacha sanaydi&#x20;

Yanvar = 0.

Dekabr = 11.
{% endhint %}

11-oydan katta oyni ko'rsatish xatolikka olib kelmaydi, lekin keyingi yilga o'tib ketadi:

```
const d = new Date(2018, 15, 24, 10, 33, 30);

bu bilan bir xil

const d = new Date(2019, 3, 24, 10, 33, 30);
```

Ohirgi kunlik sanadan katta sanani ko'rsatish xatolikka olib kelmaydi, lekin keyingi oyga o'tib ketadi.

```
const d = new Date(2018, 5, 35, 10, 33, 30);

bu bilan bir xil

const d = new Date(2018, 6, 5, 10, 33, 30);
```

### 6, 4, 3 yoki 2 raqamlardan foydalanish

Quyidagi misolda ko'rsatilgan 6 ta raqam yil, oy, kun, soat, daqiqa, soniyani bildiradi:

```
const d = new Date(2018, 11, 24, 10, 33, 30);
```

5 ta raqam yil, oy, kun, soat va daqiqani bildiradi:

```
const d = new Date(2018, 11, 24, 10, 33);
```

4 ta raqam yil, oy, kun va soatni bildiradi:

```
const d = new Date(2018, 11, 24, 10);
```

3 ta raqam yil, oy va kunni bildiradi:

```
const d = new Date(2018, 11, 24);
```

2 raqam yil va oyni ko'rsatadi:

```
const d = new Date(2018, 11);
```

{% hint style="warning" %}
Siz oyni kiritmasdan qoldirib ketolmaysiz. Agar faqat bitta parametrni bersangiz, u millisekund sifatida qabul qilinadi.
{% endhint %}

```
const d = new Date(2018);
```

### O'tgan asr

Yil kiritiladigan qismga bitta va ikkita raqam kiritish yilni 19xx sifatida qabul qiladi:

```
const d = new Date(99, 11, 24);
```

```
const d = new Date(9, 11, 24);
```

{% hint style="warning" %}
### JavaScript sanalarni millisekundlar sifatida saqlaydi

JavaScript sanalarni 1970 yil 1 yanvardan boshlab millisekundlar sifatida saqlaydi.

Boshlang'ich vaqt 1970 yil 01 yanvar 00:00:00 UTC .

Bir kun (24 soat) 86 400 000 millisekundga teng.

Hozirgi vaqt: 1970 yil 1 yanvardan **1678679270393** millisekund o'tgan.
{% endhint %}

### new Date(_millisekundlar_)

`new Date(`_`milliseconds`_`)` millisekundlar va boshlang'ich vaqt sifatida yangi sana obektini yaratadi:

{% code title="01 yanvar 1970 yil, dan boshlab 100 000 000 000 millisekundni hisoblash:" %}
```
const d = new Date(100000000000)
```
{% endcode %}

{% code title="1970 yil 1 yanvar sanasidan 100 000 000 000 millisekundni ayirish:" %}
```
const d = new Date(-100000000000);
```
{% endcode %}

{% code title=" 1970 yil 1-yanvar-ga 24 soat qo'shish:" %}
```
const d = new Date(24 * 60 * 60 * 1000);
// yoki
const d = new Date(86400000);
```
{% endcode %}

{% code title="01 yanvar 1970 yilaga 0 millisekund qo'shish:" %}
```
const d = new Date(0);
```
{% endcode %}

### Date metodlari

Date obekti yaratilganda, bir qancha **metodlar** u bilan ishlashga imkon beradi.

Date metodlari mahalliy vaqt yoki UTC (universal yoki GMT) dan foydalangan holda sana obyektlarining yil, oy, kun, soat, daqiqa, soniya va millisekundini olish va belgilash imkonini beradi.

{% hint style="warning" %}
Date metodlari va vaqt zonalari keyingi bo'limlarda tushuntiriladi.
{% endhint %}

### Sanalarni ko'rsatish

JavaScript (default tarzda) sanalarni to'liq matnli string formatida ko'rsatadi:

```
Mon Mar 13 2023 08:47:50 GMT+0500 (Pakistan Standard Time)
```

HTML-da date obektini chiqarganingizda, u `toString()` metodi bilan avtomatik tarzda stringga aylantiriladi.

```
const d = new Date();
d.toString();
```

`toDateString()` metodi sanani o'qishga osonroq bo'lgan holatga keltiradi:

```
const d = new Date();
d.toDateString();
```

`toUTCString()` metodi UTC standarti yordamida sanani stringga o'tkazadi:

```
const d = new Date();
d.toUTCString();
```

`toISOString()` metodi ISO standarti yordamida sanani stringga o'tkazadi:

```
const d = new Date();
d.toISOString();
```

{% hint style="warning" %}
### Date haqida to'liq ma'lumotnoma

Date haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda date haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_date.asp)

Ma'lumotnomada Datening barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
