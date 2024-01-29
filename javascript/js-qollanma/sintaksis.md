---
description: >-
  JavaScript sintaksisi - bu JavaScript kodlar qanday yozilishi kerakligini
  belgilovchi qoidalari to'plami:
---

# Sintaksis

```javascript
// O'zgaruvchi qanday yaratiladi:
var x;
let y;

// O'zgaruvchidan qanday foydalaniladi:
x = 5;
y = 6;
let z = x + y;
```

## Javascript qiymatlari

JavaScript sintaksisi ikki turdagi qiymatlarni belgilaydi:

* Fixed qiymatlar
* O'zgaruvchan qiymatlar

Fixed qiymatlar **literal**lar deb ataladi.

O'zgaruvchan qiymatlar **o'zgaruvchilar** deb ataladi.

### JavaScript literallari

Fixed qiymatlar uchun ikkita eng muhim sintaksis qoidalari:

1\. **Raqamlar** o‘nli yoki o‘nli kasrsiz yoziladi:

```
10.50

1001
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_numbers" %}

2\. **Stringlar** qo'shtirnoq yoki bir tirnoq ichida yozilgan matndir:

```
"John Doe"

'John Doe'
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_strings" %}

## JavaScript o'zgaruvchilari

Dasturlash tilida **o'zgaruvchilar** ma'lumotlar qiymatlarini saqlash uchun ishlatiladi.

JavaScript **o'zgaruvchi**larni e'lon qilish uchun  **`var`**, **`let`** va **`const`**  kalit so'zlaridan foydalanadi.

O'zgaruvchilarga **qiymat** berish uchun = belgisi ishlatiladi.

Ushbu misolda `x` nomli o'zgaruvchi e'lon qilinadi. Keyin `x` ga 6 qiymati beriladi:

```
let x;
x = 6;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_variables" %}

## JavaScript operatorlari

JavaScript qiymatlarni hisoblash uchun **arifmetik operatorlar**dan ( `+` `-` `*` `/`) foydalanadi:

```
(5 + 6) * 10
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_operators" %}

JavaScript o'zgaruvchilarga qiymatlarni belgilash uchun **tayinlash operatoridan** ( `=`) foydalanadi:

```
let x, y;
x = 5;
y = 6;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_assign" %}

## JavaScript ifodalari

{% hint style="warning" %}
Dasturlash  sohasining o'zbek auditoriyasida **ifoda** so'zi keng tarqalmaganligi va dasturlash sohasiga tegishli terminlarni o'z nomi bilan atashlik maqsadga muvofiqligi sababli **ifoda** so'zini bildiruvchi expression (ekspreshshn) atamasini o'z nomi bilan ataymiz.
{% endhint %}

Expression bu ma'lum bir kombinatsiyalarni hisoblaydigan qiymatlar, o'zgaruvchilar va operatorlarning birikmasidir.

```
5 * 10
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_expressions" %}

Expressionlar o'zgaruvchi qiymatlarni ham o'z ichiga olishi mumkin:

```
x * 10
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_expressions_variables" %}

Qiymatlar turli xil bo'lishi mumkin, masalan, raqamlar va stringlar.

Masalan, **"John" + " " + "Doe"**, "_John Doe_" deb hisoblanadi:

```
"John" + " " + "Doe"
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_expressions_strings" %}

## JavaScript kalit so'zlari

JavaScript **kalit so'zlari** bajariladigan amalni ifodalash uchun ishlatiladi.

`let` kalit so'zi brauzerga o'zgaruvchilar yaratishni aytadi:

```
let x, y;
x = 5 + 6;
y = x * 10;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_let" %}

`var` kalit so'zi ham brauzerga o'zgaruvchilar yaratishni aytadi:

```
var x, y;
x = 5 + 6;
y = x * 10;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_keywords" %}

{% hint style="warning" %}
Ushbu misollardagi `var`yoki `let` dan foydalanilganda natija bir xil bo'ladi.

`var` va `let` haqida keyinroq batafsil bilib olasiz.
{% endhint %}

## JavaScriptda izohlar

Hech qaysi steytmentlar "bajarilmaydi".

Kodning oldidan 2 talik **//** belgi yoki `/*` va `*/` ning orasida yozilgan kodlar izoh deb qabul qilinadi.

Izohlar e'tiborga olinmaydi va bajarilmaydi:

```
let x = 5;   // Ishlaydi

// x = 6;   Ishlamaydi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_comments" %}

{% hint style="warning" %}
Keyingi bo'limda izohlar haqida ko'proq bilib olasiz.
{% endhint %}

## Identifikatorlar/Nomlar

Identifikatorlar biror bir nom hisoblanadi.

Identifikatorlar o'zgaruvchilar va kalit so'zlar va funksiyalarni nomlash uchun ishlatiladi.

To'g'ri nom berish qoidalari boshqa dasturlash tillar bilan bir xil.

JavaScriptda nom berish quyidagilar bilan boshlanishi kerak:

* Harf (AZ yoki az)
* Dollar belgisi ($)
* Yoki pastki chiziq (\_)

Ushbu belgilardan keyingi belgilar harf, raqam, pastki chiziq yoki dollar belgisi bo'lishi mumkin.

{% hint style="warning" %}
### Eslatma

Nom berishda birinchi belgi sifatida raqamlardan foydalanib bo'lmaydi

Shu orqali JavaScript berilgan nomni raqamlardan osongina farqlab oladi.
{% endhint %}

## JavaScript case sensitive hisonlanadi

{% hint style="warning" %}
Case Sensitive bu harflarning katta kichikligiga etibor qilishdir.&#x20;
{% endhint %}

Barcha JavaScript identifikatorlari **case sensitive** hisonlanadi.&#x20;

`lastName` va `lastname` o'zgaruvchilari ikki xil o'zgaruvchilar hisoblanadi:

```
let lastname, lastName;
lastName = "Doe";
lastname = "Peterson";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_syntax_case" %}

JavaScript LET yoki Let ni `let` kalit so'zi sifatida qabul qilmaydi.

## JavaScript va Camel Case

Dasturchilar azaldan bir nechta so'zlardan iborat o'zgaruvchini bitta o'zgaruvchi nomiga birlashtirishning turli usullaridan foydalanganlar:

**Chiziqlar:**

first-name, last-name, master-card, inter-city

{% hint style="warning" %}
JavaScript-da chiziqdan foydalanib bo'lmaydi. Ular ayirish amallari uchun belgilab qo'yilgan.
{% endhint %}

**Pastki chiziq:**

first\_name, last\_name, master\_card, inter\_city.

**Katta Camel Case (Paskal Case):**

FirstName, LastName, MasterCard, InterCity.

**Kichik Camel Case:**

JavaScript dasturchilari odatda kichik harf bilan boshlanadigan camel case usuidan foydalanadilar:

firstName, lastName, masterCard, interCity.

## JavaScript belgilar to'plami

JavaScript **Unicode** belgilar to'plamidan foydalanadi.

Unicode (deyarli) dunyodagi barcha belgilarni, tinish belgilarini va simvollarni o'z ichiga oladi.

Batafsil ma'lumot olish uchun bizning [Unicode ma'lumotnomamizni ](https://www.w3schools.com/charsets/ref\_html\_utf8.asp)o'rganing.
