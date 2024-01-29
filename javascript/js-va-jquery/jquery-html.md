# jQuery HTML

### jQuery va JavaScript

[jQuery](https://www.w3schools.com/jquery/default.asp) 2006 yilda Jon Resig tomonidan yaratilgan. U brauzerning nomuvofiqliklarini boshqarish va HTML DOM manipulyatsiyasini, hodisalarni boshqarish, animatsiyalar va Ajaxni soddalashtirish uchun mo'ljallangan.

10 yildan ortiq vaqt davomida jQuery dunyodagi eng mashhur JavaScript kutubxonasi bo'lib kelgan.

Biroq, JavaScript-ning [5-versiyasi](https://www.w3schools.com/js/js\_es5.asp)dan (2009) so'ng, jQuery qulayliklarining aksariyatini standart JavaScriptda bir necha qator kod orqali amalga oshirish mumkin:

### Matn tarkibini sozlash

HTML elementining ichki matnini o'rnatish:

{% code title="jQuery:" %}
```
myElement.text("Hello Sweden!");
```
{% endcode %}

{% code title="JavaScript:" %}
```
myElement.textContent = "Hello Sweden!";
```
{% endcode %}

### Matn tarkibini oling

HTML elementining matnini olish:

{% code title="jQuery:" %}
```
myText = $("#02").text();
```
{% endcode %}

{% code title="JavaScript:" %}
```
myText = document.getElementById("02").textContent;
```
{% endcode %}

### HTML tarkibini o'rnatish

Elementning HTML tarkibini o'rnatish:

{% code title="jQuery:" %}
```
myElement.html("<p>Hello World</p>");
```
{% endcode %}

{% code title="JavaScript:" %}
```
myElement.innerHTML = "<p>Hello World</p>";
```
{% endcode %}

### HTML tarkibini olish

Elementning HTML tarkibini olish:

{% code title="jQuery:" %}
```
content = myElement.html();
```
{% endcode %}

{% code title="JavaScript:" %}
```
content = myElement.innerHTML
```
{% endcode %}
