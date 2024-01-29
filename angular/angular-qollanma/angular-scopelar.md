# Angular Scopelar

Scope HTML (view) va JavaScript (kontroller) o'rtasidagi bog'lovchi qismdir.

Scope, mavjud xususiyatlar va metodlarga ega obyekt bo'ladi.

Scope view uchun ham, controller uchun ham mavjud.

### Scopedan qanday foydalanish kerak?

AngularJS-da kontroller yaratganingizda, `$scope` obyektini argument sifatida topshirasiz:

{% code title="Controllerda yaratilgan xususiyatlarni quyidagi ko'rinishda ko'rsatish mumkin:" %}
```
<div ng-app="myApp" ng-controller="myCtrl">

<h1>{{carname}}</h1>

</div>

<script>
var app = angular.module('myApp', []);

app.controller('myCtrl', function($scope) {
  $scope.carname = "Volvo";
});
</script>
```
{% endcode %}

Controllerdagi `$scope` obyektiga xususiyatlar qo'shganda , view (HTML) ushbu xususiyatlarga murojaat qilish huquqiga ega bo'ladi.

Viewda `$scope` prefiksidan foydalanmaysiz, shunchaki xususiyat nomiga murojaat qilasiz, masalan `{{carname}}`.

### Scopeni tushunish

Agar AngularJS ilovasini quyidagilardan iborat deb hisoblasak:

* View, ya'ni HTML.
* Model, bu joriy view uchun mavjud ma'lumotlar.
* Controller, ya'ni ma'lumotlarni yaratadigan/o'zgartiradigan/o'chiradigan/boshqaradigan JavaScript funksiyasi.

Ayrgancha scope bu model hisoblanadi.

Scope view va controller uchun mavjud bo'lgan xususiyatlar va metodlarga ega JavaScript obyektidir.

{% code title="Agar viewga o'zgartirish kiritsangiz, model va controller yangilanadi:" %}
```
<div ng-app="myApp" ng-controller="myCtrl">

<input ng-model="name">

<h1>My name is {{name}}</h1>

</div>

<script>
var app = angular.module('myApp', []);

app.controller('myCtrl', function($scope) {
  $scope.name = "John Doe";
});
</script>
```
{% endcode %}

### Scope-ingizni biling

Har doim qaysi scope-da shug'ullanayotganingizni bilish muhim.

Yuqoridagi ikki misolda faqat bitta scope bor, shuning uchun scope-ingizni bilish muammo emas, lekin kattaroq ilovalar uchun HTML DOMda faqat ma'lum scopelarga murojaat qilishi mumkin bo'lgan bo'limlar bo'lishi mumkin.

{% code title="Ng-repeat direktivasi bilan ishlashda har bir takrorlash joriy takrorlash obyektiga murojaat qilish huquqiga ega:" %}
```
<div ng-app="myApp" ng-controller="myCtrl">

<ul>
  <li ng-repeat="x in names">{{x}}</li>
</ul>

</div>

<script>
var app = angular.module('myApp', []);

app.controller('myCtrl', function($scope) {
  $scope.names = ["Emil", "Tobias", "Linus"];
});
</script>
```
{% endcode %}

Har bir `<li>` elementi joriy takrorlash obyektiga murojaat qilish huquqiga ega, hozirgi holatdagi string `x` yordamida havola qilingan.

### Root scope

Barcha ilovalarda `$rootScope` mavjud, bu `ng-app` direktivasini o'z ichiga olgan HTML elementida yaratilgan scopedir.

RootScope butun ilovada mavjud.

Agar o'zgaruvchi joriy scopeda ham, `rootScope`da ham bir xil nomga ega bo'lsa, dastur joriy doiradagidan foydalanadi.

{% code title=""Color" deb nomlangan o'zgaruvchi scope-ida ham, rootScope'da ham mavjud:" %}
```
<body ng-app="myApp">

<p>The rootScope's favorite color:</p>
<h1>{{color}}</h1>

<div ng-controller="myCtrl">
  <p>The scope of the controller's favorite color:</p>
  <h1>{{color}}</h1>
</div>

<p>The rootScope's favorite color is still:</p>
<h1>{{color}}</h1>

<script>
var app = angular.module('myApp', []);
app.run(function($rootScope) {
  $rootScope.color = 'blue';
});
app.controller('myCtrl', function($scope) {
  $scope.color = "red";
});
</script>
</body>
```
{% endcode %}
