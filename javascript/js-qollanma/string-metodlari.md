# String metodlari

{% hint style="success" %}
String length                                                   String trim()\
String slice()                                                   String trimStart()\
String substring()                                           String trimEnd()\
String substr()                                                String padStart()\
String replace()                                              String padEnd()\
String replaceAll()                                          String charAt()\
String toUpperCase()                                    String charCodeAt()\
String toLowerCase()                                    String split()\
String concat()
{% endhint %}

{% hint style="warning" %}
## Eslatma

Stringni qidirish metodlari keyingi bo'limda ko'rib chiqiladi.
{% endhint %}

### JavaScriptda string uzunligi

`length` xususiyati string uzunligini qaytaradi:

```javascript
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_length" %}

### String qismlarini ajratib olish

Stringning bir qismini ajratib olishning 3 ta usuli mavjud:

* <mark style="color:red;">`slice(start,`</mark><mark style="color:red;">` `</mark>_<mark style="color:red;">`end)`</mark>_
* <mark style="color:red;">`substring(`</mark>_<mark style="color:red;">`start`</mark>_<mark style="color:red;">`,`</mark><mark style="color:red;">` `</mark>_<mark style="color:red;">`end`</mark>_<mark style="color:red;">`)`</mark>
* <mark style="color:red;">`substr(`</mark>_<mark style="color:red;">`start`</mark>_<mark style="color:red;">`,`</mark><mark style="color:red;">` `</mark>_<mark style="color:red;">`length`</mark>_<mark style="color:red;">`)`</mark>

### String slice()

`slice()` strigning bir qismini ajratadi va ajratilgan qismni yangi stringda qaytaradi.

Metod ikkita parametr qabul qiladi: boshlang'ich nuqta va oxirgi index:

{% code title="Stringning 7-indexdan 13-indexgacha bo'lgan qismini kesib olish:" %}
```javascript
let text = "Apple, Banana, Kiwi";
let part = text.slice(7, 13);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_slice" %}

{% hint style="warning" %}
### Eslatma

JavaScript indexlarni noldan boshlab sanaydi.

Birinchi index 0.

Ikkinchi index esa - 1.
{% endhint %}

{% code title="Agar siz ikkinchi parametrni kiritmasangiz, metod stringning qolgan qismini kesib oladi:" %}
```javascript
let text = "Apple, Banana, Kiwi";
let part = text.slice(7);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_slice_rest" %}

{% code title="Agar parametr manfiy qilib berilsa, indexni hisoblash string oxiridan boshlanadi:" %}
```javascript
let text = "Apple, Banana, Kiwi";
let part = text.slice(-12);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_slice_rest_negative" %}

{% code title="Ushbu misol stringning bir qismini -12 indexdan -6 indexgacha kesib oladi:" %}
```javascript
let text = "Apple, Banana, Kiwi";
let part = text.slice(-12, -6);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_slice_negative" %}

### String substring()

`substring()` `slice()` ga o'xshaydi.

Uning farqi shundaki, `substring()` da 0 dan kichik bo'lgan boshlang'ich index va oxirgi index raqamlarni  0 sifatida qabul qilinadi.

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substring(7, 13);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_substring" %}

Agar siz ikkinchi parametrni kiritmasangiz, `substring()` stringning qolgan qismini qaytaradi.

### JavaScript String substr()

`substr()` `slice()` ga o'xshaydi.

Uning farqi shundaki, ikkinchi parametrga oxirgi indexni emas qaytarilishi kerak bo'lgan matnning uzunligi beriladi.

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substr(7, 6);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_substr" %}

Agar ikkinchi parametrni kiritmasangiz, `substr()` stringning qolgan qismini qaytaradi.

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substr(7);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_substr1" %}

Agar birinchi parametr manfiy qilib berilsa, index stringning oxiridan boshlab hisoblanadi.

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substr(-4);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_substr2" %}

### String tarkibini almashtirish

`replace()`  metodi belgilangan qiymatni stringdagi boshqa qiymat bilan almashtiradi:

```javascript
let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_replace" %}

{% hint style="warning" %}
### Eslatma

`replace()` metodi berilgan stringni o'zgartirmaydi.

`replace()` metodi yangi string qaytaradi.

`replace()` metodi faqat birinchi topilgan matnni almashtiradi

Agar siz barcha mos keladigan matnlarni almashtirmoqchi bo'lsangiz, /g  flag-i yordamida RegEx-dan foydalaning. Quyidagi misollarga qarang.
{% endhint %}

Defult tarzda, `replace()` metodi berilgan matnga mos keluvchi birinchi topilgan matnni almashtiradi

```javascript
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_replace_first" %}

Defult tarzda, `replace()` metodi katta-kichik harflarga e'tibor qaratadi. MICROSOFT (katta harf bilan) yozish ishlamaydi:

```javascript
let text = "Please visit Microsoft!";
let newText = text.replace("MICROSOFT", "W3Schools");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_replace_case" %}

Katta-kichik harflarni o'zgartirish uchun `/i` bilan **RegEx-**dan foydalaning:

```javascript
let text = "Please visit Microsoft!";
let newText = text.replace(/MICROSOFT/i, "W3Schools");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_replace_insensitive" %}

{% hint style="warning" %}
### Eslatma

Regex-lar tinish belgilarisiz yoziladi.
{% endhint %}

Berilgan matnga mos keluvchi matnlarning barchasini almashtirish uchun `/g` belgisi yordamida **RegEx**-dan foydalaning (global mos):

```javascript
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace(/Microsoft/g, "W3Schools");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_replace_global" %}

{% hint style="warning" %}
### Eslatma

RegEx haqida [JavaScriptda RegEx](regexp.md) bo'limida batafsil bilib olasiz.
{% endhint %}

### String ReplaceAll()

2021 yilda JavaScript `replaceAll()` metodini taqdim qildi:

```javascript
text = text.replaceAll("Cats","Dogs");
text = text.replaceAll("cats","dogs");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_replaceall" %}

`replaceAll()` metodi RegEx o'rniga, mos keluvchi barcha stringlarni almashtirish imkonini beradi.

Agar parametr RegEx bo'lsa, global argument (g) berilishi kerak, aks holda TypeError yuzaga keladi

```javascript
text = text.replaceAll(/Cats/g,"Dogs");
text = text.replaceAll(/cats/g,"dogs");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_replaceall2" %}

{% hint style="warning" %}
### Eslatma

`replaceAll()`[ES2021](../js-versiyalari/js-2021-2022.md) taqdim qilgan xususiyat hisoblanadi.

`replaceAll()`Internet Explorer-da ishlamaydi.
{% endhint %}

### Katta va kichik harflarga o'girish

Stringni`toUpperCase()` yordamida katta harfga aylantiriladi:

Stingni `toLowerCase()` yordamida kichik harfga aylantiriladi:

***

### String toUpperCase()

```javascript
let text1 = "Hello World!";
let text2 = text1.toUpperCase();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_toupper" %}

### String toLowerCase()

```javascript
let text1 = "Hello World!";       // String
let text2 = text1.toLowerCase();  // text2-ga text1 ning kichik harflarga o'tkazilgan shakli tayinlanadi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_tolower" %}

### String concat()

`concat()` metodi ikki yoki undan ortiq stringlarni birlashtiradi:

```javascript
let text1 = "Hello";
let text2 = "World";
let text3 = text1.concat(" ", text2);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_concat" %}

`concat()` metodini `+` operatorining o'rniga ishlatish mumkin.&#x20;

```javascript
text = "Hello" + " " + "World!";
text = "Hello".concat(" ", "World!");
```

{% hint style="warning" %}
### Eslatma

Barcha string metodlar yangi string qaytaradi. Ular asl stringni o'zgartirmaydi.

Stringlar o'zgarmasdir: stringlarni o'zgartirib bo'lmaydi, faqat almashtiriladi.
{% endhint %}

### String trim()

&#x20;`trim()` metodi stringning ikkala tomonidagi bo'sh joyni olib tashlaydi:

```javascript
let text1 = "      Hello World!      ";
let text2 = text1.trim();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_trim" %}

### String trimStart()

**ECMAScript 2019** JavaScript-ga `trimStart()`ni qo'shdi.

`trimStart()` metodi `trim()` metodi kabi ishlaydi, lekin bo'sh joyni faqat stringning boshidan olib tashlaydi.

```javascript
let text1 = "     Hello World!     ";
let text2 = text1.trimStart();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_trimstart" %}

JavaScriptda `trimStart()` metodi 2020-yil yanvar oyidan boshlab barcha brauzerlarda qo‘llab-quvvatlanadi:

| Chrome    | Edge     | Firefox    | Safari    |          |
| --------- | -------- | ---------- | --------- | -------- |
| Chrome 66 | Edge 79  | Firefox 61 | Safari 12 | Opera 50 |
| Apr 2018  | Jan 2020 | Jun 2018   | Sep 2018  | May 2018 |

### String trimEnd()

**ECMAScript 2019** JavaScript-ga String `trimEnd()` metodini ham qo'shdi.

`trimEnd()` metodi `trim()` kabi ishlaydi, lekin bo'sh joyni faqatgina stringning  oxiridan olib tashlaydi.

```javascript
let text1 = "     Hello World!     ";
let text2 = text1.trimEnd();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_trimend" %}

JavaScriptda String `trimEnd()` metodi 2020-yil yanvar oyidan boshlab barcha brauzerlarda qo‘llab-quvvatlanadi:

| Chrome    | Edge     | Firefox    | Safari    |          |
| --------- | -------- | ---------- | --------- | -------- |
| Chrome 66 | Edge 79  | Firefox 61 | Safari 12 | Opera 50 |
| Apr 2018  | Jan 2020 | Jun 2018   | Sep 2018  | May 2018 |

### String Padding

**ECMAScript 2017** ikkita `padStart()`va `padEnd()` metodlarini qo'shdi: string boshida va oxirida uni to'ldirib turishni qo'llab-quvvatlash uchun.

### String padStart()

`padStart()` metodi stringni berilgan boshqa string bilan to'ldiradi:

```javascript
let text = "5";
let padded = text.padStart(4,"0");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_padding1" %}

```javascript
let text = "5";
let padded = text.padStart(4,"x");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_padding4" %}

{% hint style="warning" %}
### Eslatma

`padStart()` metodi string metodi hisoblanadi.

Raqamni toʻldirish uchun avval uni stringga o'tkazing.

Quyidagi misolga qarang.
{% endhint %}

```javascript
let numb = 5;
let text = numb.toString();
let padded = text.padStart(4,"0");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_padding4" %}

### Brauzerning qo'llab-quvvatlashi

`padStart()` **ECMAScript 2017**ning xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`padStart()` Internet Explorer-da qo'llab-quvvatlanmaydi.

### String padEnd()

`padEnd()` metodi stingning ohirini berilgan boshqa string bilan to'ldiradi:

```javascript
let text = "5";
let padded = text.padEnd(4,"0");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_padding2" %}

```javascript
let text = "5";
let padded = text.padEnd(4,"x");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_padding6" %}

{% hint style="warning" %}
### Eslatma

`padEnd()` metodi string metodi hisoblanadi.

Raqamni toʻldirish uchun avval uni stringga o'tkazing.

Quyidagi misolga qarang.
{% endhint %}

```javascript
let numb = 5;
let text = numb.toString();
let padded = text.padEnd(4,"0");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_padding5" %}

### Brauzerning qo'llab-quvvatlashi

`padEnd()` **ECMAScript 2017**ning xususiyati hisoblanadi.

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`padEnd()` Internet Explorer-da qo'llab-quvvatlanmaydi.

### String belgilarini ajratib olish

String belgilarini ajratib olishning 3 ta usuli mavjud:

* `charAt(`_`index`_`)`
* `charCodeAt(`_`index`_`)`
* Xususiyat murojaat qilish \[ ]

### String charAt()

`charAt()` metodi stringdagi belgilangan index (pozitsiya)dagi belgini qaytaradi:

```javascript
let text = "HELLO WORLD";
let char = text.charAt(0);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_charat" %}

### String charCodeAt()

`charCodeAt()` metodi stringda belgilangan indexdagi belgining unikodini qaytaradi:

Metod UTF-16 kodini qaytaradi (0 dan 65535 gacha bo'lgan butun son).

```javascript
let text = "HELLO WORLD";
let char = text.charCodeAt(0);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_charat" %}

### Murojaat qilish xususiyati

**ECMAScript 5** (2009) stringlarga \[ ] murojaat qilish xususiyatinia berdi:

```javascript
let text = "HELLO WORLD";
let char = text[0];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_prop" %}

{% hint style="warning" %}
### Eslatma

Murojaat qilish xususiyatining qiymati oldindan aytib bo'lmaydigan qiymat bo'lishi mumkin:

* Bu stringlarni massivlarga o'xshatadi (lekin massiv emas)
* Hech qanday belgi topilmasa, \[ ] `undefined` qaytaradi, charAt() esa bo'sh qatorni qaytaradi.
* Uni faqat o'qish mumkin. str\[0] = "A" xato bermaydi (lekin ishlamaydi!)
{% endhint %}

```javascript
let text = "HELLO WORLD";
text[0] = "A";    // Xatolik chiqmaydi lekin ishlamaydi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_prop2" %}

### Stringni massivga aylantirish

Agar siz string bilan massiv sifatida ishlamoqchi bo'lsangiz, uni massivga aylantirishingiz mumkin.

### String split()

Stringni `split()` metodi yordamida massivga aylantirish mumkin:

```javascript
text.split(",")    // Vergullargacha bo'lgan qismlarni alohida massiv qilib kesadi
text.split(" ")    // Bo'sh joyni kesadi
text.split("|")    // Pipe ni kesadi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_split" %}

Agar qavs ichiga hech nima kiritilmasa, qaytarilgan massiv butun qatorni \[0] indeksidan boshlab o'z ichiga oladi.

Agar faqat "" berilsa, qaytarilgan massivda bittalik belgilar bo'ladi:

```javascript
text.split("")
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_split_char" %}

{% hint style="warning" %}
### String haqida to'liq ma'lumotnoma

String haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda string haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_string.asp)

Ma'lumotnomada barcha string xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
