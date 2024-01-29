# String qidiruvi

{% hint style="success" %}
### JavaScript qidiruv metodlari

* String indexOf()
* String lastIndexOf()
* String search()
* String match()
* String matchAll()
* String includes()
* String startsWith()
* String endsWith()
{% endhint %}

### String indexOf()

`indexOf()` metodi stringdagi matnning birinchi topilgan indeksini (joylashuvini) qaytaradi:

```javascript
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_indexof" %}

{% hint style="warning" %}
### Eslatma

JavaScript indexlarni noldan boshlab sanaydi.

0 - stringning birinchi indexi, 1 - ikkinchi, 2 - uchinchi, ...
{% endhint %}

### String lastIndexOf()

`lastIndexOf()`  metodi stringda belgilangan matnning oxirgi aniqlangan **indexini** qaytaradi:

```javascript
let text = "Please locate where 'locate' occurs!";
text.lastIndexOf("locate");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_lastindexof" %}

`indexOf()`va `lastIndexOf()`ning har ikkisida, agar matn topilmasa, -1 qaytariladi:

```javascript
let text = "Please locate where 'locate' occurs!";
text.lastIndexOf("John");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_indexof_1" %}

Ikkala metod ham qidiruv uchun boshlang'ich index sifatida ikkinchi parametrni qabul qiladi:

```javascript
let text = "Please locate where 'locate' occurs!";
text.indexOf("locate", 15);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_indexof_2" %}

`lastIndexOf()` metodi matnning oxiridan boshiga qarab qidiradi, ya'ni: agar ikkinchi parametr  `15`bo'lsa , qidiruv 15-indexdan boshlanadi va stringning boshigacha qidiradi.

```javascript
let text = "Please locate where 'locate' occurs!";
text.lastIndexOf("locate", 15);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_lastindexof_2" %}

### String search()

`search()` metodi stringni qidiradi va mos keladigan indexni qaytaradi:

```javascript
let str = "Please locate where 'locate' occurs!";
str.search("locate");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_search_locate" %}

```javascript
let str = "Please locate where 'locate' occurs!";
str.search(/locate/);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_search_locate2" %}

### E'tibor berdingizmi ?

`indexOf()` va `search()` metodlari bir xilmi ?

Ular bir xil parametrlarni qabul qiladi va bir xil qiymatni qaytaradimi ?

Bu ikki metod bir xil emas. Ularning farqi:

* `search()` metodi ikkinchi argument qabul qila olmaydi.
* `indexOf()` metodi RegEx qiymatlarini qabul qila ololmaydi.

RegEx haqida keyingi bo'limda batafsil bilib olasiz.

### String match()

`match()` metodi berilgan stringga mos keluvchi qiymatni o'z ichiga olgan massivni qaytaradi.

{% code title=""Ain" uchun qidiruvni amalga oshirish:" %}
```javascript
let text = "The rain in SPAIN stays mainly in the plain";
text.match("ain");
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_match" %}

{% code title=""Ain" uchun qidiruvni amalga oshiring:" %}
```javascript
let text = "The rain in SPAIN stays mainly in the plain";
text.match(/ain/);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_match_regexp3" %}

{% code title=""Ain" uchun global qidiruvni amalga oshiring:" %}
```javascript
let text = "The rain in SPAIN stays mainly in the plain";
text.match(/ain/g);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_match_regexp" %}

{% code title=""ain" uchun global, katta-kichik harflarsiz qidiruvni amalga oshiring:" %}
```
let text = "The rain in SPAIN stays mainly in the plain";
text.match(/ain/gi);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_match_regexp2" %}

{% hint style="warning" %}
### Eslatma

_Agar RegExpda  g_ modifikatori bo'lmasa `match()` stringdagi faqat birinchi mos kelgan qiymatni qaytaradi.

[JS RegExp](https://www.w3schools.com/js/js\_regexp.asp) bo'limida u haqida batafsil o'qing.
{% endhint %}

### String matchAll()

`matchAll()` metodi berilgan stringga mos keluvchi barcha matnlarni o'z ichiga olgan iteratorni qaytaradi.

```javascript
const iterator = text.matchAll("Cats");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_matchall" %}

Agar parametr RegEx bo'lsa, global argument (g) berilishi kerak, aks holda TypeError yuzaga keladi.

```javascript
const iterator = text.matchAll(/Cats/g);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_matchall2" %}

Agar siz katta-kichik harflarga etibor qilmasdan qidirishni istasangiz, i belgisini kiritishingiz kerak:

```javascript
const iterator = text.matchAll(/Cats/gi);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_matchall3" %}

{% hint style="warning" %}
### Eslatmalar

`matchAll()`[ES2020](https://www.w3schools.com/js/js\_2020.asp)ning xususiyati hisoblanadi.

`matchAll()` Internet Explorer-da ishlamaydi.
{% endhint %}

### String includes()

Agar stringda berilgan matn  mavjud bo'lsa, `includes()` metodi  "true"  qaytaradi.

Aks holda `false` qaytariladi.

{% code title="Stringda "world" so'zi mavjudligini tekshiring:" %}
```javascript
let text = "Hello world, welcome to the universe.";
text.includes("world");
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_includes" %}

{% code title="Stringda "world" so'zi mavjudligini tekshiring. 12-indeksdan boshlang:" %}
```javascript
let text = "Hello world, welcome to the universe.";
text.includes("world", 12);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_includes2" %}

{% hint style="warning" %}
### Eslatmalar

`includes()`katta-kichik harflarga e'tibor beradi.

`includes()`[ES6](https://www.w3schools.com/js/js\_es6.asp) ning xususiyati hisoblanadi.

`includes()` Internet Explorer-da qo'llab-quvvatlanmaydi.
{% endhint %}

### String startsWith()

Agar string berilgan matndan boshlansa, `startsWith()` metodi `true` qaytaradi.

Aks holda `false` qaytariladi:

{% code title="True qaytaradi:" %}
```javascript
let text = "Hello world, welcome to the universe.";
text.startsWith("Hello");
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_startswith" %}

{% code title="False qaytaradi:" %}
```javascript
let text = "Hello world, welcome to the universe.";
text.startsWith("world")
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_startswith4" %}

Qidiruv uchun boshlang'ich index haam berilishi mumkin:

{% code title="False qaytaradi:" %}
```javascript
let text = "Hello world, welcome to the universe.";
text.startsWith("world", 5);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_startswith3" %}

{% code title="True qaytaradi:" %}
```javascript
let text = "Hello world, welcome to the universe.";
text.startsWith("world", 6);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_startswith2" %}

{% hint style="warning" %}
### Eslatmalar

`startsWith()`katta-kichik harflaga e'tibor beradi.

`startsWith()`[ES6](https://www.w3schools.com/js/js\_es6.asp) ning xususiyati hisoblanadi.

`startsWith()` Internet Explorer-da qo'llab-quvvatlanmaydi.
{% endhint %}

### String endsWith()

Agar string berilgan matn bilan tugasa, `endsWith()`  metodi `true`  qaytariladi.

Aks holda `false` qaytariladi:

{% code title="String  "Doe" so'zi bilan tugashini tekshiring:" %}
```javascript
let text = "John Doe";
text.endsWith("Doe");
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_endswith" %}

Stringning 11-indexidagi matn "world" so'zi bilan tugashini tekshiring:

<pre class="language-javascript"><code class="lang-javascript"><strong>let text = "Hello world, welcome to the universe.";
</strong>text.endsWith("world", 11);
</code></pre>

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_endswith2" %}

{% hint style="warning" %}
### Eslatmalar

`endsWith()`katta-kichik harflaga e'tibor beradi.

`endsWith()`[ES6](https://www.w3schools.com/js/js\_es6.asp) ning xususiyati hisoblanadi.

`endsWith()` Internet Explorer-da qo'llab-quvvatlanmaydi.
{% endhint %}

{% hint style="warning" %}
### String haqida to'liq ma'lumotnoma

String haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda string haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_string.asp)

Ma'lumotnomada barcha string xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
