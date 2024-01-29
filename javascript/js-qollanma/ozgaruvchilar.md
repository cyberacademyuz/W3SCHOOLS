# O'zgaruvchilar

{% hint style="success" %}
#### JavaScriptda o'zgaruvchilarni e'lon qilishning 4 ta yo'li

* `var` dan foydalanish
* `let` dan foydalanish
* `const` dan foydalanish
* hech narsadan foydalanmay
{% endhint %}

## O'zgaruvchilar nima ?

O'zgaruvchilar - ma'lumotlarni saqlash uchun konteyner hisoblanadi (ma'lumotlarning qiymatlarini saqlovchi).

Bu misolda , `x`, `y` va `z` o'zgaruvchilar bo'lib `var` kalit so'zi bilan e'lon qilingan:

```javascript
var x = 5;
var y = 6;
var z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_undeclared" %}

{% hint style="warning" %}
## Eslatma

O'zgaruvchidan foydalanishdan avval uni e'lon qilish best practice hisoblanadi.
{% endhint %}

* x 5 qiymatini saqlaydi
* y 6 qiymatini saqlaydi
* z 11 qiymatini saqlaydi

```javascript
var x = 5;
var y = 6;
var z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables" %}

{% hint style="warning" %}
## Var-ni qachon foydalanish kerak?

`var` kalit so'zi 1995 yildan 2015 yilgacha barcha JavaScript kodlarida qo'llanilgan.

`let` va `const` kalit so'zlari 2015 yilda JavaScriptga qo'shilgan.

Agar kodingiz eski brauzerlarda ham ishlashini istasangiz `var`dan foydalanishingiz kerak.
{% endhint %}

{% code title="let-dan foydalanishga misol" %}
```javascript
let x = 5;
let y = 6;
let z = x + y;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_let" %}

{% code title="" %}
```javascript
const x = 5;
const y = 6;
const z = x + y;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_const" %}

{% code title="Aralash misol:" %}
```javascript
const price1 = 5;
const price2 = 6;
let total = price1 + price2;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_total" %}

Ushbu misolda, `price1`, `price2` va `total` o'zgaruvchilar e'lon qilingan:

```javascript
const price1 = 5;
const price2 = 6;
let total = price1 + price2;
```

`price1` va `price2` o'zgaruvchilari `const` kalit so'zi bilan e'lon qilingan.

Bular doimiy qiymatlar va ularni o'zgartirib bo'lmaydi.

`total` o'zgaruvchisi `let` kalit so'zi bilan e'lon qilingan.

Bu o'zgartirilishi mumkin bo'lgan qiymat.

{% hint style="warning" %}
## var, let va const-dan qachon foydalaniladi ?

1\. Har doim o'zgaruvchilarni e'lon qilishda

2\. O'zgaruvchining qiymati o'zgarmasa har doim `const` bilan e'lon qiling&#x20;

3\. O'zgaruvchining turi o'zgarmasa har doim `const` bilan e'lon qiling (Arraylar va obyektlar)

4\. Agar const dan foydalana olmasangiz, `let`dan foydalaning

5\. Agar eski brauzerlarni qo'llab-quvvatlash kerak bo'lsa, `var`dan foydalaning.
{% endhint %}

## Xuddi algebra kabi

Xuddi algebrada bo'lgani kabi, o'zgaruvchilar ham qiymatlarga ega:

```javascript
let x = 5;
let y = 6;
```

Xuddi algebrada bo'lgani kabi, o'zgaruvchilar expressionlarda ishlatiladi:

```javascript
let z = x + y;
```

Yuqoridagi misolda z ning qiymati 11 ga teng ekanligini taxmin qilishingiz mumkin.

{% hint style="warning" %}
### Eslatma

O'zgaruvchilar qiymatlarni saqlash uchun konteynerlardir.
{% endhint %}

## JavaScript identifikatorlari

Barcha o'zgaruvchilar unikal nomlar bilan e'lon qilinishi kerak.

Ushbu unikal nomlar identifikatorlar deb ataladi.

Identifikatorlar **x** va **y** kabi qisqa yoki **age**, **sum**, **totalVolume** kabi batafsilroq bo'lishi mumkin.

O'zgaruvchilar (unikal identifikatorlar) uchun nom berishning umumiy qoidalari:

* O'zgaruvchi nomlari  harflardan, raqamlardan, pastki chiziq va dollar belgilaridan iborat bo'lishi mumkin.
* O'zgaruvchi nomlari harf bilan boshlanishi kerak.
* O'zgaruvchi nomlari $ va \_ bilan ham boshlanishi mumkin (lekin biz ushbu qo'llanmada bundan foydalanmaymiz).
* O'zgaruvchi nomlari katta-kichik harflarga farq qiladi (y va Y boshqa boshqa o'zgaruvchi hisoblanadi).
* Standart kalit so'zlar o'zgaruvchi nomi sifatida ishlatilmaydi.

{% hint style="warning" %}
### Eslatma

JavaScript identifikatorlari katta-kichik harflarga farq qiladi.
{% endhint %}

## Tayinlash operatori

JavaScript-da teng belgisi (`=`) "...ga teng" operatori emas, balki "tayinlash" operatoridir.

Bu algebradan farq qiladi. Quyidagi misol algebraga mos emas:

```javascript
x = x + 5
```

Biroq, JavaScript-da bu boshqacha: u `x` ga `x + 5` qiymatini tayinlaydi.

(U x + 5 qiymatini hisoblab chiqadi va natijani x ga tayinlaydi. X qiymati 5 ga oshiriladi)

{% hint style="warning" %}
### Eslatma

"...ga teng" operatori `==`JavaScript-dagi kabi yozilgan.
{% endhint %}

## JavaScript ma'lumotlar turlari

O'zgaruvchilar <mark style="color:blue;">100</mark> kabi raqamlarni va <mark style="color:orange;">"</mark><mark style="color:yellow;">Jon Doe</mark><mark style="color:orange;">"</mark> kabi matn qiymatlarini saqlashi mumkin.

Dasturlashda matn qiymatlari <mark style="color:yellow;">**string**</mark>lar deb ataladi.

JavaScript ko'p turdagi ma'lumotlar bilan ishlay oladi, ammo hozircha **raqamlar** va **stringlar** bilan cheklanadi.

Stringlar qo'shtirnoq yoki bir tirnoq ichida yoziladi. Raqamlar esa  yoziladi.

Agar siz raqamni qo'shtirnoq ichida yozsangiz u string sifatida qabul qilinadi.

{% code title="Misol:" %}
```javascript
const pi = 3.14;
let person = "John Doe";
let answer = 'Yes I am!';
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_types" %}

### JavaScript o'zgaruvchisini e'lon qilish

JavaScript-da o'zgaruvchi yaratish o'zgaruvchini "e'lon qilish" deb ataladi.

Siz JavaScript oʻzgaruvchisini `var` va `let` kalit soʻzlari bilan eʼlon qilasiz.

```javascript
var carName;
```

yoki:

```javascript
let carName;
```

O'zgaruvchi e'lon qilinganidan keyin uning qiymati yo'q (texnik jihatdan bu `undefined`).

O'zgaruvchiga qiymat berish uchun = belgisidan foydalaning:

```javascript
carName = "Volvo";
```

Siz o'zgaruvchini e'lon qilganingizda unga qiymat berib ketishingiz ham mumkin:

```javascript
let carName = "Volvo";
```

Quyidagi misolda biz `carName` nomli o'zgaruvchi yaratamiz va unga "Volvo" qiymatini beramiz.

Keyin HTMLning paragraf elementidagi id="demo" yordamida uni ekranga chiqaramiz:

```markup
<p id="demo"></p>

<script>
let carName = "Volvo";
document.getElementById("demo").innerHTML = carName;
</script>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_create" %}

{% hint style="warning" %}
### Eslatma

O'zgaruvchilarni script boshida e'lon qilish **good practice** hisoblanadi.
{% endhint %}

### Bir steytmentada bir nechta o'zgaruvchilar

Bir steytmentda ko'plab o'zgaruvchilar e'lon qilishingiz mumkin.

Steytmentni `let` bilan boshlang va o'zgaruvchilarni **vergul**  (`,`)  bilan ajrating :

```
let person = "John Doe", carName = "Volvo", price = 200;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_multi" %}

E'lon qilish bir nechta qatorlardan tashkil topshi mumkin:

```
let person = "John Doe",
carName = "Volvo",
price = 200;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_multiline" %}

### Qiymat = undefined

Kompyuter dasturlarida o'zgaruvchilar ko'pincha qiymatsiz e'lon qilinadi. O'zgaruvchining qiymati keyinchalik hisoblanishi kerak bo'lgan narsa yoki foydalanuvchi kiritadigan ma'lumot kabi keyinchalik beriladigan qiymat bo'lishi mumkin.

Qiymatsiz e'lon qilingan o'zgaruvchi `undefined` qiymatiga ega bo'ladi.

`CarName` o'zgaruvchisi ushbu steytment bajarilgandan keyin `undefined` qiymatiga ega bo'ladi :

```
let carName;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_undefined" %}

### JavaScript o'zgaruvchilarini qayta e'lon qilish

`var` bilan e'lon qilingan o'zgaruvchini qayta e'lon qilsangiz, u o'z qiymatini yo'qotmaydi.

Ushbu steytmentlar bajarilgandan keyin `carName` o'zgaruvchisi "Volvo" qiymatiga ega bo'ladi:

```javascript
var carName = "Volvo";
var carName;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_redefine" %}

{% hint style="warning" %}
### Eslatma

`let`yoki `const` bilan e'lon qilingan o'zgaruvchini qayta e'lon qila olmaysiz.

Bu ishlamaydi:

```javascript
let carName = "Volvo";
let carName;
```
{% endhint %}

### JavaScriptda arifmetika

Algebrada bo'lgani kabi `=` va `+` kabi operatorlardan foydalanib o'zgaruvchilar bilan arifmetik amallarni bajarishingiz mumkin:

```javascript
let x = 5 + 2 + 3;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_add_numbers" %}

Siz stringlarni ham qo'shishingiz mumkin, lekin stringlar birlashtiriladi:

```javascript
let x = "John" + " " + "Doe";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_add_strings" %}

Buni ham sinab ko'ring:

```javascript
let x = "5" + 2 + 3;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_add_string_number" %}

{% hint style="warning" %}
### Eslatma

Agar siz raqamni qo'shtirnoq ichida yozsangiz qolgan raqamlar string sifatida qabul qilinadi va birlashtiriladi.
{% endhint %}

Endi buni sinab ko'ring:

```
let x = 2 + 3 + "5";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_add_number_string" %}

### JavaScriptda $ belgisi

JavaScript, dollar belgisiga harf sifatida qaraganligi sababli, $ ni o'z ichiga olgan identifikatorlar to'g'ri nomdagi o'zgaruvchi hisoblanadi:

```javascript
let $ = "Hello World";
let $$$ = 2;
let $myMoney = 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_dollar" %}

Dollar belgisidan foydalanish JavaScript-da unchalik keng tarqalmagan, lekin professional dasturchilar uni JavaScript kutubxonasidagi asosiy funksiya uchun **alias** sifatida ishlatishadi.

Masalan, jQuery kutubxonasida HTML elementlarini tanlash uchun `$` main funksiyasidan foydalaniladi. jQuery da $("p"); "barcha p elementlarni tanlash" degan ma'noni anglatadi.

## JavaScriptda pastki chiziq (\_)

JavaScript pastki chiziqni harf sifatida qabul qilganligi sababli, \_ ni o'z ichiga olgan identifikatorlar to'g'ri nomdagi o'zgaruvchi hisoblanadi:

```javascript
let _lastName = "Johnson";
let _x = 2;
let _100 = 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_variables_underscore" %}

Pastki chiziqdan foydalanish JavaScript-da unchalik keng tarqalmagan, lekin professional dasturchilar oʻrtasidagi kelishuvga asosan uni “private (yashirin)” oʻzgaruvchilar uchun **alias** sifatida ishlatiladi.
