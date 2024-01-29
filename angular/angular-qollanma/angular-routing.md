# Angular Routing

Modul `ngRoute`ilovangizga bitta sahifali ilovaga aylanishiga yordam beradi.

### AngularJS da marshrutlash nima?

Agar siz ilovangizdagi turli sahifalarga oʻtmoqchi boʻlsangiz, lekin ilova sahifani qayta yuklamasdan, SPA (Yagona sahifali ilova) boʻlishini ham istasangiz, moduldan foydalanishingiz mumkin `ngRoute`.

Modul ilovangizni butun ilovani qayta yuklamasdan turli sahifalarga `ngRoute`yo‘naltiradi _._

{% code title=""red.htm", "green.htm" va "blue.htm" ga o'ting:" %}
```
<body ng-app="myApp">

<p><a href="#/!">Main</a></p>

<a href="#!red">Red</a>
<a href="#!green">Green</a>
<a href="#!blue">Blue</a>

<div ng-view></div>

<script>
var app = angular.module("myApp", ["ngRoute"]);
app.config(function($routeProvider) {
  $routeProvider
  .when("/", {
    templateUrl : "main.htm"
  })
  .when("/red", {
    templateUrl : "red.htm"
  })
  .when("/green", {
    templateUrl : "green.htm"
  })
  .when("/blue", {
    templateUrl : "blue.htm"
  });
});
</script>
</body>
```
{% endcode %}

### Menga nima kerak?

Ilovalaringizni marshrutlashga tayyor qilish uchun siz AngularJS Route modulini kiritishingiz kerak:

```
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular-route.js"></script>
```

`ngRoute`Keyin ilova moduliga bog'liqlik sifatida qo'shishingiz kerak :

```
var app = angular.module("myApp", ["ngRoute"]);
```

Endi sizning ilovangiz marshrut moduliga kirish huquqiga ega, u `$routeProvider`

`$routeProvider`Ilovangizdagi turli marshrutlarni sozlash uchun foydalaning:

```
app.config(function($routeProvider) {
  $routeProvider
  .when("/", {
    templateUrl : "main.htm"
  })
  .when("/red", {
    templateUrl : "red.htm"
  })
  .when("/green", {
    templateUrl : "green.htm"
  })
  .when("/blue", {
    templateUrl : "blue.htm"
  });
});
```

### Qayerga ketadi?

Ilovangizga marshrutlash tomonidan taqdim etilgan tarkibni joylashtirish uchun konteyner kerak.

Ushbu konteyner `ng-view`direktiv hisoblanadi.

`ng-view`Direktivni arizangizga kiritishning uch xil usuli mavjud :

```
<div ng-view></div>
```

```
<ng-view></ng-view>
```

```
<div class="ng-view"></div>
```

Ilovalar faqat bitta `ng-view`direktivaga ega bo'lishi mumkin va bu marshrut tomonidan taqdim etilgan barcha ko'rinishlar uchun to'ldiruvchi bo'ladi.

### $routeProvider

Uning yordamida `$routeProvider`siz foydalanuvchi havolani bosganida qaysi sahifani ko'rsatishni belgilashingiz mumkin.

{% code title="a ni aniqlang $routeProvider:" %}
```
var app = angular.module("myApp", ["ngRoute"]);
app.config(function($routeProvider) {
  $routeProvider
  .when("/", {
    templateUrl : "main.htm"
  })
  .when("/london", {
    templateUrl : "london.htm"
  })
  .when("/paris", {
    templateUrl : "paris.htm"
  });
});
```
{% endcode %}

Ilovangizdan `$routeProvider`foydalanish usulini aniqlang . `config`Usulda ro'yxatdan o'tgan ish `config`dastur yuklanganda amalga oshiriladi.

### Kontrollerlar

Uning yordamida `$routeProvider`siz har bir "ko'rinish" uchun kontrollerni ham belgilashingiz mumkin.

{% code title="Kontrollerlarni qo'shing:" %}
```
var app = angular.module("myApp", ["ngRoute"]);
app.config(function($routeProvider) {
  $routeProvider
  .when("/", {
    templateUrl : "main.htm"
  })
  .when("/london", {
    templateUrl : "london.htm",
    controller : "londonCtrl"
  })
  .when("/paris", {
    templateUrl : "paris.htm",
    controller : "parisCtrl"
  });
});
app.controller("londonCtrl", function ($scope) {
  $scope.msg = "I love London";
});
app.controller("parisCtrl", function ($scope) {
  $scope.msg = "I love Paris";
});
```
{% endcode %}

"London.htm" va "paris.htm" oddiy HTML fayllar bo'lib, siz AngularJS ilovangizning boshqa HTML bo'limlari kabi AngularJS ifodalarini qo'shishingiz mumkin.

Fayllar quyidagicha ko'rinadi:

{% code title="london.htm" %}
```
<h1>London</h1>
<h3>London is the capital city of England.</h3>
<p>It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
<p>{{msg}}</p>
```
{% endcode %}

{% code title="paris.htm" %}
```
<h1>Paris</h1>
<h3>Paris is the capital city of France.</h3>
<p>The Paris area is one of the largest population centers in Europe, with more than 12 million inhabitants.</p>
<p>{{msg}}</p>
```
{% endcode %}

### Shablon

Oldingi misollarda biz `templateUrl`usulda xususiyatdan foydalanganmiz `$routeProvider.when`.

`template`Siz HTML-ni sahifaga murojaat qilmasdan, to'g'ridan-to'g'ri xususiyat qiymatiga yozish imkonini beruvchi xususiyatdan foydalanishingiz mumkin .

{% code title="Shablonlarni yozing:" %}
```
var app = angular.module("myApp", ["ngRoute"]);
app.config(function($routeProvider) {
  $routeProvider
  .when("/", {
    template : "<h1>Main</h1><p>Click on the links to change this content</p>"
  })
  .when("/banana", {
    template : "<h1>Banana</h1><p>Bananas contain around 75% water.</p>"
  })
  .when("/tomato", {
    template : "<h1>Tomato</h1><p>Tomatoes contain around 95% water.</p>"
  });
});
```
{% endcode %}

### Boshqa usul

Oldingi misollarda biz `when`usulidan foydalanganmiz `$routeProvider`.

`otherwise`Boshqalardan hech biri mos kelmasa, standart yo'nalish bo'lgan usuldan ham foydalanishingiz mumkin .

{% code title="Agar "Banan" yoki "Pomidor" havolasi bosilmasa, ularga xabar bering:" %}
```
var app = angular.module("myApp", ["ngRoute"]);
app.config(function($routeProvider) {
  $routeProvider
  .when("/banana", {
    template : "<h1>Banana</h1><p>Bananas contain around 75% water.</p>"
  })
  .when("/tomato", {
    template : "<h1>Tomato</h1><p>Tomatoes contain around 95% water.</p>"
  })
  .otherwise({
    template : "<h1>None</h1><p>Nothing has been selected</p>"
  });
});
```
{% endcode %}
