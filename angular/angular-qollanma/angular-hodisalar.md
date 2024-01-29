# Angular Hodisalar

AngularJS o'zining HTML hodisalari direktivasiga ega.

### AngularJS Hodisalar

AngularJS hodisa tinglovchilarini HTML elementlariga bir yoki bir nechta direktivalardan foydalanib qo'shishingiz mumkin:

* `ng-blur`
* `ng-change`
* `ng-click`
* `ng-copy`
* `ng-cut`
* `ng-dblclick`
* `ng-focus`
* `ng-keydown`
* `ng-keypress`
* `ng-keyup`
* `ng-mousedown`
* `ng-mouseenter`
* `ng-mouseleave`
* `ng-mousemove`
* `ng-mouseover`
* `ng-mouseup`
* `ng-paste`

Hodisa direktivalari bizga ma'lum user hodisalarida AngularJS funksiyalarini ishga tushirishga imkon beradi.

AngularJS hodisasi HTML hodisasini qayta yozmaydi, ikkala hodisa ham bajariladi.

### Mouse hodisalari

Mouse hodisalari kursor element ustida quyidagi tartibda harakat qilganda sodir bo'ladi:

1. ng-mouseover
2. ng-mouseenter
3. ng-mousemove
4. ng-mouseleave

Yoki element ustida sichqoncha tugmasi bosilganda, quyidagi tartibda najariladi:

1. ng-mousedown
2. ng-mouseup
3. ng-click

Har qanday HTML elementiga mouse hodisalarini qo'shishingiz mumkin.

{% code title="Sichqoncha H1 elementi ustida harakat qilganda count  o'zgaruvchisining qiymatini oshiring:" %}
```
<div ng-app="myApp" ng-controller="myCtrl">

<h1 ng-mousemove="count = count + 1">Mouse over me!</h1>

<h2>{{ count }}</h2>

</div>
<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.count = 0;
});
</script>
```
{% endcode %}

### ng-click direktivasi

`ng-click` direktivasi element bosilganda bajariladigan AngularJS kodini belgilaydi.

```
<div ng-app="myApp" ng-controller="myCtrl">

<button ng-click="count = count + 1">Click me!</button>

<p>{{ count }}</p>

</div>
<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.count = 0;
});
</script>
```

Funksiyaga ham murojaat qilishingiz mumkin:

```
<div ng-app="myApp" ng-controller="myCtrl">

<button ng-click="myFunction()">Click me!</button>

<p>{{ count }}</p>

</div>
<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.count = 0;
  $scope.myFunction = function() {
    $scope.count++;
  }
});
</script>
```

### Toggle, true/false

Agar tugma bosilganda HTML kodining bo'limi ko'rsatilishni va tugma yana bosilganda dropdown menyu kabi yashirishni istasangiz, tugmani toggle tugmasi kabi qiling:

![](<../../.gitbook/assets/image (170).png>)

```
<div ng-app="myApp" ng-controller="myCtrl">

<button ng-click="myFunc()">Click Me!</button>

<div ng-show="showMe">
  <h1>Menu:</h1>
  <div>Pizza</div>
  <div>Pasta</div>
  <div>Pesce</div>
</div>

</div>
<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.showMe = false;
  $scope.myFunc = function() {
    $scope.showMe = !$scope.showMe;
  }
});
</script>
```

`showMe` o'zgaruvchisi boolean qiymat `false` sifatida boshlanadi.

`myFunc` funksiyasi `!` (not) operatoridan foydalanib, `showMe` o'zgaruvchisini o'ziga qarama-qarshi tomonga o'rnatadi.

### $event obyekti

Funksiyani chaqirishda `$event` obyektini argument sifatida berishingiz mumkin.

`$event` obyekti brauzerning hodisa obyektini o'z ichiga oladi:

```
<div ng-app="myApp" ng-controller="myCtrl">

<h1 ng-mousemove="myFunc($event)">Mouse Over Me!</h1>

<p>Coordinates: {{x + ', ' + y}}</p>

</div>
<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.myFunc = function(myE) {
    $scope.x = myE.clientX;
    $scope.y = myE.clientY;
  }
});
</script>
```
