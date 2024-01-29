# Angular Modullar

AngularJS moduli ilovani belgilaydi.

Modul, dasturning turli qismlari uchun konteyner hisoblanadi.

Modul, ilova kontrollerlari uchun konteyner hisoblanadi.

Kontrollerlar har doim modulga tegishli bo'ladi.

### Modul yaratish

AngularJSda `angular.module` funksiyasi orqali modul yaratiladi.

```
<div ng-app="myApp">...</div>

<script>

var app = angular.module("myApp", []);

</script>
```

"myApp" parametri ilova ishga tushadigan HTML elementiga havola bo'ladi.

Endi AngularJS ilovangizga kontrollerlar, direktivlar, filtrlar va boshqa narsalar ham qo'shishingiz mumkin.

### Kontroller qo'shish

Ilovangizga kontroller qo'shing va `ng-controller` direktivasi orqali kontrollerga murojaat qiling:

```
<div ng-app="myApp" ng-controller="myCtrl">
{{ firstName + " " + lastName }}
</div>

<script>

var app = angular.module("myApp", []);

app.controller("myCtrl", function($scope) {
  $scope.firstName = "John";
  $scope.lastName = "Doe";
});

</script>
```

Ushbu qo'llanmada controllerlar haqida keyinroq batafsil bilib olasiz.

### Direktiva qo'shish

AngularJS ilovangizga funksionallikni qo'shish uchun foydalanishingiz mumkin bo'lgan built-in direktivalar to'plamiga ega.

Bu haqida batafsil ma'lumot uchun <mark style="color:green;">AngularJS direktivalari</mark> sahifasiga o'ting.

Bundan tashqari, moduldan ilovalaringizga o'z direktivalaringizni qo'shish uchun foydalanishingiz mumkin:

```
<div ng-app="myApp" w3-test-directive></div>

<script>
var app = angular.module("myApp", []);

app.directive("w3TestDirective", function() {
  return {
    template : "I was made in a directive constructor!"
  };
});
</script>
```

Ushbu qo'llanmada direktivalar haqida keyinroq batafsil bilib olasiz.

### Fayllardagi modullar va kontrollerlar

AngularJS ilovalarida modul va kontrollerlarni JavaScript fayllariga joylashtirish odatiy holga aylangan.

Ushbu misolda "myApp.js" ilova moduli ta'rifini o'z ichiga oladi, "myCtrl.js" esa kontrollerni o'z ichiga oladi:

```
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="myApp" ng-controller="myCtrl">
{{ firstName + " " + lastName }}
</div>

<script src="myApp.js"></script>
<script src="myCtrl.js"></script>

</body>
</html>
```

{% code title="myApp.js" %}
```
var app = angular.module("myApp", []);
```
{% endcode %}

{% hint style="warning" %}
Modul taʼrifidagi `[]` parametri tobe modullarni ifodalash uchun ishlatilishi mumkin.

`[]` parametrisiz yangi modul _yaratmaysiz_, balki mavjud modulni _qayta tiklaysiz ._
{% endhint %}

{% code title="myCtrl.js" %}
```
app.controller("myCtrl", function($scope) {
  $scope.firstName = "John";
  $scope.lastName= "Doe";
});
```
{% endcode %}

### Funksiyalar global namespacelarni buzishi mumkin

JavaScript-da global funksiyalardan saqlanish kerak. Ular boshqa skriptlar tomonidan osongina qayta yozilishi yoki yo'q qilinishi mumkin.

AngularJS modullari modulning barcha funktsiyalarini lokal saqlash orqali bu muammoni kamaytiradi.

### Kutubxonani qachon yuklash kerak

HTML ilovalarida skriptlarni `<body>` elementining oxiriga joylashtirish odatiy holga aylangan bo'lsa-da, AngularJS kutubxonasini `<head>` yoki `<body>` elementining boshida yuklash tavsiya qilinadi.

Buning sababi, `angular.module`ni chaqirishni faqat kutubxona yuklangandan keyin kompilyatsiya qilish mumkin.

```
<!DOCTYPE html>
<html>
<body>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>

<div ng-app="myApp" ng-controller="myCtrl">
{{ firstName + " " + lastName }}
</div>

<script>
var app = angular.module("myApp", []);
app.controller("myCtrl", function($scope) {
  $scope.firstName = "John";
  $scope.lastName = "Doe";
});
</script>

</body>
</html>
```
