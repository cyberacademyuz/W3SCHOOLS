# jQuery Selektorlar

### jQuery va JavaScript

[jQuery](https://www.w3schools.com/jquery/default.asp) 2006 yilda Jon Resig tomonidan yaratilgan. U brauzerning nomuvofiqliklarini boshqarish va HTML DOM manipulyatsiyasini, hodisalarni boshqarish, animatsiyalar va Ajaxni soddalashtirish uchun mo'ljallangan.

10 yildan ortiq vaqt davomida jQuery dunyodagi eng mashhur JavaScript kutubxonasi bo'lib kelgan.

Biroq, JavaScript-ning [5-versiyasi](https://www.w3schools.com/js/js\_es5.asp)dan (2009) so'ng, jQuery qulayliklarining aksariyatini standart JavaScriptda bir necha qator kod orqali amalga oshirish mumkin:

### HTML elementini id orqali topish

Elementni id = "id01"  yordamida qaytarish:

{% code title="jQuery:" %}
```
myElement = $("#id01");
```
{% endcode %}

{% code title="JavaScript:" %}
```
myElement = document.getElementById("id01");
```
{% endcode %}

### HTML elementlarini teg nomi bo'yicha topish

Barcha \<p> elementlarini qaytarish:

{% code title="jQuery:" %}
```
myElements = $("p");
```
{% endcode %}

{% code title="JavaScript:" %}
```
myElements = document.getElementsByTagName("p");
```
{% endcode %}

### HTML elementlarini class nomi bo'yicha topish

class="intro" yordamida barcha elementlarni qaytarish.

{% code title="jQuery:" %}
```
myElements = $(".intro");
```
{% endcode %}

{% code title="JavaScript:" %}
```
myElements = document.getElementsByClassName("intro");
```
{% endcode %}

### HTML elementlarini CSS selektorlari yordamida topish

class="intro"  orqali barcha \<p> elementlar ro'yxatini qaytarish.

{% code title="jQuery:" %}
```
myElements = $("p.intro");
```
{% endcode %}

{% code title="JavaScript:" %}
```
myElements = document.querySelectorAll("p.intro");
```
{% endcode %}
