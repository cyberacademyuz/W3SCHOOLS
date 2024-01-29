# Angular API

**API qisqartmasi A** ilova **P** dasturlash **I** nterfeysini anglatadi .

### AngularJS Global API

AngularJS Global API umumiy vazifalarni bajarish uchun global JavaScript funktsiyalari to'plamidir:

* Ob'ektlarni taqqoslash
* Ob'ektlarni takrorlash
* Ma'lumotlarni konvertatsiya qilish

Global API funktsiyalariga burchakli ob'ekt yordamida kirish mumkin.

Quyida ba'zi umumiy API funktsiyalari ro'yxati keltirilgan:

| API                 | Tavsif                                             |
| ------------------- | -------------------------------------------------- |
| angular.lowercase() | Satrni kichik harfga aylantiradi                   |
| angular.uppercase() | Satrni bosh harfga aylantiradi                     |
| angular.isString()  | Malumot satr bo'lsa, true qiymatini qaytaradi      |
| angular.isNumber()  | Agar havola raqam bo'lsa, true qiymatini qaytaradi |

#### angular.lowercase()

```
<div ng-app="myApp" ng-controller="myCtrl">
  <p>{{ x1 }}</p>
  <p>{{ x2 }}</p>
</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.x1 = "JOHN";
  $scope.x2 = angular.lowercase($scope.x1);
});
</script>
```

#### angular.uppercase()

```
<div ng-app="myApp" ng-controller="myCtrl">
  <p>{{ x1 }}</p>
  <p>{{ x2 }}</p>
</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.x1 = "John";
  $scope.x2 = angular.uppercase($scope.x1);
});
</script>
```

#### angular.isString()

```
<div ng-app="myApp" ng-controller="myCtrl">
  <p>{{ x1 }}</p>
  <p>{{ x2 }}</p>
</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.x1 = "JOHN";
  $scope.x2 = angular.isString($scope.x1);
});
</script>
```

#### angular.isNumber()

```
<div ng-app="myApp" ng-controller="myCtrl">
  <p>{{ x1 }}</p>
  <p>{{ x2 }}</p>
</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.x1 = "JOHN";
  $scope.x2 = angular.isNumber($scope.x1);
});
</script>
```
