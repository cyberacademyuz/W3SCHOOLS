# Angular Select

AngularJS massiv yoki obyektdagi elementlar asosida dropdown yaratish imkonini beradi.

### ng-options yordamida tanlash qutisini yaratish

Agar AngularJS-dagi obyekt yoki massiv asosida dropdown ro'yxat yaratmoqchi bo'lsangiz `ng-options` direktivasini ishlatishingiz kerak:

```
<div ng-app="myApp" ng-controller="myCtrl">

<select ng-model="selectedName" ng-options="x for x in names">
</select>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
  $scope.names = ["Emil", "Tobias", "Linus"];
});
</script>
```

### ng-options va ng-repeat

Xuddi shunday dropdown ro'yxat yaratish uchun `ng-repeat` direktivasidan ham foydalanishingiz mumkin:

```
<select>
  <option ng-repeat="x in names">{{x}}</option>
</select>
```

`ng-repeat` direktivasi massivdagi har bir element uchun HTML kod blokini takrorlaganligi sababli, undan dropdown ro'yxatdagi variantlarni yaratish uchun foydalanish mumkin, ammo `ng-options` direktivasi dropdown ro'yxatini variantlar bilan to'ldirish uchun yaratilgan.

### Nimadan foydalanaman ?

Siz `ng-repeat` direktivasidan ham, `ng-options` direktivasidan ham foydalanishingiz mumkin:

O'zingizda massiv obyektlari bor deb faraz qiling:

```
$scope.cars = [
  {model : "Ford Mustang", color : "red"},
  {model : "Fiat 500", color : "white"},
  {model : "Volvo XC90", color : "black"}
];
```

{% code title="ng-repeat-dan foydalanish:" %}
```
<select ng-model="selectedCar">
  <option ng-repeat="x in cars" value="{{x.model}}">{{x.model}}</option>
</select>

<h1>You selected: {{selectedCar}}</h1>
```
{% endcode %}

Qiymatni obyekt sifatida ishlatganda, `ng-value` o'rniga `value`dan foydalaning:

{% code title="ng-repeat-dan obyekt sifatida foydalanish:" %}
```
<select ng-model="selectedCar">
  <option ng-repeat="x in cars" ng-value="{{x}}">{{x.model}}</option>
</select>

<h1>You selected a {{selectedCar.color}} {{selectedCar.model}}</h1>
```
{% endcode %}

{% code title="ng-options-dan foydalanish:" %}
```
<select ng-model="selectedCar" ng-options="x.model for x in cars">
</select>

<h1>You selected: {{selectedCar.model}}</h1>
<p>Its color is: {{selectedCar.color}}</p>
```
{% endcode %}

Tanlangan qiymat obyekt bo'lsa, u ko'proq ma'lumotga ega bo'lishi mumkin va ilovangiz yanada moslashuvchan bo'lishi mumkin.

Ushbu qo'llanmada biz `ng-options` direktivasidan foydalanamiz.

### Obyekt sifatida data sourcedan foydalanish&#x20;

Avvalgi misollarda ma'lumotlar manbai massiv edi, lekin biz obyektdan ham foydalanishimiz mumkin.

O'zingizda kalit-qiymat juftligi bo'lgan obyekt bor deb faraz qiling:

```
$scope.cars = {
  car01 : "Ford",
  car02 : "Fiat",
  car03 : "Volvo"
};
```

`ng-options` atributidagi expression obyektlarda biroz farq qiladi:

{% code title="Obyektdan ma'lumot manbai sifatida foydalanishda, x kalitni, y esa qiymatni ifodalaydi:" %}
```
<select ng-model="selectedCar" ng-options="x for (x, y) in cars">
</select>

<h1>You selected: {{selectedCar}}</h1>
```
{% endcode %}

Tanlangan qiymat har doim kalit:qiymat juftligidagi qiymat bo'ladi .

**Kalit**:**qiymat** juftligidagi qiymat ham obyekt bo'lishi mumkin:

{% code title="Tanlangan qiymat kalit:qiymat juftligidagi qiymat bo'lib qoladi , faqat bu safar u obyekt bo'ladi:" %}
```
$scope.cars = {
  car01 : {brand : "Ford", model : "Mustang", color : "red"},
  car02 : {brand : "Fiat", model : "500", color : "white"},
  car03 : {brand : "Volvo", model : "XC90", color : "black"}
};
```
{% endcode %}

Dropdown ro'yxatidagi parametrlar **kalit:qiymat** juftligidagi **kalit** bo'lishi shart emas , u qiymat obyektining qiymati yoki xususiyati ham bo'lishi mumkin:

```
<select ng-model="selectedCar" ng-options="y.brand for (x, y) in cars">
</select>
```
