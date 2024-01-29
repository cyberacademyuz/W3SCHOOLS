# Angular Model

**ng-model** direktivasi HTMLdagi boshqaruv elementlarining qiymatini (input, select, matn maydoni) dastur ma'lumotlariga bog'laydi.

### ng-model direktivasi

`ng-model` direktivasi yordamida input maydonining qiymatini AngularJS da yaratilgan o'zgaruvchiga bog'lashingiz mumkin.

```
<div ng-app="myApp" ng-controller="myCtrl">
  Name: <input ng-model="name">
</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.name = "John Doe";
});
</script>
```

### Ikki tomonlama bog'lanish

Bog'lanish ikkala tomonga ham boradi. Agar foydalanuvchi input maydonidagi qiymatni o'zgartirsa, AngularJS xususiyati ham uning qiymatini o'zgartiradi:

```
<div ng-app="myApp" ng-controller="myCtrl">
  Name: <input ng-model="name">
  <h1>You entered: {{name}}</h1>
</div>
```

### Inputni tekshirish

`ng-model` direktivasi ilova ma'lumotlarining turini tekshirishni ta'minlashi mumkin (raqam, email, required):

```
<form ng-app="" name="myForm">
  Email:
  <input type="email" name="myAddress" ng-model="text">
  <span ng-show="myForm.myAddress.$error.email">Not a valid e-mail address</span>
</form>
```

Yuqoridagi misolda `ng-show` atributidagi expression `true` bo'lsagina oraliq ko'rsatiladi.

{% hint style="warning" %}
Agar `ng-model` atributidagi xususiyat mavjud bo'lmasa, AngularJS uni siz uchun yaratadi.
{% endhint %}

### Ilova holati

`ng-model` direktivasi Ilova ma'lumotlarining statusini taqdim qiladi (invalid, dirty, touched, error).

```
<form ng-app="" name="myForm" ng-init="myText = 'post@myweb.com'">
  Email:
  <input type="email" name="myAddress" ng-model="myText" required>
  <h1>Status</h1>
  {{myForm.myAddress.$valid}}
  {{myForm.myAddress.$dirty}}
  {{myForm.myAddress.$touched}}
</form>
```

### CSS classlari

`ng-model` direktivasi HTML elementlari uchun ularning statusiga qarab CSS classlarini taqdim qiladi:

```
style>
input.ng-invalid {
  background-color: lightblue;
}
</style>
<body>

<form ng-app="" name="myForm">
  Enter your name:
  <input name="myName" ng-model="myText" required>
</form>
```

`ng-model` direktivasi forma maydonining holatiga ko'ra quyidagi classlarni qo'shadi/o'chiradi:

* ng-bo'sh
* ng-bo'sh emas
* ng-tegilgan
* ng-tegishlanmagan
* ng-yaroqli
* ng-yaroqsiz
* ng-iflos
* kutilmoqda
* ng - toza
