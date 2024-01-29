# Angular Formalar

AngularJS-dagi formalar ma'lumotlarni bog'lash va input  boshqaruvlarini tekshirishni ta'minlaydi.

### Input boshqaruvlari

Kirish boshqaruv elementlari HTML kiritish elementlari:

* nput elementlari
* select elementlari
* button elementlari
* textarea elementlari

### Ma'lumotlarni bog'lash

Input boshqaruvlari `ng-model` direktivasi yordamida ma'lumotlarni bog'lashni ta'minlaydi.

```
<input type="text" ng-model="firstname">
```

Endi ilovada `firstname` nomli xususiyat mavjud.

`ng-model` direktivasi input boshqaruvchisini ilovangizning qolgan qismiga bog'laydi.

`firstname` xususiyati kontrollerda ko'rsatilishi mumkin:

```
<script>
var app = angular.module('myApp', []);
app.controller('formCtrl', function($scope) {
  $scope.firstname = "John";
});
</script>
```

Bundan tashqari, ilovaning boshqa joyiga ham murojaat qilish mumkin:

```
<form>
  First Name: <input type="text" ng-model="firstname">
</form>

<h1>You entered: {{firstname}}</h1>
```

### Checkbox

Checkbox `true` yoki `false` qiymatiga ega bo'ladi. `ng-model` direktivasini checkboxga qo'llang va uning qiymatini ilovangizda ishlating.

{% code title="Checkbox belgilanganda, sarlavhani ko'rsatish:" %}
```
<form>
  Check to show a header:
  <input type="checkbox" ng-model="myVar">
</form>

<h1 ng-show="myVar">My Header</h1>
```
{% endcode %}

### Radio tugmalari

`ng-model` direktivasi yordamida radio tugmachalarini ilovangizga bog'lang.

Xuddi shu `ng-model`ga ega bo'lgan radio tugmalari turli qiymatlarga ega bo'lishi mumkin, lekin faqat tanlanganidan foydalaniladi.

{% code title="Tanlangan radio tugma qiymatiga asoslangan ba'zi matnlarni ko'rsatish:" %}
```
<form>
  Pick a topic:
  <input type="radio" ng-model="myVar" value="dogs">Dogs
  <input type="radio" ng-model="myVar" value="tuts">Tutorials
  <input type="radio" ng-model="myVar" value="cars">Cars
</form>
```
{% endcode %}

`myVar`ning qiymati `dogs`, `tuts` yoki `cars` bo'ladi.

### Selectbox

`ng-model` direktivasi yordamida ilovangizga selectboxlarni bog'lang.

`ng-model` atributida tuzilgan xususiyat selectboxda tanlangan variantning qiymatiga ega bo'ladi.

{% code title="Tanlangan variantning qiymatiga asoslanib, ba'zi matnlarni ko'rsatish:" %}
```
<form>
  Select a topic:
  <select ng-model="myVar">
    <option value="">
    <option value="dogs">Dogs
    <option value="tuts">Tutorials
    <option value="cars">Cars
  </select>
</form>
```
{% endcode %}

`myVar` qiymati yoki `dogs`, `tuts` yoki `cars` bo'ladi.

### AngularJS Formaga misol

![](<../../.gitbook/assets/image (125).png>)

forma = {"firstName":"Jon","familiya":"Doe"}

master = {"firstName":"Jon","familiya":"Doe"}

### Ilova kodi

```
<div ng-app="myApp" ng-controller="formCtrl">
  <form novalidate>
    First Name:<br>
    <input type="text" ng-model="user.firstName"><br>
    Last Name:<br>
    <input type="text" ng-model="user.lastName">
    <br><br>
    <button ng-click="reset()">RESET</button>
  </form>
  <p>form = {{user}}</p>
  <p>master = {{master}}</p>
</div>

<script>
var app = angular.module('myApp', []);
app.controller('formCtrl', function($scope) {
  $scope.master = {firstName: "John", lastName: "Doe"};
  $scope.reset = function() {
    $scope.user = angular.copy($scope.master);
  };
  $scope.reset();
});
</script>
```

{% hint style="warning" %}
Novalidate atributi HTML5 da yangi**.** U har qanday standart brauzer tekshiruvini o'chiradi.
{% endhint %}

### Misolni tushuntirish

**Ng-app** direktivasi AngularJS ilovasini yaratadi.

**Ng-controller** direktivasi dastur controllerini yaratadi.

**Ng-model** direktivasi modeldagi **user** obyektiga ikkita input elementini bog'laydi.

**formCtrl** kontrolleri **master** obyektiga dastlabki qiymatlarni o'rnatadi va **reset()** metodini belgilaydi.

**reset()** metidu **user** obyektini **master** obyektiga tenglashtiradi.

**Ng-click** direktivasi tugma bosilganda **reset()** metodini chaqiradi.

Ushbu ilova uchun **novalidate** atributi kerak emas, lekin odatda standart HTML5 tekshiruvini bekor qilish uchun uni AngularJS formalarida ishlatasiz.
