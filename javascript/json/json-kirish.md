# JSON Kirish

|                                                                                        | JSON Java Script Object Notation degan ma'noni anglatadi             |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| <img src="https://www.w3schools.com/js/img_json.jpg" alt="HTML" data-size="original">  | JSON - bu ma'lumotlarni saqlash va uzatish uchun maxsus matn formati |
|                                                                                        | ‌JSON "o'zini tavsiflovchi" va uni tushunish oson                    |

### JSONga misol

Bu misol JSON stringni:

```
'{"name":"John", "age":30, "car":null}'
```

U 3 xususiyatga ega obyekt tuadi:

* name
* age
* car

Har bir xususiyatning qiymati bor.

Agar JSON stringini JavaScript dasturi bilan parse qilsangiz, ma'lumotlarga obyekt sifatida murojaat qilishingiz mumkin:

```
let personName = obj.name;
let personAge = obj.age;
```

### JSON nima ?

* JSON **J**ava **S**cript **O**bject **N**otation degan ma'noni anglatadi
* ‌JSON ma'lumotlar almashishning yengil formatidir
* JSON - bu JavaScript obyekti ko'rinishi yozilgan oddiy matn
* JSON kompyuterlar o'rtasida ma'lumotlar yuborish uchun ishlatiladi
* JSON tildan mustaqil \*

{% hint style="warning" %}
\*\
JSON sintaksisi JavaScript obyektining ko'rinishida tuzilgan, ammo JSON formati faqatgina matn hisoblanadi.

JSON ni o'qish va yaratish uchun kod ko'plab dasturlash tillarida mavjud.
{% endhint %}

JSON formati dastlab[ Duglas Krokford](http://www.crockford.com/) tomonidan iishlab chiqilgan.

### Nega JSON dan foydalanish kerak ?

JSON formati sintaktik jihatdan JavaScript obyektlarini yaratish kodiga oʻxshaydi. Shu sababli, JavaScript dasturi JSON ma'lumotlarini osongina JavaScript obyektlariga aylantira oladi.

Format faqat matn bo'lganligi sababli, JSON ma'lumotlari kompyuterlar o'rtasida osongina yuborilishi va istalgan dasturlash tili tomonidan ishlatilishi mumkin.

JavaScript-da JSON stringlarini JavaScript obyektlariga aylantirish uchun built-in funksiya mavjud:

`JSON.parse()`

Bundan tashqari JavaScript-da, obyektni JSON stringgiga aylantiruvchi built-in funksiyaga ham bor:

`JSON.stringify()`

{% hint style="warning" %}
Siz serverdan haqiqiy string qabul qilishingiz va uni obyekt sifatida ishlatishingiz mumkin.

JavaScript obyektini esa serverga string formatida yuborishingiz ham mumkin.

Ma'lumotlar bilan hech qanday murakkab parsing va konvertatsiyalarsiz obyekt sifatida ishlashingiz mumkin.
{% endhint %}

### Ma'lumotlarni saqlash

Ma'lumotlarni saqlashda ma'lumotlar ma'lum bir formatda bo'lishi kerak va uni qayerga saqlashni tanlashingizdan qat'iy nazar, _matn_ har doim to'g'ri formatlardan biri bo'ladi.

JSON JavaScript obyektlarini matn sifatida saqlash imkonini beradi.
