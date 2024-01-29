# Angular Validatsiya

AngularJS kiritilgan ma'lumotlarni tekshirishi mumkin.

### Formani tasdiqlash

AngularJS mijoz tomonidan shaklni tekshirishni taklif qiladi.

AngularJS forma va kiritish maydonlarining holatini (kirish, matn maydoni, tanlash) kuzatib boradi va foydalanuvchini joriy holat haqida xabardor qilish imkonini beradi.

AngularJS shuningdek, ularga tegilganmi yoki o'zgartirilganmi yoki yo'qmi haqida ma'lumotga ega.

Kirishni tekshirish uchun standart HTML5 atributlaridan foydalanishingiz mumkin yoki oʻzingiz tekshirish funksiyalarini yaratishingiz mumkin.

{% hint style="warning" %}
Mijoz tomonidan tekshirish faqat foydalanuvchi kiritishini ta'minlay olmaydi. Server tomonini tekshirish ham zarur.
{% endhint %}

### Majburiy

`required`Kirish maydoni to'ldirilishi kerakligini belgilash uchun HTML5 atributidan foydalaning :

{% code title="Kirish maydoni talab qilinadi:" %}
```
<form name="myForm">
  <input name="myInput" ng-model="myInput" required>
</form>

<p>The input's valid state is:</p>
<h1>{{myForm.myInput.$valid}}</h1>
```
{% endcode %}

### Elektron pochta

`email`Qiymat elektron pochta bo'lishi kerakligini belgilash uchun HTML5 turidan foydalaning :

{% code title="Kirish maydoni elektron pochta bo'lishi kerak:" %}
```
<form name="myForm">
  <input name="myInput" ng-model="myInput" type="email">
</form>

<p>The input's valid state is:</p>
<h1>{{myForm.myInput.$valid}}</h1>
```
{% endcode %}

### Shakl holati va kirish holati

AngularJS doimiy ravishda shakl va kiritish maydonlarining holatini yangilab turadi.

Kirish maydonlarida quyidagi holatlar mavjud:

* `$untouched`Maydonga hali tegilmagan
* `$touched`Maydonga tegdi
* `$pristine`Maydon hali o'zgartirilmagan
* `$dirty`Maydon o'zgartirildi
* `$invalid`Maydon mazmuni noto'g'ri
* `$valid`Maydon mazmuni haqiqiy

Ularning barchasi kirish maydonining xossalari bo'lib, yoki `true`yoki bo'ladi `false`.

Shakllar quyidagi holatlarga ega:

* `$pristine`Hech qanday maydon hali oʻzgartirilmagan
* `$dirty`Bir yoki bir nechtasi o'zgartirilgan
* `$invalid`Shakl mazmuni haqiqiy emas
* `$valid`Shakl mazmuni haqiqiydir
* `$submitted`Shakl topshiriladi

Ularning barchasi shaklning xossalari bo'lib, yoki `true`yoki `false`.

Siz ushbu holatlardan foydalanuvchiga mazmunli xabarlarni ko'rsatish uchun foydalanishingiz mumkin. Misol uchun, agar maydon kerak bo'lsa va foydalanuvchi uni bo'sh qo'ysa, foydalanuvchiga ogohlantirish kerak:

{% code title="Agar maydonga tegilgan VA bo'sh bo'lsa, xato xabarini ko'rsating:" %}
```
<input name="myName" ng-model="myName" required>
<span ng-show="myForm.myName.$touched && myForm.myName.$invalid">The name is required.</span>
```
{% endcode %}

### CSS sinflari

AngularJS shakllari va kiritish maydonlariga ularning holatiga qarab CSS sinflarini qo'shadi.

Quyidagi sinflar kirish maydonlariga qo'shiladi yoki o'chiriladi:

* `ng-untouched`Maydonga hali tegilmagan
* `ng-touched`Maydonga tegdi
* `ng-pristine`Maydon hali o'zgartirilmagan
* `ng-dirty`Maydon o'zgartirildi
* `ng-valid`Maydon mazmuni haqiqiy
* `ng-invalid`Maydon mazmuni noto'g'ri
* `ng-valid-`_`key`_Har bir tekshirish uchun bitta _kalit ._ Misol: `ng-valid-required`, tasdiqlanishi kerak bo'lgan bir nechta narsalar mavjud bo'lganda foydalidir
* `ng-invalid-`_`key`_Misol:`ng-invalid-required`

Quyidagi sinflar shakllarga qo'shiladi yoki undan olib tashlanadi:

* `ng-pristine`Hech bir maydon hali oʻzgartirilmagan
* `ng-dirty`Bir yoki bir nechta maydon o'zgartirildi
* `ng-valid`Shakl mazmuni haqiqiydir
* `ng-invalid`Shakl mazmuni haqiqiy emas
* `ng-valid-`_`key`_Har bir tekshirish uchun bitta _kalit ._ Misol: `ng-valid-required`, tasdiqlanishi kerak bo'lgan bir nechta narsalar mavjud bo'lganda foydalidir
* `ng-invalid-`_`key`_Misol:`ng-invalid-required`

Agar ular ifodalagan qiymat bo'lsa, sinflar o'chiriladi `false`.

Ilovangizga yaxshiroq va intuitiv foydalanuvchi interfeysini berish uchun ushbu sinflar uchun uslublar qo'shing.

{% code title="Standart CSS-dan foydalanib uslublarni qo'llang:" %}
```
<style>
input.ng-invalid {
  background-color: pink;
}
input.ng-valid {
  background-color: lightgreen;
}
</style>
```
{% endcode %}

Shakllar ham shunday bo'lishi mumkin:

{% code title="O'zgartirilmagan (toza) shakllar va o'zgartirilgan shakllar uchun uslublarni qo'llang:" %}
```
<style>
form.ng-pristine {
  background-color: lightblue;
}
form.ng-dirty {
  background-color: pink;
}
</style>
```
{% endcode %}

### Maxsus tekshirish

O'zingizning tasdiqlash funksiyangizni yaratish biroz qiyinroq; Ilovangizga yangi direktivani qo'shishingiz va muayyan belgilangan argumentlar bilan funktsiya ichidagi tekshirish bilan shug'ullanishingiz kerak.

Maxsus tekshirish funksiyasini o'z ichiga olgan o'z direktivangizni yarating va dan foydalanib unga murojaat qiling `my-directive`.

Agar qiymatda "e" belgisi bo'lsa, maydon haqiqiy bo'ladi:

```
<form name="myForm">
<input name="myInput" ng-model="myInput" required my-directive>
</form>

<script>
var app = angular.module('myApp', []);
app.directive('myDirective', function() {
  return {
    require: 'ngModel',
    link: function(scope, element, attr, mCtrl) {
      function myValidation(value) {
        if (value.indexOf("e") > -1) {
          mCtrl.$setValidity('charE', true);
        } else {
          mCtrl.$setValidity('charE', false);
        }
        return value;
      }
      mCtrl.$parsers.push(myValidation);
    }
  };
});
</script>
```

#### Misol tushuntirildi:

HTMLda yangi direktiva atributidan foydalangan holda havola qilinadi `my-directive`.

JavaScript-da biz nomli yangi direktivani qo'shishdan boshlaymiz `myDirective`.

Esda tutingki, direktivani nomlashda siz tuya holi nomini ishlatishingiz kerak, `myDirective`lekin uni chaqirganda, `-`ajratilgan nomdan foydalanishingiz kerak `my-directive`.

Keyin, biz talab qiladigan ob'ektni qaytaring  `ngModel`, ya'ni ngModelController.

Ba'zi argumentlarni qabul qiladigan bog'lash funktsiyasini yarating, bu erda to'rtinchi argument, `mCtrl`, `ngModelController`,

Keyin funksiyani belgilang, bu holda `myValidation`bitta argumentni oladi, bu argument kirish elementining qiymati hisoblanadi.

Qiymatda "e" harfi bor yoki yo'qligini tekshirib ko'ring va model boshqaruvchisining haqiqiyligini yoki ga `true`o'rnating `false`.

Nihoyat, funktsiyani har safar kirish qiymati o'zgarganda bajariladigan boshqa funktsiyalar qatoriga `mCtrl.$parsers.push(myValidation);`qo'shadi . `myValidation`

### Tasdiqlash misoli

```
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<h2>Validation Example</h2>

<form  ng-app="myApp"  ng-controller="validateCtrl"
name="myForm" novalidate>

<p>Username:<br>
  <input type="text" name="user" ng-model="user" required>
  <span style="color:red" ng-show="myForm.user.$dirty && myForm.user.$invalid">
  <span ng-show="myForm.user.$error.required">Username is required.</span>
  </span>
</p>

<p>Email:<br>
  <input type="email" name="email" ng-model="email" required>
  <span style="color:red" ng-show="myForm.email.$dirty && myForm.email.$invalid">
  <span ng-show="myForm.email.$error.required">Email is required.</span>
  <span ng-show="myForm.email.$error.email">Invalid email address.</span>
  </span>
</p>

<p>
  <input type="submit"
  ng-disabled="myForm.user.$dirty && myForm.user.$invalid ||
  myForm.email.$dirty && myForm.email.$invalid">
</p>

</form>

<script>
var app = angular.module('myApp', []);
app.controller('validateCtrl', function($scope) {
  $scope.user = 'John Doe';
  $scope.email = 'john.doe@gmail.com';
});
</script>

</body>
</html>
```

{% hint style="warning" %}
HTML forma atributi **novalidate** standart brauzer tekshiruvini o'chirish uchun ishlatiladi.
{% endhint %}

#### Misol tushuntirildi

AngularJS direktivasi **ng-modeli** kirish elementlarini modelga bog'laydi.

Model ob'ekti ikkita xususiyatga ega: **foydalanuvchi** va **elektron pochta** .

**Ng-show** tufayli , rang: qizil bo'lgan oraliqlar faqat foydalanuvchi yoki elektron pochta **$kirli** va **$invalid** bo'lganda ko'rsatiladi .
