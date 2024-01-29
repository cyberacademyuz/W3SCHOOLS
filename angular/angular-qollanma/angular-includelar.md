# Angular Includelar

AngularJS yordamida siz tashqi fayldan HTMLni kiritishingiz mumkin.

### AngularJS o'z ichiga oladi

**AngularJS bilan ng-include** direktivasi yordamida HTML tarkibini kiritishingiz mumkin :

```
<body ng-app="">

<div ng-include="'myFile.htm'"></div>

</body>
```

### AngularJS kodini qo'shing

Siz ng-include direktivasiga qo'shgan HTML fayllari AngularJS kodini ham o'z ichiga olishi mumkin:

{% code title="myTable.htm:" %}
```
<table>
  <tr ng-repeat="x in names">
    <td>{{ x.Name }}</td>
    <td>{{ x.Country }}</td>
  </tr>
</table>
```
{% endcode %}

Veb-sahifangizga "myTable.htm" faylini qo'shing va barcha AngularJS kodi, hatto kiritilgan fayl ichidagi kod ham bajariladi:

```
<body>

<div ng-app="myApp" ng-controller="customersCtrl">
  <div ng-include="'myTable.htm'"></div>
</div>

<script>var app = angular.module('myApp', []);
app.controller('customersCtrl', function($scope, $http) {
  $http.get("customers.php").then(function (response) {
    $scope.names = response.data.records;
  });
});
</script>
```

### Oʻzaro domenlarni qoʻshing

Odatiy bo'lib, ng-include direktivasi boshqa domenlardagi fayllarni qo'shishga ruxsat bermaydi.

Boshqa domendagi fayllarni kiritish uchun siz ilovangizning konfiguratsiya funksiyasiga qonuniy fayllar va/yoki domenlarning oq roʻyxatini qoʻshishingiz mumkin:

```
<body ng-app="myApp">

<div ng-include="'https://tryit.w3schools.com/angular_include.php'"></div>

<script>var app = angular.module('myApp', [])
app.config(function($sceDelegateProvider) {
  $sceDelegateProvider.resourceUrlWhitelist([
    'https://tryit.w3schools.com/**'
  ]);
});
</script>

</body>
```

{% hint style="warning" %}
Belgilangan manzildagi server o'zaro domen fayllariga kirishga ruxsat berishiga ishonch hosil qiling.
{% endhint %}
