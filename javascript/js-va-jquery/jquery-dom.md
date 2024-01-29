# jQuery DOM

### jQuery va JavaScript

[jQuery](https://www.w3schools.com/jquery/default.asp) 2006 yilda Jon Resig tomonidan yaratilgan. U brauzerning nomuvofiqliklarini boshqarish va HTML DOM manipulyatsiyasini, hodisalarni boshqarish, animatsiyalar va Ajaxni soddalashtirish uchun mo'ljallangan.

10 yildan ortiq vaqt davomida jQuery dunyodagi eng mashhur JavaScript kutubxonasi bo'lib kelgan.

Biroq, JavaScript-ning [5-versiyasi](https://www.w3schools.com/js/js\_es5.asp)dan (2009) so'ng, jQuery qulayliklarining aksariyatini standart JavaScriptda bir necha qator kod orqali amalga oshirish mumkin:

### HTML elementlarini olib tashlash

HTML elementini olib tashlash:

{% code title="jQuery:" %}
```
$("#id02").remove();
```
{% endcode %}

{% code title="JavaScript:" %}
```
document.getElementById("id02").remove();
```
{% endcode %}

### Ota-ona elementini olish

Elementning ota-ona elementini qaytarish:

{% code title="jQuery:" %}
```
myParent = $("#02").parent().prop("nodeName"); ;
```
{% endcode %}

{% code title="JavaScript:" %}
```
myParent = document.getElementById("02").parentNode.nodeName;
```
{% endcode %}
