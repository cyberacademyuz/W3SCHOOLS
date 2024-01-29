# Angular Servislar

AngularJS-da o'zingizning servisingizni yaratishingiz yoki ko'plab built-in servislardan birini ishlatishingiz mumkin.

### Servis nima ?

Servis bu AngularJS ilovangiz uchun mavjud va ular bilan cheklangan funksiya yoki obyekt hisoblanadi.

AngularJS 30 ga yaqin built-in servislarga ega. Ulardan biri `$location` servisidir.

`$location` servisida joriy veb-sahifaning joylashuvi haqidagi ma'lumotlarni qaytaradigan metodlar mavjud:

{% code title="$locationXizmatdan kontrollerda foydalaning :" %}
```
var app = angular.module('myApp', []);
app.controller('customersCtrl', function($scope, $location) {
    $scope.myUrl = $location.absUrl();
});
```
{% endcode %}

E'tibor bering, `$location` servisi kontrollerga argument sifatida uzatiladi. Controllerda servisdan foydalanish uchun u qaramlik sifatida belgilanishi kerak.

### Nima uchun servisdan foydalanish kerak ?

`$location` xizmati kabi koʻplab servislar uchun DOMda allaqachon mavjud boʻlgan obyektlardan, masalan, `window.location` obyektidan foydalanishingiz mumkin lekin hech bo'lmaganda AngularJS ilovangiz uchun ba'zi cheklovlar bo'ladi.

AngularJS ilovangizni doimiy ravishda nazorat qiladi va o'zgarishlar va hodisalarni to'g'ri ishlashi uchun AngularJS `window.location` obyekti o'rniga `$location` servisidan foydalanishni afzal ko'radi.

### $http servisi

Ushbu `$http` servisi AngularJS ilovalarida eng ko'p ishlatiladigan servislardan biridir. Servis serverga so'rov yuboradi va ilovangizga javobni boshqarishga imkon beradi.

{% code title="Serverdan ma'lumotlarni so'rash uchun $http xizmatidan foydalanish:" %}
```
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope, $http) {
  $http.get("welcome.htm").then(function (response) {
    $scope.myWelcome = response.data;
  });
});
```
{% endcode %}

Ushbu misol `$http` servisidan juda oddiy foydalanishni ko'rsatadi. AngularJS Http qo'llanmasida `$http` servisi haqida batafsil bilib oling.

### $timeout servisi

`$timeout` servisi `window.setTimeout` funksiyasining AngularJS versiyasidir.

{% code title="Ikki soniyadan so'ng yangi xabarni ko'rsatish:" %}
```
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope, $timeout) {
  $scope.myHeader = "Hello World!";
  $timeout(function () {
    $scope.myHeader = "How are you today?";
  }, 2000);
});
```
{% endcode %}

### $interval servjsj

`$interval` servisi `window.setInterval` funksiyasining AngularJS versiyasidir.

{% code title="Vaqtni har soniyada ko'rsatish:" %}
```
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope, $interval) {
  $scope.theTime = new Date().toLocaleTimeString();
  $interval(function () {
    $scope.theTime = new Date().toLocaleTimeString();
  }, 1000);
});
```
{% endcode %}

### O'z servisingizni yaratish

O'z servisingizni yaratish uchun servisingizni modulga ulang:

{% code title="hexafy nomli servjs yaratish:" %}
```
app.service('hexafy', function() {
  this.myFunc = function (x) {
    return x.toString(16);
  }
});
```
{% endcode %}

Maxsus tayyorlangan servisdan foydalanish uchun controllerni belgilashda uni qaram sifatida qo'shing:

{% code title="Raqamni o'n oltilik raqamga aylantirish uchun maxsus tayyorlangan hexafy servisidan foydalanish :" %}
```
app.controller('myCtrl', function($scope, hexafy) {
  $scope.hex = hexafy.myFunc(255);
});
```
{% endcode %}

### Filtr ichida maxsus servisdan foydalanish

Servisni yaratganingizdan va uni ilovangizga ulaganingizdan so'ng, servisdan istalgan kontroller, direktiva, filtr yoki hatto boshqa servislar ichida foydalanishingiz mumkin.

Filtr ichidagi servisdan foydalanish uchun filtrni belgilashda uni bog'liqlik sifatida qo'shing:

{% code title="Filtrda ishlatiladigan hexafy xizmat myFormat:" %}
```
app.filter('myFormat',['hexafy', function(hexafy) {
  return function(x) {
    return hexafy.myFunc(x);
  };
}]);
```
{% endcode %}

Obyekt yoki massivdagi qiymatlarni ko'rsatishda filtrdan foydalanishingiz mumkin:

<pre><code><strong>&#x3C;ul>
</strong>  &#x3C;li ng-repeat="x in counts">{{x | myFormat}}&#x3C;/li>
<strong>&#x3C;/ul>
</strong></code></pre>
