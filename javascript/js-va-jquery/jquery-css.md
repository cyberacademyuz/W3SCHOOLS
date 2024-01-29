# jQuery CSS

### jQuery va JavaScript

[jQuery](https://www.w3schools.com/jquery/default.asp) 2006 yilda Jon Resig tomonidan yaratilgan. U brauzerning nomuvofiqliklarini boshqarish va HTML DOM manipulyatsiyasini, hodisalarni boshqarish, animatsiyalar va Ajaxni soddalashtirish uchun mo'ljallangan.

10 yildan ortiq vaqt davomida jQuery dunyodagi eng mashhur JavaScript kutubxonasi bo'lib kelgan.

Biroq, JavaScript-ning [5-versiyasi](https://www.w3schools.com/js/js\_es5.asp)dan (2009) so'ng, jQuery qulayliklarining aksariyatini standart JavaScriptda bir necha qator kod orqali amalga oshirish mumkin:

### HTML elementlarini yashirish

HTML elementini yashirish:

{% code title="jQuery:" %}
```
myElement.hide();
```
{% endcode %}

{% code title="JavaScript:" %}
```
myElement.style.display = "none";
```
{% endcode %}

### HTML elementlari ko'rsatish

HTML elementini ko'rsatish:

{% code title="jQuery:" %}
```
myElement.show();
```
{% endcode %}

{% code title="JavaScript:" %}
```
myElement.style.display = "";
```
{% endcode %}

### HTML elementlariga still berish

HTML elementining shrift o'lchamini o'zgartirish:

{% code title="jQuery:" %}
```
$("#demo").css("font-size","35px");
```
{% endcode %}

{% code title="JavaScript:" %}
```
document.getElementById("demo").style.fontSize = "35px";
```
{% endcode %}
