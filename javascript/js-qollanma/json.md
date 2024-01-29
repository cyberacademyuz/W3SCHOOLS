# JSON

JSON - bu ma'lumotlarni saqlash va uzatish uchun format hisoblanadi.

JSON ko'pincha ma'lumotlar serverdan veb-sahifaga yuborilganda ishlatiladi.

### JSON nima ?

* ‌JSON **J**ava **S**cript **O**bject **N**otation degan ma'noni anglatadi
* ‌JSON ma'lumotlar almashishning yengil formatidir
* JSON tildan mustaqil \*
* ‌JSON "o'zini tavsiflovchi" va uni tushunish oson

\* JSON sintaksisi JavaScriptning obyekt belgilari sintaksisidan olingan, ammo JSON formati faqat stringdan tashkil topadi. JSON ma'lumotlarini o'qish va yaratish uchun kodni har qanday dasturlash tilida yozish mumkin.

### JSONga misol

Ushbu JSON sintaksisi employees obyektini ifodalaydi: 3 ta xodim yozuvlari (ob'ektlar) massivi:

{% code title="JSONga misoli:" %}
```
{
"employees":[
  {"firstName":"John", "lastName":"Doe"},
  {"firstName":"Anna", "lastName":"Smith"},
  {"firstName":"Peter", "lastName":"Jones"}
]
}
```
{% endcode %}

### JSON formati JavaScript obyektlarini baholaydi

JSON formati sintaktik jihatdan JavaScript obyektlarini yaratuvchi kodning o'zginasi.

Ushbu o'xshashlik tufayli kodlar JSON ma'lumotlarini lokal JavaScript obyektlariga osongina aylantirishi mumkin.

### JSON sintaksisining qoidalari

* Ma'lumotlar nom/qiymat juftligida bo'ladi
* Ma'lumotlar vergul bilan ajratiladi
* Jingalak qavslar malumotlarni o'rab turadi
* Kvadrat qavslar massivlarni o'rab turadi

### JSON ma'lumotlari - nom va qiymat

JSON ma'lumotlari xuddi obyekt xususiyatlaridek nom/qiymat juftliklari kabi yoziladi.

Nom/qiymat juftligi nom yoziladigan maydon (ikki qo'shtirnoq ichida), ikki nuqta va undan keyin qiymatdan tashkil topgan:

```
"firstName":"John"
```

{% hint style="warning" %}
JSON ma'lumotlaridagi nomlar qo'shtirnoq ichida yozilishi talab qilinadi. JavaScript da nom berish esa bunday emas.
{% endhint %}

### JSON obektlari

JSON obyektlari jingalak qavslar ichida yoziladi.

Xuddi JavaScript-da bo'lgani kabi, obyektlarda bir nechta nom/qiymat juftligi bo'lishi mumkin:

```
{"firstName":"John", "lastName":"Doe"}
```

### JSON massivlari

JSON massivlari kvadrat qavslar ichida yoziladi.

Xuddi JavaScript-da bo'lgani kabi, massiv obektlarni ham o'z ichiga olishi mumkin:

```
"employees":[
  {"firstName":"John", "lastName":"Doe"},
  {"firstName":"Anna", "lastName":"Smith"},
  {"firstName":"Peter", "lastName":"Jones"}
]
```

Yuqoridagi misolda “employees” obyekti massiv hisoblanadi. U uchta obektni o'z ichiga oladi.

Har bir obyekt - shaxsning ma'lumoti (ism va familiya bilan) hisoblanadi.

### JSON matnini JavaScript obyektiga aylantirish

Veb serverdan ma'lumotlarni o'qish va ularni veb sahifada ko'rsatishda JSONdan foydalanish keng tarqalgan.

Birinchi bo'lib, JSON sintaksisini o'z ichiga olgan JavaScript stringini yarating:

```
let text = '{ "employees" : [' +
'{ "firstName":"John" , "lastName":"Doe" },' +
'{ "firstName":"Anna" , "lastName":"Smith" },' +
'{ "firstName":"Peter" , "lastName":"Jones" } ]}';
```

Keyin, stringni JavaScript obyektiga aylantirish uchun JavaScriptning maxsus `JSON.parse()` funktsiyasidan foydalaning:

```
const obj = JSON.parse(text);
```

Ana endi, sahifangizda yangi JavaScript obyektidan foydalaning:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML =
obj.employees[1].firstName + " " + obj.employees[1].lastName;
</script>
```

{% hint style="warning" %}
JSON haqida to'liq ma'lumotnomani ko'rish uchun JSON qo'llanmasi sahifamizga o'ting:
{% endhint %}
