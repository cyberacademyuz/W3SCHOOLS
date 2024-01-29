# Angular Jadvallar

`ng-repeat` direktivasi jadvallarni ko'rsatish uchun juda mos keladi.

### Ma'lumotlarni jadvalda ko'rsatish

Jadvallarni angular bilan ko'rsatish juda oddiy:

{% code title="AngularJSga misol:" %}
```
<div ng-app="myApp" ng-controller="customersCtrl">

<table>
  <tr ng-repeat="x in names">
    <td>{{ x.Name }}</td>
    <td>{{ x.Country }}</td>
  </tr>
</table>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('customersCtrl', function($scope, $http) {
  $http.get("customers.php")
  .then(function (response) {$scope.names = response.data.records;});
});
</script>
```
{% endcode %}

### CSS stili bilan ko'rsatish

Endi uni chiroyliroq qilish uchun sahifaga bir nechta CSS qo'shing:

{% code title="CSS stili" %}
```
<style>
table, th , td {
  border: 1px solid grey;
  border-collapse: collapse;
  padding: 5px;
}

table tr:nth-child(odd) {
  background-color: #f1f1f1;
}

table tr:nth-child(even) {
  background-color: #ffffff;
}
</style>
```
{% endcode %}

### orderBy filtri bilan ko'rsatish

Jadvalni saralash uchun **orderBy** filtrini qo'shing:&#x20;

{% code title="AngularJSga misol:" %}
```
<table>
  <tr ng-repeat="x in names | orderBy : 'Country'">
    <td>{{ x.Name }}</td>
    <td>{{ x.Country }}</td>
  </tr>
</table>
```
{% endcode %}

### uppercase filtri bilan ko'rsatish

Katta harflarda ko'rsatish uchun `uppercase` filtrini qo'shing:&#x20;

{% code title="AngularJSga misol:" %}
```
<table>
  <tr ng-repeat="x in names">
    <td>{{ x.Name }}</td>
    <td>{{ x.Country | uppercase }}</td>
  </tr>
</table>
```
{% endcode %}

### Jadval indeksini ko'rsatish ($index)

Jadval indeksini ko'rsatish uchun **$index** bilan `<td>` qo'shing :&#x20;

{% code title="AngularJSga misol:" %}
```
<table>
  <tr ng-repeat="x in names">
    <td>{{ $index + 1 }}</td>
    <td>{{ x.Name }}</td>
    <td>{{ x.Country }}</td>
  </tr>
</table>
```
{% endcode %}

### $even va $odd dan foydalanish

{% code title="AngularJSga misol:" %}
```
<table>
  <tr ng-repeat="x in names">
    <td ng-if="$odd" style="background-color:#f1f1f1">{{ x.Name }}</td>
    <td ng-if="$even">{{ x.Name }}</td>
    <td ng-if="$odd" style="background-color:#f1f1f1">{{ x.Country }}</td>
    <td ng-if="$even">{{ x.Country }}</td>
  </tr>
</table>
```
{% endcode %}
