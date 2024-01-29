# Angular Application

Haqiqiy AngularJS ilovasini yaratish vaqti keldi.

### Xarid qilish ro'yxatini tuzing

Elementlarni qo'shishingiz yoki olib tashlashingiz mumkin bo'lgan xaridlar ro'yxatini tuzish uchun AngularJSning ba'zi xususiyatlaridan foydalanamiz:

#### Mening xaridlar roʻyxatim

![](<../../.gitbook/assets/image (195).png>)

### Ilova tushuntirildi

#### 1-qadam. Ishni boshlash:

deb nomlangan ilova yaratishdan boshlang va unga `myShoppingList`boshqaruvchini qo'shing .`myCtrl`

`products`Tekshirish moslamasi joriy nomli massivni qo'shadi `$scope`.

HTMLda biz `ng-repeat`massivdagi elementlardan foydalangan holda ro'yxatni ko'rsatish uchun direktivadan foydalanamiz.

{% code title="Hozirgacha biz massiv elementlari asosida HTML ro'yxatini tuzdik:" %}
```
<script>
var app = angular.module("myShoppingList", []);
app.controller("myCtrl", function($scope) {
  $scope.products = ["Milk", "Bread", "Cheese"];
});</script>

<div ng-app="myShoppingList" ng-controller="myCtrl">
  <ul>
    <li ng-repeat="x in products">{{x}}</li>
  </ul>
</div>
```
{% endcode %}

#### 2-qadam. Elementlarni qo'shish:

HTMLda matn maydonini qo'shing va uni direktiv bilan ilovaga bog'lang `ng-model`.

Tekshirgichda nomli funktsiyani yarating va qatorga element qo'shish uchun kirish maydonining `addItem`qiymatidan foydalaning .`addMeproducts`

Tugma qo'shing va tugma bosilganda funksiyani `ng-click`ishga tushiradigan ko'rsatma bering .`addItem`

{% code title="Endi biz xaridlar ro'yxatiga narsalarni qo'shishimiz mumkin:" %}
```
<script>
var app = angular.module("myShoppingList", []);
app.controller("myCtrl", function($scope) {
  $scope.products = ["Milk", "Bread", "Cheese"];
  $scope.addItem = function () {
    $scope.products.push($scope.addMe);
  }
});
</script>

<div ng-app="myShoppingList" ng-controller="myCtrl">
  <ul>
    <li ng-repeat="x in products">{{x}}</li>
  </ul>
  <input ng-model="addMe">
  <button ng-click="addItem()">Add</button>
</div>
```
{% endcode %}

#### 3-qadam. Elementlarni olib tashlash:

Shuningdek, biz xaridlar ro'yxatidan narsalarni olib tashlashni xohlaymiz.

Tekshirish moslamasida `removeItem`siz olib tashlamoqchi bo'lgan elementning indeksini parametr sifatida qabul qiladigan funktsiyani yarating.

HTMLda `<span>`har bir element uchun element yarating va ularga joriy funksiyani `ng-click`chaqiradigan direktivani bering .`removeItem$index`

{% code title="Endi biz xaridlar ro'yxatidan narsalarni olib tashlashimiz mumkin:" %}
```
<script>
var app = angular.module("myShoppingList", []);
app.controller("myCtrl", function($scope) {
  $scope.products = ["Milk", "Bread", "Cheese"];
  $scope.addItem = function () {
    $scope.products.push($scope.addMe);
  }
  $scope.removeItem = function (x) {
    $scope.products.splice(x, 1);
  }
});
</script>

<div ng-app="myShoppingList" ng-controller="myCtrl">
  <ul>
    <li ng-repeat="x in products">
      {{x}}<span ng-click="removeItem($index)">&times;</span>
    </li>
  </ul>
  <input ng-model="addMe">
  <button ng-click="addItem()">Add</button>
</div>
```
{% endcode %}

#### 4-qadam. Xatolarni hal qilish:

Ilovada ba'zi xatolar bor, masalan, bir xil elementni ikki marta qo'shmoqchi bo'lsangiz, dastur ishdan chiqadi. Bundan tashqari, bo'sh narsalarni qo'shishga yo'l qo'ymaslik kerak.

Yangi elementlarni qo'shishdan oldin qiymatni tekshirish orqali buni tuzatamiz.

HTMLda biz xato xabarlari uchun konteyner qo'shamiz va kimdir mavjud elementni qo'shishga harakat qilganda xato xabari yozamiz.

{% code title="Xato xabarlarini yozish imkoniyatiga ega xaridlar ro'yxati:" %}
```
<script>
var app = angular.module("myShoppingList", []);
app.controller("myCtrl", function($scope) {
  $scope.products = ["Milk", "Bread", "Cheese"];
  $scope.addItem = function () {
    $scope.errortext = "";
    if (!$scope.addMe) {return;}
    if ($scope.products.indexOf($scope.addMe) == -1) {
      $scope.products.push($scope.addMe);
    } else {
      $scope.errortext = "The item is already in your shopping list.";
    }
  }
  $scope.removeItem = function (x) {
    $scope.errortext = "";
    $scope.products.splice(x, 1);
  }
});
</script>

<div ng-app="myShoppingList" ng-controller="myCtrl">
  <ul>
    <li ng-repeat="x in products">
      {{x}}<span ng-click="removeItem($index)">&times;</span>
    </li>
  </ul>
  <input ng-model="addMe">
  <button ng-click="addItem()">Add</button>
  <p>{{errortext}}</p>
</div>
```
{% endcode %}

#### 5-qadam. Dizayn:

Ilova ishlaydi, lekin yaxshiroq dizayndan foydalanishi mumkin. Ilovani uslublash uchun biz W3.CSS uslublar jadvalidan foydalanamiz.

W3.CSS uslublar jadvalini qo'shing va ilova bo'ylab tegishli sinflarni kiriting va natija ushbu sahifaning yuqori qismidagi xaridlar ro'yxati bilan bir xil bo'ladi.

W3.CSS uslublar jadvalidan foydalanib ilovangizni uslublang:

```
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
```
