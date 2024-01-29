# JS Location

`window.location` obyekti joriy sahifa manzilini (URL) olish va brauzerni yangi sahifaga yo'naltirish uchun ishlatilishi mumkin.

### Window Location

`window.location` obyekti window qo'shimchasisiz ham yozilishi mumkin.

Uning ba'zi metodlari:

* `window.location.href`joriy sahifaning URLni qaytaradi
* `window.location.hostname` veb-xostning domen nomini qaytaradi
* `window.location.pathname` joriy sahifaning yo'li va fayl nomini qaytaradi
* `window.location.protocol` foydalanilgan veb-protokolni qaytaradi (`http:` yoki `https:`)
* `window.location.assign()`yangi hujjatni yuklaydi

### Window Location Href

`window.location.href` xususiyati joriy sahifaning URL manzilini qaytaradi.

{% code title="Joriy sahifaning URLini ko‘rsatish:" %}
```
document.getElementById("demo").innerHTML =
"Page location is " + window.location.href;
```
{% endcode %}

{% code title="Natija:" %}
```
Page location is https://www-w3schools-com.translate.goog/js/js_window_location.asp?_x_tr_sl=ru&_x_tr_tl=uz&_x_tr_hl=en&_x_tr_pto=wapp
```
{% endcode %}

### Window Location Hostname

`window.location.hostname` xususiyati websayt xost nomini qaytaradi.

{% code title="Xost nomini ko'rsatish:" %}
```
document.getElementById("demo").innerHTML =
"Page hostname is " + window.location.hostname;
```
{% endcode %}

{% code title="Natija:" %}
```
Page hostname is www-w3schools-com.translate.goog
```
{% endcode %}

### Window Location Pathname

`window.location.pathname` xususiyati joriy sahifaning yo'l nomini qaytaradi.

{% code title="Joriy URL manzilining yo‘l nomini ko‘rsating:" %}
```
document.getElementById("demo").innerHTML =
"Page path is " + window.location.pathname;
```
{% endcode %}

{% code title="Natija:" %}
```
Page path is /js/js_window_location.asp
```
{% endcode %}

### Window Location Protocol

`window.location.protocol` xususiyati sahifaning veb-protokolini qaytaradi.

{% code title="Veb-protokolni ko'rsatish:" %}
```
document.getElementById("demo").innerHTML =
"Page protocol is " + window.location.protocol;
```
{% endcode %}

{% code title="Natija:" %}
```
Page protocol is https:
```
{% endcode %}

### Window Location Port

`window.location.port` xususiyati websayt xost portining raqamini qaytaradi.

{% code title="Xost nomini ko'rsating:" %}
```
document.getElementById("demo").innerHTML =
"Port number is " + window.location.port;
```
{% endcode %}

{% code title="Natija:" %}
```
Port number is
```
{% endcode %}

{% hint style="warning" %}
Ko'pgina brauzerlar standart port raqamlarini ko'rsatmaydi (http uchun 80 va https uchun 443).
{% endhint %}

### Window Location Assign

`window.location.assign()` metodi yangi hujjatni yuklaydi.

{% code title="Yangi hujjat yuklang:" %}
```
<html>
<head>
<script>
function newDoc() {
  window.location.assign("https://www.w3schools.com")
}
</script>
</head>
<body>

<input type="button" value="Load new document" onclick="newDoc()">

</body>
</html>
```
{% endcode %}
