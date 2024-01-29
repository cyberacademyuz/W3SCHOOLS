# Angular Kirish

AngularJS bu **JavaScript freymworki** hisoblanadi. Uni HTML sahifasiga `<script>` tegi orqali qo'shish mumkin.

AngularJS HTML atributlarini **Direktivlar** bilan kengaytiradi va ma'lumotlarni **Expressionlar** orqali HTML bilan bog'laydi.

### AngularJS JavaScript Frameworki hisoblanadi

AngularJS JavaScript-da yozilgan JavaScript freymworkidir.

AngularJS JavaScript fayli sifatida tarqatiladi va veb-sahifaga `<script>` tegi bilan qo'shilishi mumkin:

```
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
```

### AngularJS HTMLni kengaytiradi

AngularJS HTMLni **ng-** direktivalari bilan kengaytiradi.

**ng-app** direktivasi AngularJS ilovasini ifodalaydi.

**ng-model** direktivasi HTMLdagi boshqaruv elementlarining qiymatini (input, select, matn maydoni) dastur ma'lumotlariga bog'laydi.

**ng-bind** direktivasi dastur ma'lumotlarini HTML ko'rinishiga bog'laydi.

{% code title="AngularJS misoli:" %}
```
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
  <p>Name: <input type="text" ng-model="name"></p>
  <p ng-bind="name"></p>
</div>

</body>
</html>
```
{% endcode %}

Misolni tushuntirish:

Veb-sahifa yuklanganda AngularJS avtomatik tarzda ishga tushadi.

**ng-app** direktivasi AngularJSga `<div>` elementi AngularJS ilovasining "**owner**"i ekanligini aytadi.

**ng-model** direktivasi input maydonining qiymatini dastur o'zgaruvchisining nomi bilan bog'laydi.

**ng-bind** direktivasi `<p>` ​​elementining tarkibimi dastur o'zgaruvchisining nomi bilan bog'laydi.

### AngularJS direktivalari

Ko'rib turganingizdek, AngularJS direktivalari **ng** prefiksi bilan yoziladigan HTMLning atributi hisoblanadi.

**ng-init** direktivasi AngularJS dasturining o'zgaruvchilarini ishga tushiradi.

{% code title="AngularJSga misol:" %}
```
<div ng-app="" ng-init="firstName='John'">

<p>The name is <span ng-bind="firstName"></span></p>

</div>
```
{% endcode %}

Shu bilan bir qatorda HTML bilan:

{% code title="AngularJS misoli" %}
```
<div data-ng-app="" data-ng-init="firstName='John'">

<p>The name is <span data-ng-bind="firstName"></span></p>

</div>
```
{% endcode %}

{% hint style="warning" %}
Agar HTML sahifangizni to'gri qilishni hohlasangiz **ng-** o'rniga **data-ng**-dan foydalanishingiz mumkin.
{% endhint %}

Ushbu qo'llanmada keyinroq direktivalar haqida batafsil bilib olasiz.

### AngularJS Expressionlar

AngularJS ifodalari ikkita jingalak qavs ichida yoziladi: **\{{expression\}}**.

AngularJS ma'lumotlarni expression yozilgan joyda "chiqaradi":

{% code title="AngularJSga misol:" %}
```
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
  <p>My first expression: {{ 5 + 5 }}</p>
</div>

</body>
</html>
```
{% endcode %}

AngularJS expressionlari AngularJS ma'lumotlarini **ng-bind** direktivasi bilan bir xil tarzda HTML bilan bog'laydi.

{% code title="AngularJSga misol:" %}
```
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
  <p>Name: <input type="text" ng-model="name"></p>
  <p>{{name}}</p>
</div>

</body>
</html>
```
{% endcode %}

Ushbu qo'llanmada keyinroq expressionlar haqida batafsil bilib olasiz.

### AngularJS ilovalari

AngularJS **modullari** AngularJS ilovalarini belgilaydi.

AngularJS **kontrollerlari** AngularJS ilovalarini boshqaradi.

**ng-app** direktivasi dasturni belgilaydi, **ng-controller** direktivasi kontrollerni belgilaydi.

{% code title="AngularJSga misol:" %}
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
  $scope.firstName= "John";
  $scope.lastName= "Doe";
});
</script>
```
{% endcode %}

AngularJS modullari ilovalarni belgilaydi:

{% code title="AngularJS moduli:" %}
```
var app = angular.module('myApp', []);
```
{% endcode %}

AngularJS kontrollerlari ilovalarni boshqaradi:

{% code title="AngularJS Controller" %}
```
app.controller('myCtrl', function($scope) {
  $scope.firstName= "John";
  $scope.lastName= "Doe";
});
```
{% endcode %}

Ushbu qo'llanmada modullar va kontrollerlar haqida keyinroq batafsil bilib olasiz.
