# Angular Ma'lumotlarni bog'lash

AngularJS-da ma'lumotlarni bog'lash - bu model va ko'rsatish o'rtasidagi sinxronizatsiya.

### Ma'lumotlar modeli

AngularJS ilovalari odatda ma'lumotlar modeliga ega. Ma'lumotlar modeli - bu dastur uchun mavjud bo'lgan ma'lumotlar to'plami hisoblanadi.

```
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.firstname = "John";
  $scope.lastname = "Doe";
});
```

### HTML view

AngularJS ilovasida ko'rsatiladigan HTML konteyneri view deb ataladi.

View modelga murojaat qilish huquqiga ega va viewda model ma'lumotlarini ko'rsatishning bir necha usullari mavjud.

Elementning innerHTMLini, belgilangan model xususiyatiga bog'laydigan `ng-bind` direktivasidan foydalanishingiz mumkin:

```
<p ng-bind="firstname"></p>
```

Modeldagi kontentni ko'rsatish uchun ikkita jingalak qavs `{{}}` dan ham foydalanishingiz mumkin:

```
<p>First name: {{firstname}}</p>
```

Yoki modelni ko'rinishga bog'lash uchun HTML boshqaruvlarida `ng-model` direktivasidan foydalanishingiz mumkin.

### `ng-model` Direktivasi

Modeldan ma'lumotlarni HTML boshqaruvidagi viewga ulash uchun `ng-model` direktivasidan foydalaning (input, select, matn maydoni)

```
<input ng-model="firstname">
```

`ng-model` direktivasi model va view o'rtasida ikki tomonlama bog'lanishni ta'minlaydi.

### Ikki tomonlama bog'lanish

AngularJS-da ma'lumotlarni bog'lash - bu model va view o'rtasidagi sinxronizatsiya.

Modeldagi ma'lumotlar o'zgarganda, _view_ o'zgarishlarni ko'rsatadi va viewdagi ma'lumotlar o'zgarganda_, model_ ham _yangilanadi_. Bu darhol va avtomatik tarzda sodir bo'ladi, bu esa model va viewning har doim yangilanishiga ishonch hosil qiladi.

```
<div ng-app="myApp" ng-controller="myCtrl">
  Name: <input ng-model="firstname">
  <h1>{{firstname}}</h1>
</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.firstname = "John";
  $scope.lastname = "Doe";
});</script>
```

### AngularJS Controller

AngularJS-dagi ilovalar kontrollerlar tomonidan boshqariladi. <mark style="color:green;">AngularJS Controllerlari</mark> bo'limida kontrollerlar haqida o'qing.

Model va viewning tezda sinxronizatsiya bo'lishi tufayli kontroller viewdan butunlay ajratilishi mumkin va shunchaki model ma'lumotlariga e'tibor qaratish mumkin. AngularJS-da ma'lumotlarni bog'lash tufayli, view kontrollerda kiritilgan har qanday o'zgarishlarni aks ettiradi.

```
<div ng-app="myApp" ng-controller="myCtrl">
  <h1 ng-click="changeName()">{{firstname}}</h1>
</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.firstname = "John";
  $scope.changeName = function() {
    $scope.firstname = "Nelly";
  }
});
</script>
```
