# RegExp

RegExp - qidiruv sxemasining belgilar ketma-ketligini o'z ichiga oladi.

Qidiruv sxemasi matnni qidirish va almashtirish kabi amallarni bajarish uchun ishlatiladi.

### Regular Expression nima ?

RegExp - qidiruv sxemasining belgilar ketma-ketligini o'z ichiga oladi.

Matndagi ma'lumotlarni qidirganingizda, qidirayotgan narsangizni tasvirlash uchun ushbu qidiruv sxemasidan foydalanishingiz mumkin.

RegExp birgina belgi yoki murakkabroq sxema bo'lishi mumkin.

RegExp matnni qidirish va matnni almashtirish kabi amallarning barcha turlarini bajarish uchun ishlatilishi mumkin.

### Sintaksisi

```
/pattern/modifiers;
```

```
/w3schools/i;
```

Misol orqali tushuntirish:

**/w3schools/i**  RegExp deyiladi.

**w3schools**   - bu pattern \[sxema] (qidiruvda foydalanish uchun).

**i**   - modifikator (qidiruvni katta-kichik harflarga farqlanuvchi qilib o'zgartiradi).

### String metodlaridan foydalanish

JavaScript-da RegExp ko'pincha ikkita string metodi bilan ishlatiladi: `search()` va `replace()`.

`search()` metodi moslikni qidirish uchun ifodadan foydalanadi va mos keladigan joyni qaytaradi.

`replace()` metodi pattern o'zgartirilgan joydagi o'zgargan stringni qaytaradi.

### String search()ni String bilan ishlatish

`search()` metodi berilgan qiymatga mos keluvchi stringni qidiradi va mos kelgan indexni qaytaradi:

{% code title="String ichidan "W3schools" ni qidirish uchun stringdan foydalaning:" %}
```
let text = "Visit W3Schools!";
let n = text.search("W3Schools");
```
{% endcode %}

{% code title="n dagi natija quyidagicha bo'ladi:" %}
```
6
```
{% endcode %}

### String search()ni RegExp bilan ishlatish

{% code title="Stringdagi "w3schools" uchun katta-kichik harflarsiz qidiruvni amalga oshirish uchun RegExpdan foydalaning:" %}
```
let text = "Visit W3Schools";
let n = text.search(/w3schools/i);
```
{% endcode %}

{% code title="n dagi natija quyidagicha bo'ladi:" %}
```
6
```
{% endcode %}

### String replace() ni String bilan ishlatish

`replace()` metodi parametr sifatida berilgan qiymatni stringdagi boshqa qiymat bilan almashtiradi:

```
let text = "Visit Microsoft!";
let result = text.replace("Microsoft", "W3Schools");
```

### String replace()ni RegExp bilan ishlatish

{% code title="String ichidagi Microsoftni W3schools bilan almashtirish uchun katta kichik harflarga farq qiluvchi RegExpdan foydalaning:" %}
```
let text = "Visit Microsoft!";
let result = text.replace(/microsoft/i, "W3Schools");
```
{% endcode %}

{% code title="result o'zgaruvchisining qiymati:" %}
```
Visit W3Schools! 
```
{% endcode %}

### E'tibor berdingizmi?

{% hint style="warning" %}
Yuqoridagi metodlarda RegExp argumentlaridan (string argumentlari o'rniga) foydalanish mumkin.\
RegExplar qidiruvingizni yanada kuchliroq qilishi mumkin (masalan, katta-kichik harflarga farqlanmaydigan qilib).
{% endhint %}

### RegExp modifikatorlari

**Modifikatorlar** katta-kichik harflarga e'tibot qilinmaydigan global qidiruvlarni amalga oshirish uchun ishlatilishi mumkin:

| Modifier | Ta'rif                                                                                              |
| -------- | --------------------------------------------------------------------------------------------------- |
| i        | Katta kichik harflarga e'tibor qilmaydigan moslikni topish                                          |
| g        | Global moslikni topish. (Birinchi moslik topilganidan keyin ham qolgan barcha mosliklarni aniqlash) |
| m        | Ko'p qatorli moslikni topish                                                                        |

### RexExp patternlari

**Qavslar** bir qator belgilarni topish uchun ishlatiladi:

| Expression | Ta'rif                                                     |
| ---------- | ---------------------------------------------------------- |
| \[abc]     | Qavslar orasidagi har qanday belgilarni topish             |
| \[0-9]     | Qavslar orasidagi istalgan raqamni toping                  |
| (x\|y)     | \| bilan ajratilgan alternativ variantlardan birini toping |

**Metabelgilar** - bu alohida ma'noga ega bo'lgan belgilar:

**Miqdorlar** miqdorlarni belgilaydi:

| Metabelgi | Ta'rif                                                                                         |
| --------- | ---------------------------------------------------------------------------------------------- |
| \d        | Raqamni topish                                                                                 |
| \s        | Bo'sh joy belgisini topish                                                                     |
| \b        | Quyidagi kabi so'zning boshlanishini toping: \bWORD yoki so'zning ohiri WORD\b bilan tugovchi. |

Quantifier-lar miqdorni belgilaydi:

| Quantifier | Ta'rif                                                                                              |
| ---------- | --------------------------------------------------------------------------------------------------- |
| n+         | Kamida bitta n ni o'z ichiga olgan har qanday stringga mos keladi                                   |
| n\*        | n ning nol marta yoki undan ko'proq takrorlanishini o'z ichiga olgan har qanday stringga mos keladi |
| n?         | n ning nol yoki bitta takrorlanishini o'z ichiga olgan har qanday qatorga mos keladi                |

### RegExp obektidan foydalanish

JavaScript-da RegExp ob'ekti oldindan belgilangan xususiyatlar va usullarga ega muntazam ifoda ob'ektidir.

### test()dan foydalanish

Usul `test()`RegExp ifoda usuli hisoblanadi.

U naqsh uchun satrni qidiradi va natijaga qarab rost yoki noto'g'ri qaytaradi.

Quyidagi misol "e" belgisi uchun satrni qidiradi:

```
const pattern = /e/;
pattern.test("The best things in life are free!");
```

{% code title="Satrda "e" mavjud bo'lganligi sababli, yuqoridagi kodning chiqishi quyidagicha bo'ladi:" %}
```
true
```
{% endcode %}

Avval o'zgaruvchiga muntazam ifodani qo'yish shart emas. Yuqoridagi ikkita qatorni bittaga qisqartirish mumkin:

```
/e/.test("The best things in life are free!");
```

### exec() dan foydalanish

Usul `exec()`RegExp ifoda usuli hisoblanadi.

U belgilangan naqsh uchun satrni qidiradi va topilgan matnni ob'ekt sifatida qaytaradi.

Agar moslik topilmasa, u bo'sh _(null)_ ob'ektni qaytaradi.

Quyidagi misol "e" belgisi uchun satrni qidiradi:

```
/e/.exec("The best things in life are free!");
```

### RegExp ma'lumotnomasini to'ldiring

[To'liq ma'lumot olish uchun bizning JavaScript RegExp to'liq ma'lumotnomamizga](https://www-w3schools-com.translate.goog/jsref/jsref\_obj\_regexp.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) o'ting .

Ma'lumotnomada barcha RegExp xususiyatlari va usullarining tavsiflari va misollari mavjud.
