# Angular Directivalar

AngularJS HTMLni **Direktivalar** deyiladigan yangi atributlar bilan kengaytirish imkonini beradi.

AngularJS ilovalaringizga funksionallikni taklif qiluvchi built-in direktivalar to'plamiga ega.

Bundan tashqari AngularJS, o'z direktivalaringizni belgilash imkonini beradi.

### AngularJS Direktivalar

AngularJSda direktivalar `ng-` prefiksi bilan yoziladigan HTMLning kengaytirilgan atributlari hisoblanadi.

Direktiva AngularJS ilovasini ishga tushiradi.

`ng-app` direktivasi AngularJS ilovasini ishga tushiradi.

`ng-init` direktivasi ilova ma'lumotlarini ishga tushiradi.

**ng-model** direktivasi HTMLdagi boshqaruv elementlarining qiymatini (input, select, matn maydoni) dastur ma'lumotlariga bog'laydi.

Barcha AngularJS direktivalari haqida bizning <mark style="color:green;">AngularJS direktivasi</mark> nomli qo'llanmamizda o'qing.

```
<div ng-app="" ng-init="firstName='John'">

<p>Name: <input type="text" ng-model="firstName"></p>
<p>You wrote: {{ firstName }}</p>

</div>
```

`ng-app` direktivasi AngularJSga `<div>` elementi AngularJS ilovasining "**owner**"i ekanligini aytadi.

### Ma'lumotlarni bog'lash

Yuqoridagi misoldagi `{{ firstName }}` expressioni AngularJSning ma'lumotlarni bog'lovchi expressioni hisoblanadi.

AngularJS-da ma'lumotlarni bog'lash AngularJS expressionlarini AngularJS ma'lumotlari bilan bog'laydi.

`{{ firstName }}` `ng-model="firstName"` bilan bog'langan.

Keyingi misoldagi ikkita matn maydoni ikkita `ng-model` direktivasi bilan bog'langan:

```
<div ng-app="" ng-init="quantity=1;price=5">

Quantity: <input type="number" ng-model="quantity">
Costs:    <input type="number" ng-model="price">

Total in dollar: {{ quantity * price }}

</div>
```

{% hint style="warning" %}
`ng-init`dan foydalanish keng tarqalmagan. Ma'lumotlarni qanday ishga tushirishni  kontrollerlar haqidagi bo'limda bilib olasiz.
{% endhint %}

### HTML elementlarida tskil

`ng-repeat` direktivasi HTML elementida tskil qiladi:

```
<div ng-app="" ng-init="names=['Jani','Hege','Kai']">
  <ul>
    <li ng-repeat="x in names">
      {{ x }}
    </li>
  </ul>
</div>
```

`ng-repeat` direktiva aslida to'plamdagi har bir element uchun HTML elementlarini bir marta klonlaydi**.**

`ng-repeat` direktivasi obyektlar massivida ishlatiladi:

```
<div ng-app="" ng-init="names=[
{name:'Jani',country:'Norway'},
{name:'Hege',country:'Sweden'},
{name:'Kai',country:'Denmark'}]">

<ul>
  <li ng-repeat="x in names">
    {{ x.name + ', ' + x.country }}
  </li>
</ul>

</div>
```

{% hint style="warning" %}
AngularJS ma'lumotlar bazasi CRUD (Create Read Update Delete) ilovalari uchun juda mos keladi.\
Tasavvur qiling, agar bu obyektlar ma'lumotlar bazasidan olingan ma'lumotlar bo'lsa.
{% endhint %}

### Ng-app direktivasi

`ng-app` direktivasi AngularJS ilovasining root elementini belgilaydi.

`ng-app` direktivasi veb-sahifa yuklanganda dasturni **avtomatik yuklaydi** ( avtomatik ravishda ishga tushiradi).

### ng-init direktivasi

`ng-init` direktivasi AngularJS ilovasi uchun **dastlabki qiymatlarni** belgilaydi.

Odatda, `ng-init`dan foydalanmaysiz. Uning o'rniga kotroller yoki moduldan foydalanasiz.

Kontrollerlar va modullar haqida keyinroq bilib olasiz.

### ng-model direktivasi

`ng-model` direktivasi HTMLdagi boshqaruv elementlarining qiymatini (input, select, matn maydoni) dastur ma'lumotlariga bog'laydi.

`ng-model` direktivasi shuningdek:

* Ilova ma'lumotlarining turini tekshirishni taqdim qiladi (raqam, mail, required).
* Ilova ma'lumotlarining statusini taqdim qiladi (invalid, dirty, touched, error).
* HTML elementlari uchun CSS classlarini taqdim qiladi.
* HTML elementlarini HTML formalariga ulaydi.

`ng-model` direktivasi haqida keyingi bo'limda batasil o'rganasiz.

### Yangi Direktivalar yaratish

AngularJSning barcha built-in direktivalariga qo'shimcha ravishda o'zingizning direktivalaringizni yaratishingiz mumkin.

Yangi direktiva `.directive` funksiyasi yordamida yaratiladi.

Yangi direktivani chaqirish uchun yangi direktiva nomi bilan bir xil nomdagi HTML elementini yarating.

Direktivaga nom berishda  `w3TestDirective` camel case-idan foydalanishingiz kerak, lekin uni chaqirganda, ajratilgan nom  `w3-test-directive` dan foydalaning:

```
<body ng-app="myApp">

<w3-test-directive></w3-test-directive>

<script>
var app = angular.module("myApp", []);
app.directive("w3TestDirective", function() {
  return {
    template : "<h1>Made by a directive!</h1>"
  };
});
</script>

</body>
```

Direktivani quyidagilar yordamida chaqirishingiz mumkin:

* Element nomi
* Atribut
* Class
* Izoh

Quyidagi misollarning barchasi bir xil natija beradi:

{% code title="Element nomi" %}
```
<w3-test-directive></w3-test-directive>
```
{% endcode %}

{% code title="Atribut" %}
```
<div w3-test-directive></div>
```
{% endcode %}

{% code title="Class" %}
```
<div class="w3-test-directive"></div>
```
{% endcode %}

{% code title="Izoh" %}
```
<!-- directive: w3-test-directive -->
```
{% endcode %}

### Cheklovlar

Direktivalaringizni faqat ba'zi usullar bilan chaqirilishini cheklashingiz mumkin.

{% code title=""A" qiymati bilan restrict xususiyatini qo'shish orqali direktivani faqat atributlar orqali chaqirish mumkin:" %}
```
var app = angular.module("myApp", []);
app.directive("w3TestDirective", function() {
  return {
    restrict : "A",
    template : "<h1>Made by a directive!</h1>"
  };
});
```
{% endcode %}

To'g'ri restrict qiymatlari quyidagilardir:

* `E` - Eement nomi uchun
* `A` - Atribut uchun
* `C` - Class uchun
* `M` - Izoh uchun

Default qiymat `EA` hisoblanadi, ya'ni element nomlari ham, atribut nomlari ham direktivani chaqirishi mumkin.
