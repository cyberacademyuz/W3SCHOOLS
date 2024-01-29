# Angular Animatsiyalar

AngularJS CSS yordamida jonlantirilgan o'tishlarni ta'minlaydi.

### Animatsiya nima?

Animatsiya HTML elementining o'zgarishi sizga harakat illyuziyasini beradi.

{% code title="DIVni yashirish uchun katagiga belgi qo'ying:" %}
```
<body ng-app="ngAnimate">

Hide the DIV: <input type="checkbox" ng-model="myCheck">

<div ng-hide="myCheck"></div>

</body>
```
{% endcode %}

{% hint style="warning" %}
Ilovalar animatsiya bilan to'ldirilmasligi kerak, lekin ba'zi animatsiyalar dasturni tushunishni osonlashtirishi mumkin.
{% endhint %}

### Menga nima kerak?

Ilovalaringizni animatsiyalarga tayyor qilish uchun siz AngularJS Animate kutubxonasini qo'shishingiz kerak:

```
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular-animate.js"></script>
```

\
`ngAnimate`Keyin ilovangizdagi modulga murojaat qilishingiz kerak :

```
<body ng-app="ngAnimate">
```

Yoki ilovangizning nomi bo'lsa, `ngAnimate`ilova modulingizga qaramlik sifatida qo'shing:

```
<body ng-app="myApp">

<h1>Hide the DIV: <input type="checkbox" ng-model="myCheck"></h1>

<div ng-hide="myCheck"></div>

<script>
var app = angular.module('myApp', ['ngAnimate']);
</script>
```

### NgAnimate nima qiladi?

NgAnimate moduli sinflarni qo'shadi va o'chiradi.

NgAnimate moduli HTML elementlaringizni jonlantirmaydi, lekin ngAnimate HTML elementini yashirish yoki koʻrsatish kabi baʼzi hodisalarni sezganda, element animatsiyalarni yaratish uchun ishlatilishi mumkin boʻlgan oldindan belgilangan sinflarni oladi.

Sinflarni qo'shadigan/o'chiruvchi AngularJS direktivalari quyidagilardir:

* `ng-show`
* `ng-hide`
* `ng-class`
* `ng-view`
* `ng-include`
* `ng-repeat`
* `ng-if`
* `ng-switch`

va direktivalari sinf qiymatini qo'shadi yoki `ng-show`o'chiradi .`ng-hideng-hide`

Boshqa direktivalar `ng-enter`DOMga kirganda sinf qiymatini va `ng-leave`DOMdan olib tashlanganida atributni qo'shadi.

Direktiv shuningdek , HTML elementi o'rnini o'zgartirganda sinf qiymatini `ng-repeat`qo'shadi .`ng-move`

Bundan tashqari, animatsiya _paytida_ HTML elementi sinf qiymatlari to'plamiga ega bo'ladi, ular animatsiya tugagandan so'ng o'chiriladi. Misol: `ng-hide`direktiva quyidagi sinf qiymatlarini qo'shadi:

* `ng-animate`
* `ng-hide-animate`
* `ng-hide-add`(agar element yashirin bo'lsa)
* `ng-hide-remove`(agar element ko'rsatilsa)
* `ng-hide-add-active`(agar element yashirin bo'lsa)
* `ng-hide-remove-active`(agar element ko'rsatilsa)

### CSS yordamida animatsiyalar

HTML elementlarini jonlantirish uchun CSS o'tishlari yoki CSS animatsiyalaridan foydalanishimiz mumkin. Ushbu o'quv qo'llanma sizga ikkalasini ham ko'rsatadi.

CSS animatsiyasi haqida ko'proq ma'lumot olish uchun CSS o'tish bo'yicha qo'llanmamiz va CSS animatsiya qo'llanmamizni o'rganing.

### CSS o'tishlari

CSS o'tishlari sizga ma'lum vaqt davomida CSS xususiyati qiymatlarini bir qiymatdan ikkinchisiga muammosiz o'zgartirish imkonini beradi:

{% code title="DIV elementi sinfni olganida .ng-hide, o'tish 0,5 soniya davom etadi va balandlik 100px dan 0 gacha silliq o'zgaradi:" %}
```
<style>
div {
  transition: all linear 0.5s;
  background-color: lightblue;
  height: 100px;
}

.ng-hide {
  height: 0;
}
</style>

```
{% endcode %}

### CSS animatsiyalari

CSS Animations sizga ma'lum vaqt davomida CSS xususiyat qiymatlarini bir qiymatdan ikkinchisiga muammosiz o'zgartirish imkonini beradi:

{% code title="DIV elementi sinfni olganida .ng-hide, myChangeanimatsiya ishlaydi, bu balandlikni 100px dan 0 ga silliq o'zgartiradi:" %}
```
<style>
@keyframes myChange {
  from {
    height: 100px;
  } to {
    height: 0;
  }
}

div {
  height: 100px;
  background-color: lightblue;
}

div.ng-hide {
  animation: 0.5s myChange;
}
</style>
```
{% endcode %}
