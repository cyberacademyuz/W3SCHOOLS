# Stringlar

{% hint style="success" %}
Stringlar matnni saqlash va boshqarish uchun mo'ljallangan.
{% endhint %}

JavaScriptda string tinish belgilari ichida yozilgan belgilardir.

```javascript
let text = "John Doe";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string" %}

Siz bir tirnoqdan ham qo'shtirnoqdan ham foydalanishingiz mumkin:

```javascript
let carName1 = "Volvo XC60";  // Qo'shtirnoq
let carName2 = 'Volvo XC60';  // Birtirnoq
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_quotes" %}

Agar ular stringni o'rab turuvchi tinish belgi bilan mos kelmasa, string ichida qo'shtirnoqdan foydalanishingiz mumkin:

```javascript
let answer1 = "It's alright";
let answer2 = "He is called 'Johnny'";
let answer3 = 'He is called "Johnny"';
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_quotes_mixed" %}

### String uzunligi

String uzunligini topish uchun maxsusu `length` xususiyatidan foydalaning :

```javascript
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_length" %}

### Aylanib o'tuvchi belgilar

Stringlar tinish belgilarining ichida yozilishi kerakligi sababli, JavaScript bu stringni noto'g'ri tushunadi:

```javascript
let text = "We are the so-called "Vikings" from the north.";
```

Stringning "We are the so-called" qismi kesib olinadi.

Ushbu muammoni chetlab o'tishning yechimi backslash belgisidan foydalanishdir.

Backslash (`\`) belgisi maxsus belgilarni string belgilariga aylantiradi:

| Kod  | Natija | Ta'rif      |
| ---- | ------ | ----------- |
| \\'  | '      | Birtirnoq   |
| \\"  | "      | Qo'shtirnoq |
| \\\\ | \\     | Backslash   |

`\"`  ketma ketligi stringga qo'shtirnoq qo'shadi:

```javascript
let text = "We are the so-called \"Vikings\" from the north.";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_escape_quotes2" %}

`\'`  ketma ketligi stringga birtirnoq qo'shadi:

```javascript
let text= 'It\'s alright.';
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_escape_quotes1" %}

`\\`  ketma ketligi stringga backslash qo'yadi:

```javascript
let text = "The character \\ is called backslash.";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_escape_backslash" %}

JavaScript-da  yana shu kabi 6 ta belgilar ishlatiladi:

| Kod | Natija                            |
| --- | --------------------------------- |
| \b  | Backspace                         |
| \f  | Form Feed                         |
| \n  | Yangi qator                       |
| \r  | Carriage Return                   |
| \t  | Gorizontal 4 qator (tab) tashlash |
| \v  | Vertikal 4 qator tab tashlash     |

{% hint style="warning" %}
Yuqoridagi 6 ta escape belgilari dastlab yozuv mashinkalari, teletypelar va faks mashinalarini boshqarish uchun mo'ljallangan. Ular HTMLda hech nimani bildirmaydi.
{% endhint %}

### Uzun kodli strinlarni ikkiga bo'lish

Kodni o'qishni osonlashtirish uchun dasturchilar ko'pincha uzunroq kodning davomini 80ta belgidan keyin yangi qatordan yozishni yaxshi ko'radilar.

Agar JavaScript steytmenti bitta qatorga sig'masa, uni keyingi qatordan boshlash uchun eng yaxshi qism operatordan keyingi qism hisoblanadi:

```javascript
document.getElementById("demo").innerHTML =
"Hello Dolly!";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_statements_linebreak" %}

Bundan tashqari, kod qatoridagi string matnni bitta **backslash**dan foydalanib pastdan davom ettirishingiz mumkin:

```javascript
document.getElementById("demo").innerHTML = "Hello \
Dolly!";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_break" %}

{% hint style="warning" %}
`\` dan foydalanish usuli to'g'ri yechim bo'lmasligi mumkmin. U universal sifatida qo'llab-quvvatlanmasligi mumkin. Ba'zi brauzerlar `\` belgisidan keyin bo'sh joy qoldirishga imkon bermaydi.
{% endhint %}

Stringni ikkiga ajratishning xavfsizroq yo'li bu stringni qo'shishdan foydalanishdir:

<pre class="language-javascript"><code class="lang-javascript"><strong>document.getElementById("demo").innerHTML = "Hello " +
</strong>"Dolly!";
</code></pre>

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_break_ok" %}

Kod qatorini backslash bilan bo'la olmaysiz:

```javascript
document.getElementById("demo").innerHTML = \
"Hello Dolly!";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_strings_codebreak" %}

### Stringlarni obyektlar sifatida e'lon qilish

Odatda, stringlar harflardan yaratilgan oddiy qiymatlar hisoblanadi:

```javascript
let x = "John";
```

Ammo stringlarni `new` kalit so'zi bilan obyekt sifatida ham e'lon qilish mumkin:

```javascript
let y = new String("John");
```

```javascript
let x = "John";
let y = new String("John");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_object" %}

{% hint style="warning" %}
String bilan obyektlar yaratmang.

`new` kalit so'zi kodni murakkablashtiradi va bajarish tezligini sekinlashtiradi.

String orqali yaratilgan obyektlar kutilmagan natijalarga olib kelishi mumkin:
{% endhint %}

{% code title="== operatoridan foydalanganda x va y bir xil narsa:" %}
```javascript
let x = "John";
let y = new String("John");
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_object1" %}

{% code title="=== operatordan foydalanganda x va y bir xil emas:" %}
```javascript
let x = "John";
let y = new String("John");
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_object2" %}

{% hint style="warning" %}
`(x==y)`va `(x===y)` o'rtasidagi farqga e'tibor bering.
{% endhint %}

{% code title="(x == y) to'g'rimi yoki noto'g'ri ?" %}
```javascript
let x = new String("John");
let y = new String("John");
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_object3" %}

{% code title="(x === y) to'g'rimi yoki noto'g'ri?" %}
```javascript
let x = new String("John");
let y = new String("John");
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_string_object4" %}

{% hint style="warning" %}
Ikki obyektni solishtirganda har doim `false` qaytadi.
{% endhint %}

{% hint style="warning" %}
### String haqida to'liq ma'lumotnoma

String haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda string haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_string.asp)

Ma'lumotnomada barcha string xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
