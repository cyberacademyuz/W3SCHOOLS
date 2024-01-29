# Angular Controllerlar

AngularJS kontrollerlari AngularJS ilovalarining ma'lumotlarini boshqaradi**.**

AngularJS kontrollerlari JavaScriptning oddiy obyektlari hisoblanadi.

### AngularJS kontrollerlari

AngularJS ilovalari kontrollerlar tomonidan boshqariladi.

`ng-controller` direktivasi dastur boshqaruvchisini belgilaydi.

Controller standart obyekt konstruktori tomonidan yaratilgan JavaScript obyektidir.

{% code title="AngularJSga misolga" %}
```
<div ng-app="myApp" ng-controller="myCtrl">

First Name: <input type="text" ng-model="firstName"><br>
Last Name: <input type="text" ng-model="lastName"><br>
<br>
Full Name: {{firstName + " " + lastName}}

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.firstName = "John";
  $scope.lastName = "Doe";
});
</script>
```
{% endcode %}

Ilovani tushuntirish:

AngularJS ilovasi **ng-app="myApp"** tomonidan aniqlanadi . Ilova `<div>` ichida ishlaydi.

**Ng-controller="myCtrl"** atributi AngularJS direktivasidir. U controllerni belgilaydi.

`myCtrl` funksiyasi JavaScript funksiyasi hisoblanadi**.**

AngularJS **$scope** obyekti bilan kontrollerni chaqiradi.

AngularJS da $scope ilovaning obyekti hisoblanadi (ilova o'zgaruvchilarining va funktsiyalarining egasi).

Controller scopeda ikkita xususiyat (o'zgaruvchi) yaratadi (**firstName** va **LastName**).

**Ng-model** direktivalari input maydonlarini kontroller xususiyatlariga (firstName va lastName) bog'laydi.

### Controller metodlari

Yuqoridagi misolda ikkita xususiyatga ega kontroller obyekti ko'rsatilgan: lastName va firstName.

Controllerda metodlar (funktsiya sifatidagi o'zgaruvchilar) ham bo'lishi mumkin:

{% code title="AngularJSga misol" %}
```
<div ng-app="myApp" ng-controller="personCtrl">

First Name: <input type="text" ng-model="firstName"><br>
Last Name: <input type="text" ng-model="lastName"><br>
<br>
Full Name: {{fullName()}}

</div>

<script>
var app = angular.module('myApp', []);
app.controller('personCtrl', function($scope) {
  $scope.firstName = "John";
  $scope.lastName = "Doe";
  $scope.fullName = function() {
    return $scope.firstName + " " + $scope.lastName;
  };
});
</script>
```
{% endcode %}

### Tashqi fayllardagi kontrollerlar

Kattaroq ilovalarda kontrollerlarni tashqi fayllarda saqlash odatiy holga aylangan.

`<script>` teglari orasidagi kodni **personController.js** nomli tashqi faylga nusxalash kifoya:

{% code title="AngularJSga misol:" %}
```
<div ng-app="myApp" ng-controller="personCtrl">

First Name: <input type="text" ng-model="firstName"><br>
Last Name: <input type="text" ng-model="lastName"><br>
<br>
Full Name: {{fullName()}}

</div>

<script src="personController.js"></script>
```
{% endcode %}

### Yana bir misol

Ushbu misol uchun yangi kontroller faylini yaratamiz:

```
angular.module('myApp', []).controller('namesCtrl', function($scope) {
  $scope.names = [
    {name:'Jani',country:'Norway'},
    {name:'Hege',country:'Sweden'},
    {name:'Kai',country:'Denmark'}
  ];
});
```

Faylni <mark style="color:green;">namesController.js</mark> sifatida saqlang:

Va keyin dasturda kontroller faylidan foydalaning:

{% code title="AngularJSga misol" %}
```
<div ng-app="myApp" ng-controller="namesCtrl">

<ul>
  <li ng-repeat="x in names">
    {{ x.name + ', ' + x.country }}
  </li>
</ul>

</div>

<script src="namesController.js"></script>
```
{% endcode %}
