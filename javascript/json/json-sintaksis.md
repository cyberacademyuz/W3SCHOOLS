---
description: JSON sintaksisi JavaScript sintaksisining kichik to'plamidir.
---

# JSON Sintaksis

### JSON Sintaktik qoidalar

JSON sintaksisi obyektning tuzilish sintaksisidan olingan:

* Ma'lumotlar nom/qiymat juftligida bo'ladi
* Ma'lumotlar vergul bilan ajratiladi
* Jingalak qavslar ma'umotlarni saqlaydi
* Kvadrat qavslar massivlarni saqlaydi

### JSON ma'lumotlari - Nom va Qiymat

JSON ma'lumotlari nom/qiymat juftligi (kalit/qiymat juftligi) sifatida yoziladi.

Nom/qiymat juftligi nom maydonidan (qo'shtirnoq ichida), undan keyin ikki nuqta va qiymatdan iborat:

```
"name":"John"
```

{% hint style="warning" %}
JSON nomlarida qo'shtirnoq talab qilinadi.
{% endhint %}

### JSON - JavaScript obyektlarini baholaydi

JSON formati JavaScript obyektlari bilan deyarli bir xil.

JSON-da _kalitlar_ qo'shtirnoq bilan yozilgan stringlardan iborat bo'lishi kerak:

{% code title="JSON" %}
```
{"name":"John"}
```
{% endcode %}

JavaScript-da kalitlar string, raqam yoki identifikatsiya nomi bo'lishi mumkin:

{% code title="JavaScript" %}
```
{name:"John"}
```
{% endcode %}

### JSON qiymatlari

**JSON** da qiymatlar quyidagi ma'lumot turlaridan biri bo'lishi kerak_:_

* string
* raqam
* obyekt
* massiv
* boolean
* null

**JavaScript**da qiymatlar yuqoridagi barcha qiymatlar, va hatto boshqa har qanday JavaScript steytmentini o'z ichiga ola oladi:

* funksiya
* sana
* undefined

JSON-da _string qiymatlari_ qo'shtirnoq bilan yozilishi kerak:

{% code title="JSON" %}
```
{"name":"John"}
```
{% endcode %}

JavaScript-da qo'shtirnoqli yoki birtirnoqli string qiymatlarini yozishingiz mumkin:

{% code title="JavaScript" %}
```
{name:'John'}
```
{% endcode %}

### JavaScript obyektlari

JSON sintaksisi obyekt tuzilishidan olinganligi sababli, JavaScript ichida JSON bilan ishlash uchun juda kam qo'shimcha dastur kerak bo'ladi.

JavaScript yordamida obyekt yaratishingiz va unga ma'lumotlar berishingiz mumkin, masalan:

```
person = {name:"John", age:31, city:"New York"};
```

JavaScript obyektiga quyidagi kabi murojaat qilish mumkin:

```
// returns John
person.name;
```

Unga quyidagi tarzda murojaat qilish ham mumkin:

```
// returns John
person["name"];
```

Ma'lumotlarni quyidagicha o'zgartirish mumkin:

```
person.name = "Gilbert";
```

Shuningdek, u quyidagicha o'zgartirilishi mumkin:

```
person["name"] = "Gilbert";
```

Keyinchalik ushbu qo'llanmada JavaScript obyektlarini JSONga qanday aylantirishni bilib olasiz.

### Massivlardan JSON sifatida foydalanish

Obyektlar JSON sifatida yozilishi mumkin bo'lgani kabi massivlari ham JSON sifatida yozilishi mumkin.

Keyinchalik ushbu qo'llanmada obyektlar va massivlar haqida batafsil bilib olasiz.

### JSON fayllari

* JSON faylining fayl turi ".json"
* JSON matni uchun MIME turi "application/json"
