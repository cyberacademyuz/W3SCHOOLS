---
description: Javascript HTML sahifalarni dinamik va interaktive qiladi
---

# Javascript

<figure><img src="../../.gitbook/assets/image (448).png" alt=""><figcaption></figcaption></figure>

## HTML \<script> tegi

HTMLning \<script> tegi client-side scriptlar yozish uchun ishlatiladi.&#x20;

\<script> elementi skript bayonotlari (statement-lar)ni ham o'z ichiga oladi yoki src atributi orqali tashqi skript fayllarni ulash mumkin.

JavaScriptdan rasmlarni boshqarish, formalarni tekshirish va saytda dinamik o'zgartirishlarni bajarish usullari keng qo'llaniladi.

Javascript orqali HTML elementini tanlashning keng tarqalgan usuli `document.getElementById()` metodidan foydalanishdir.

Ushbu misoldagi JavaScript kod id="demo" ga ega HTML elementga "Hello JavaScript!" so'zini yozadi.

```
<script>
document.getElementById("demo").innerHTML = "Hello JavaScript!";
</script> 
```

## Javascriptning ta'mi

Quyida JavaScript nimalar qila olishiga ba'zi misollar keltirilgan:

{% code title="Javascript kontentlarni o'zgartira oladi" %}
```
document.getElementById("demo").innerHTML = "Hello JavaScript!"; 
```
{% endcode %}

{% code title="Javascript stillarni o'zgartira oladi" %}
```
document.getElementById("demo").style.fontSize = "25px";
document.getElementById("demo").style.color = "red";
document.getElementById("demo").style.backgroundColor = "yellow"; 
```
{% endcode %}

{% code title="Javascript atributlarni o'zgartira oladi" %}
```
document.getElementById("image").src = "picture.gif"; 
```
{% endcode %}

## HTMLdagi \<noscript> teg

HTML \<noscript> tegi brauzerda skriptlar o'chirib qo'yilganida yoki saytga skriptlarni qo'llab-quvvatlamaydigan brauzerdan kirgan foydalanuvchilarga ko'rsatiladigan matnni o'z ichiga oladi.

```
<script>
document.getElementById("demo").innerHTML = "Hello JavaScript!";
</script>
<noscript>Sorry, your browser does not support JavaScript!</noscript> 
```

## HTML script teglari

| Teg         | Description                                                                                      |
| ----------- | ------------------------------------------------------------------------------------------------ |
| \<script>   | client-side script yaratish                                                                      |
| \<noscript> | Client-side scriptlarni qo'llab quvvatlamaydigan brauzerlarda ko'rsatiladigan matnni ifodalaydi. |
