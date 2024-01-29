# Angular Expressionlar

AngularJS ma'lumotlarni **Expressionlar** yordamida HTML bilan bog'laydi.

### AngularJS expressionlari

AngularJS expressionlarini ikkita qavs ichida yozish mumkin: .`{{`_`expression`_`}}`

AngularJS expressionlari direktiv ichida ham yozilishi mumkin: .`ng-bind="`_`expression`_`"`

AngularJS expressionni bajaradi va natijani expression yozilgan joyga qaytaradi.

**AngularJS** expressionlari JavaScript expressionlari juda oʻxshaydi**:** ular literallar, operatorlar va oʻzgaruvchilarni oʻz ichiga olishi mumkin.

Misol \{{ 5 + 5 \}} yoki \{{ firstName + " " + familiyasi \}}

```
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
  <p>My first expression: {{ 5 + 5 }}</p>
</div>

</body>
</html>
```

Agar `ng-app` direktivasini olib tashlasangiz, HTML expressionni bajaramasdan ko'rsatadi:

```
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div>
  <p>My first expression: {{ 5 + 5 }}</p>
</div>

</body>
</html>

```

Expressionlarni xohlagan joyda yozishingiz mumkin, AngularJS shunchaki expressionni bajaradi va natijani qaytaradi.

Misol: AngularJS CSS xususiyatlarining qiymatini o'zgartirishi.

Quyidagi input maydonining rangini uning qiymatini o'zgartirish orqali o'zgartiring:

![](<../../.gitbook/assets/image (97).png>)

```
<div ng-app="" ng-init="myCol='lightblue'">

<input style="background-color:{{myCol}}" ng-model="myCol">

</div>
```

### AngularJS Raqamlar

AngularJSda raqamlar JavaScript raqamlariga o'xshaydi:

```
<div ng-app="" ng-init="quantity=1;cost=5">

<p>Total in dollar: {{ quantity * cost }}</p>

</div>
```

Xuddi shu misol `ng-bind` yordamida:

```
<div ng-app="" ng-init="quantity=1;cost=5">

<p>Total in dollar: <span ng-bind="quantity * cost"></span></p>

</div>
```

{% hint style="warning" %}
`ng-init`dan foydalanish keng tarqalmagan. Kontrollerlar haqidagi bo'limda ma'lumotlarni ishga tushirishning yaxshiroq usulini bilib olasiz.
{% endhint %}

### AngularJS Stringlar

AngularJSDA Stringlar JavaScript stringlariga o'xshaydi:

```
<div ng-app="" ng-init="firstName='John';lastName='Doe'">

<p>The name is {{ firstName + " " + lastName }}</p>

</div>
```

Xuddi shu misol `ng-bind` yordamida:

```
<div ng-app="" ng-init="firstName='John';lastName='Doe'">

<p>The name is <span ng-bind="firstName + ' ' + lastName"></span></p>

</div>
```

### AngularJS Obyektlar

AngularJSda obyektlar JavaScript obyektlariga o‘xshaydi:

```
<div ng-app="" ng-init="person={firstName:'John',lastName:'Doe'}">

<p>The name is {{ person.lastName }}</p>

</div>
```

Xuddi shu misol `ng-bind` yordamida:

```
<div ng-app="" ng-init="person={firstName:'John',lastName:'Doe'}">

<p>The name is <span ng-bind="person.lastName"></span></p>

</div>
```

### AngularJS Massivlar

AngularJSda massivlar JavaScript massivlariga o'xshaydi:

```
<div ng-app="" ng-init="points=[1,15,19,2,40]">

<p>The third result is {{ points[2] }}</p>

</div>
```

Xuddi shu misol `ng-bind` yordamida:

```
<div ng-app="" ng-init="points=[1,15,19,2,40]">

<p>The third result is <span ng-bind="points[2]"></span></p>

</div>
```

### AngularJS expressionlari va JavaScript expressionlari

JavaScript expressionlari singari, AngularJS expressionlari ham harflar, operatorlar va o'zgaruvchilarni o'z ichiga olishi mumkin.

JavaScript expressionlaridan farqli o'laroq, AngularJS expressionlari HTML ichida yozilishi mumkin.

AngularJS expressionlari shartlar, tsikllar va exceptionlarni qo'llab-quvvatlamaydi, JavaScript ifodalari esa bularni qo'llab quvvatlaydi.

AngularJS expressionlari filtrlarni qo'llab-quvvatlaydi, JavaScript expressionlari esa qo'llab quvvatlamaydi.

JavaScript-ni bizning [JavaScript](broken-reference) qo'llanmamizda o'rganing.
