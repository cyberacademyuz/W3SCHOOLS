# Angular Filterlar

AngularJS-da ma'lumotlarni formatlash uchun filtrlar qo'shilishi mumkin.

### AngularJS filtrlari

AngularJS ma'lumotlarni o'zgartirish uchun filtrlar taqdim qiladi:

* `currency` Raqamni valyuta formatiga o'tkazadi
* `date` Sanani belgilangan formatga o'tkazadi
* `filter` Massivdan elementlarning subsetini tanlaydi
* `json` Obyektni JSON stringiga o'tkazadi
* `limitTo` Massiv/stringni belgilangan miqdordagi elementlar/belgilar bilan cheklaydi
* `lowercase` Stringni kichik harflarga o'tkazadi&#x20;
* `number` Raqamni stringga o'tkazadi.
* `orderBy` Massivni expression orqali tartiblaydi.
* `uppercase` Stringni katta harfga o'tkazadi.

### Expressionlarga filtr qo'shish

Filtrlarni iboralarga `|` belgisi va undan keyin filtrdan foydalanib qoʻshish mumkin.

`uppercase` filtri stringlarni katta harfga o'tkazadi:

```
<div ng-app="myApp" ng-controller="personCtrl">

<p>The name is {{ lastName | uppercase }}</p>

</div>
```

`lowercase` filtri formati stringlarni kichik harflarga o'tkazadi:

```
<div ng-app="myApp" ng-controller="personCtrl">

<p>The name is {{ lastName | lowercase }}</p>

</div>
```

### Direktivlarga filtrlar qo'shish

Filtrlar `ng-repeat` kabi direktivalarga | belgisidan keyin filtrdan foydalanib qo'shiladi:

{% code title="Filtr orderBymassivni saralaydi:" %}
```
<div ng-app="myApp" ng-controller="namesCtrl">

<ul>
  <li ng-repeat="x in names | orderBy:'country'">
    {{ x.name + ', ' + x.country }}
  </li>
</ul>

</div>
```
{% endcode %}

### currency filtri

`currency` filtri raqamni valyuta sifatida formatlaydi:

```
<div ng-app="myApp" ng-controller="costCtrl">

<h1>Price: {{ price | currency }}</h1>

</div>
```

AngularJS `currency` filtri ma'lumotnomasida `currency` filtri haqida ko'proq o'qing

### filter filteri

`filter` filtri massivning subsetini tanlaydi.

`filter` filtri faqat massivlarda ishlatilishi mumkin va u faqat mos keladigan elementlarni o'z ichiga olgan massivni qaytaradi.

{% code title=""i" harfi bo'lgan nomlarni qaytarish:" %}
```
<div ng-app="myApp" ng-controller="namesCtrl">

<ul>
  <li ng-repeat="x in names | filter : 'i'">
    {{ x }}
  </li>
</ul>

</div>"i" harfi bo'lgan nomlarni qaytaring:
```
{% endcode %}

Filter filtri haqida AngularJS filter filtri ma'lumotnomasida ko'proq o'qing

### User input asosida massivni filtrlash

Input maydoniga `ng-model` direktivasini o'rnatish orqali input maydonining qiymatini filtrda expression sifatida ishlatishimiz mumkin.

Input maydoniga harf kiriting va ro'yxat mos kelishiga qarab qisqaradi/ko'payadi:

* Jani
* Karl
* Margaret
* Xege
* Jo
* Gustav
* Birgit
* Meri
* Kay

```
<div ng-app="myApp" ng-controller="namesCtrl">

<p><input type="text" ng-model="test"></p>

<ul>
  <li ng-repeat="x in names | filter : test">
    {{ x }}
  </li>
</ul>

</div>
```

### User inputga qarab massivni tartiblang

Saralash tartibini o'zgartirish uchun jadvalning sarlavhalarini bosing:

| Ism      | Mamlakat  |
| -------- | --------- |
| Jani     | Norvegiya |
| Karl     | Shvetsiya |
| Margaret | Angliya   |
| Xege     | Norvegiya |
| Jo       | Daniya    |
| Gustav   | Shvetsiya |
| Birgit   | Daniya    |
| Meri     | Angliya   |
| Kay      | Norvegiya |

Jadval sarlavhalariga `ng-click` direktivasini qo'shish orqali massivning saralash tartibini o'zgartiradigan funksiyani ishga tushirishimiz mumkin:

```
<div ng-app="myApp" ng-controller="namesCtrl">

<table border="1" width="100%">
  <tr>
    <th ng-click="orderByMe('name')">Name</th>
    <th ng-click="orderByMe('country')">Country</th>
  </tr>
  <tr ng-repeat="x in names | orderBy:myOrderBy">
    <td>{{x.name}}</td>
    <td>{{x.country}}</td>
  </tr>
</table>

</div>

<script>
angular.module('myApp', []).controller('namesCtrl', function($scope) {
  $scope.names = [
    {name:'Jani',country:'Norway'},
    {name:'Carl',country:'Sweden'},
    {name:'Margareth',country:'England'},
    {name:'Hege',country:'Norway'},
    {name:'Joe',country:'Denmark'},
    {name:'Gustav',country:'Sweden'},
    {name:'Birgit',country:'Denmark'},
    {name:'Mary',country:'England'},
    {name:'Kai',country:'Norway'}
  ];
  $scope.orderByMe = function(x) {
    $scope.myOrderBy = x;
  }
});
</script>
```

### Maxsus filtrlar

Modulingiz bilan yangi filtr zavod funksiyasini roʻyxatdan oʻtkazish orqali oʻz filtrlaringizni yaratishingiz mumkin:

{% code title=""myFormat" deb nomlangan maxsus filtr yarating:" %}
```
<ul ng-app="myApp" ng-controller="namesCtrl">
  <li ng-repeat="x in names">
    {{x | myFormat}}
  </li>
</ul>

<script>
var app = angular.module('myApp', []);
app.filter('myFormat', function() {
  return function(x) {
    var i, c, txt = "";
    for (i = 0; i < x.length; i++) {
      c = x[i];
      if (i % 2 == 0) {
        c = c.toUpperCase();
      }
      txt += c;
    }
    return txt;
  };
});
app.controller('namesCtrl', function($scope) {
  $scope.names = ['Jani', 'Carl', 'Margareth', 'Hege', 'Joe', 'Gustav', 'Birgit', 'Mary', 'Kai'];
});</script>
```
{% endcode %}

`myFormat` filtri boshqa har bir belgini katta harfga formatlaydi.
