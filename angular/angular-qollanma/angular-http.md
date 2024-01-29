# Angular HTTP

**$http** masofaviy serverlardan ma'lumotlarni o'qish uchun AngularJS servisi hisoblanadi.

### AngularJS $http

AngularJSning `$http` servisi serverga so'rov yuboradi va javob qaytaradi.

{% code title="Serverga oddiy so'rov yuboring va natijani sarlavhada ko'rsating:" %}
```
<div ng-app="myApp" ng-controller="myCtrl">

<p>Today's welcome message is:</p>
<h1>{{myWelcome}}</h1>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope, $http) {
  $http.get("welcome.htm")
  .then(function(response) {
    $scope.myWelcome = response.data;
  });
});
</script>
```
{% endcode %}

### Metodlari

Yuqoridagi misol `$http` servisining `.get` metodidan foydalanadi.

`.get` metodi `$http` servisining shortcut metodidir. Bir nechta shortcut metodlar mavjud:

* `.delete()`
* `.get()`
* `.head()`
* `.jsonp()`
* `.patch()`
* `.post()`
* `.put()`

Yuqoridagi metodlar `$http` servisini chaqirishning barcha shortcutlari hisoblanadi:

```
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope, $http) {
  $http({
    method : "GET",
      url : "welcome.htm"
  }).then(function mySuccess(response) {
    $scope.myWelcome = response.data;
  }, function myError(response) {
    $scope.myWelcome = response.statusText;
  });
});
```

Yuqoridagi misol $http xizmatini argument sifatida ob'ekt bilan bajaradi. Ob'ekt HTTP usulini, url manzilini, muvaffaqiyatga erishganda nima qilish kerakligini va muvaffaqiyatsizlikka uchraganda nima qilish kerakligini ko'rsatmoqda.

### Xususiyatlari

Serverdan javob quyidagi xususiyatlarga ega obyektdir:

* `.config` request yaratish uchun ishlatiladigan obyekt.
* `.data` serverdan responseni tashuvchi string yoki obyekt.
* `.headers` header ma'lumotlarini olish uchun foydalaniladigan funksiya.
* `.status` HTTP statusini belgilaydigan raqam.
* `.statusText` HTTP statusini belgilovchi string.

```
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope, $http) {
  $http.get("welcome.htm")
  .then(function(response) {
    $scope.content = response.data;
    $scope.statuscode = response.status;
    $scope.statustext = response.statusText;
  });
});
```

Xatolarni ushlash uchun `.then` metodiga yana bitta funksiya qo'shing:

```
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope, $http) {
  $http.get("wrongfilename.htm")
  .then(function(response) {
    // First function handles success
    $scope.content = response.data;
  }, function(response) {
    // Second function handles error
    $scope.content = "Something went wrong";
  });
});
```

### JSON

Responsedan olingan maʼlumotlar JSON formatida boʻlishi kutilmoqda.

JSON ma'lumotlarni tashishning ajoyib usuli bo'lib, uni AngularJS yoki boshqa JavaScript-da ishlatish oson.

Misol: Serverda bizda 15 ta mijozdan iborat JSON obyektini qaytaruvchi fayl bor, ularning barchasi `records` nomli massivga o'ralgan.

JSON obyektini ko'rish uchun shu yerni bosing.

{% code title="ng-repeat direktivasi massivda harakatlanish uchun juda mos keladi:" %}
```
<div ng-app="myApp" ng-controller="customersCtrl">

<ul>
  <li ng-repeat="x in myData">
    {{ x.Name + ', ' + x.Country }}
  </li>
</ul>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('customersCtrl', function($scope, $http) {
  $http.get("customers.php").then(function(response) {
    $scope.myData = response.data.records;
  });
});
</script>
```
{% endcode %}

Ilovani tushuntirish:

Ilova `$scope` va `$http` obyekti bilan `customerCtrl` kontrollerini belgilaydi.

`$http` tashqi ma'lumotlarni so'rash uchun **XMLHttpRequest** obyektidir.

`$http.get()` [https://www.w3schools.com/angular/customers.php](https://www-w3schools-com.translate.goog/angular/customers.php?\_x\_tr\_sl=en&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) dan **JSON** ma'lumotlarini o'qiydi .

Muvaffaqiyatli amalga oshganidan so'ng, kontroller serverdan JSON ma'lumotlari bilan `myData` xususiyatini yaratadi.
