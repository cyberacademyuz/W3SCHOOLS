# Sana GET metodi

### Yangi Date() konstruktori

JavaScript-da sana obyektlari `new Date()` bilan yaratiladi.

`new Date()` joriy sana va vaqt bilan birga date obektini qaytaradi.

{% code title="Joriy sana ma'lumotlarini oling" %}
```
const date = new Date();:
```
{% endcode %}

### Sana ma'lumotlarini olish metodlari

| Metod             | Ta'rif                                                              |
| ----------------- | ------------------------------------------------------------------- |
| getFullYear()     | Yilni to'rt xonali raqam sifatida oling (yyyy)                      |
| getMonth()        | Oyni raqam sifatida oling (0-11)                                    |
| getDate()         | Kunni raqam sifatida oling (1-31)                                   |
| getDay()          | Hafta kunini raqam sifatida oling (0-6)                             |
| getHours()        | Soatni oling (0-23)                                                 |
| getMinutes()      | Daqiqa olish (0-59)                                                 |
| getSeconds()      | Soniyani oling (0-59)                                               |
| getMilliseconds() | Millisekundni oling (0-999)                                         |
| getTime()         | Vaqtni oling (1970 yil 1 yanvardan boshlab millisekundlar hisobida) |

{% hint style="warning" %}
### Eslatma 1

Yuqoridagi get metodlari mahalliy vaqtni qaytaradi.

UTC haqida ushbu sahifaning pastki qismidama'lumot  keltirilgan.
{% endhint %}

{% hint style="warning" %}
### Eslatma 2

Get metodlari mavjud date obektlaridan ma'lumot qaytaradi.

Date obyektida vaqt statikdir. "Soat" "ishlamaydi".

Sana obyektidagi vaqt joriy vaqt bilan bir xil EMAS.
{% endhint %}

### getFullYear() metodi

`getFullYear()` metodi sana yilini to'rt xonali raqam sifatida qaytaradi:

```
const d = new Date("2021-03-25");
d.getFullYear();const d = new Date();
d.getFullYear();
```

{% hint style="danger" %}
### Ogohlantirish!

Eski JavaScript kodlarida nostandart bo'lgan getYear() metodidan foydalanish mumkin.

getYear()  yilni 2 xonali raqam sifatida qaytarishi kerak.

getYear() eskirgan. Undan foydalanmang!
{% endhint %}

### getMonth() metodi

`getMonth()` metodi sana oyini raqam sifatida qaytaradi (0-11).

{% hint style="warning" %}
### Eslatma

JavaScript-da yanvar 0-oy, fevral-1, ...

Va nihoyat, dekabr 11-oydir.
{% endhint %}

```
const d = new Date("2021-03-25");
d.getMonth();
```

```
const d = new Date();
d.getMonth();
```

{% hint style="warning" %}
### Eslatma

Oyni o'z nomi bilan qaytarish uchun oy nomlaridan tashkil topgan arraydan foydalanishingiz mumkin:
{% endhint %}

```
const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];

const d = new Date("2021-03-25");
let month = months[d.getMonth()];
```

```
const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];

const d = new Date();
let month = months[d.getMonth()];
```

### getDate() metodi

`getDate()` metodi sana kunini raqam sifatida qaytaradi (1-31):

```
const d = new Date("2021-03-25");
d.getDate();const d = new Date();
d.getDate();
```

### getHours() metodi

`getHours()` metodi sana soatlarini raqam sifatida qaytaradi (0-23):

```
const d = new Date("2021-03-25");
d.getHours();const d = new Date();
d.getHours();
```

### getMinutes() metodi

`getMinutes()`metodi sana minutlarini raqam sifatida qaytaradi (0-59):

```
const d = new Date("2021-03-25");
d.getMinutes();const d = new Date();
d.getMinutes();
```

### getSeconds() usuli

`getSeconds()` metodi sana soniyalarini raqam sifatida qaytaradi (0-59):

```
const d = new Date("2021-03-25");
d.getSeconds();const d = new Date();
d.getSeconds();
```

### getMilliseconds() usuli

`getMilliseconds()` metodi sana millisekundlarini raqam sifatida qaytaradi (0-999):

```
const d = new Date("2021-03-25");
d.getMilliseconds();const d = new Date();
d.getMilliseconds();
```

### getDay() metodi

`getDay()` metodi sana kunini raqam sifatida qaytaradi (0-6).

{% hint style="warning" %}
### Eslatma

JavaScript-da haftaning birinchi kuni (0-kun) yakshanba.

Dunyoning boshqa ba'zi mamlakatlari haftaning birinchi kunini dushanba deb hisoblashadi.
{% endhint %}

```
const d = new Date("2021-03-25");
d.getDay();const d = new Date();
d.getDay();
```

{% hint style="warning" %}
### Eslatma

Siz oy nomlarini o'z ichiga olgan arraydan va hafta kunini hafta nomi sifatida qaytarish uchun `getDay()` dan foydalanishingiz mumkin:
{% endhint %}

```
const days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

const d = new Date("2021-03-25");
let day = days[d.getDay()];
```

```
const days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

const d = new Date();
let day = days[d.getDay()];
```

### getTime() metodi

`getTime()`  metodi 1970 yil 1 yanvardan boshlab hozirgi kungacha bo'lgan millisekundlar sonini qaytaradi:

```
const d = new Date("1970-01-01");
d.getTime();const d = new Date("2021-03-25");
d.getTime();const d = new Date();
d.getTime();
```

### Date.now() metodi

`Date.now()`  1970 yil 1 yanvardan boshlab hozirgi kungacha bo'lgan millisekundlar sonini qaytaradi:

```
let ms = Date.now();
```

{% code title="1970/01/01 yildan boshlab necha yil o'tganini hisoblash:" %}
```
const minute = 1000 * 60;
const hour = minute * 60;
const day = hour * 24;
const year = day * 365;

let years = Math.round(Date.now() / year); 
```
{% endcode %}

`Date.now()` Date obyektining statik metodi hisoblanadi.

Siz uni `myDate.now()` kabi sana obektida ishlata olmaysiz.

Uning sintaksisi har doim `Date.now()`.

### UTC sanasini olish usullari

| Method               | Bu bilan bir xil  | Ta'rif                        |
| -------------------- | ----------------- | ----------------------------- |
| getUTCDate()         | getDate()         | Sanani UTCda qaytaradi        |
| getUTCFullYear()     | getFullYear()     | Yilni UTCda qaytaradi         |
| getUTCMonth()        | getMonth()        | Oyni UTCda qaytaradi          |
| getUTCDay()          | getDay()          | Kunni UTCda qaytaradi         |
| getUTCHours()        | getHours()        | Soatni UTCda qaytaradi        |
| getUTCMinutes()      | getMinutes()      | Daqiqani UTCda qaytaradi      |
| getUTCSeconds()      | getSeconds()      | Soniyani UTCda qaytaradi      |
| getUTCMilliseconds() | getMilliseconds() | Millisekundni UTCda qaytaradi |

UTC metodlari UTC vaqtidan foydalanadi.

UTC vaqti GMT bilan bir xil.

Mahalliy vaqt va UTC vaqti o'rtasidagi farq 24 soatgacha bo'lishi mumkin.

![](../../.gitbook/assets/image.png)

<mark style="background-color:green;">Mahalliy vaqt ?</mark>

<mark style="background-color:green;">UTC vaqti ?</mark>

### getTimezoneOffset() metodi

`getTimezoneOffset()`metodi mahalliy vaqt va UTC vaqti o'rtasidagi farqni (daqiqalarda) qaytaradi:

```
let diff = d.getTimezoneOffset();
```

{% hint style="warning" %}
### Date haqida to'liq ma'lumotnoma

Date haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda date haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_date.asp)

Ma'lumotnomada Datening barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
