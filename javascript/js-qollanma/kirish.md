---
description: Ushbu sahifada JavaScript nimalar qila olishiga oid ba'zi misollar mavjud.
---

# Kirish

## JavaScript HTML tarkibini o'zgartirishi mumkin

HTML tarkibini o'zgartiruvchi ko'pgina Javascript metodlaridan biri `getElementById()`.

Quyidagi misol, HTML elementini (**id="demo"** orqali) topadi va elementning tarkibini (**innerHTML** yordamida) "Salom JavaScript" ga o'zgartiradi:

```javascript
document.getElementById("demo").innerHTML = "Salom JavaScript";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_inner_html" %}

{% hint style="warning" %}
Javascript bir tirnoq va qo'shtirnoqning ikkalasini ham qabul qiladi
{% endhint %}

```javascript
document.getElementById('demo').innerHTML = 'Salom JavaScript';
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_inner_html_quotes" %}

## JavaScript HTMLdagi atribut qiymatlarini o'zgartira oladi

Ushbu misolda JavaScript `<img>` elementidagi `src` atributining qiymatini o'zgartiradi:

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_lightbulb" %}

## JavaScript HTML stillarini o'zgartira oladi (CSS)

HTML elementining stillarini o'zgartirish HTML atributini o'zgartirishga :

```
document.getElementById("demo").style.fontSize = "35px";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_style" %}

### JavaScript HTML elementlarini yashirishi mumkin

HTML elementlarini yashirish `display` stilni o'zgartirish orqali amalga oshirilishi mumkin:

```
document.getElementById("demo").style.display = "none";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_hide" %}

## JavaScript yashirilgan HTML elementlarini ko'rsatishi mumkin

Yashirin HTML elementlarini ko'rsatish `display` stilini o'zgartirish orqali ham amalga oshirilishi mumkin:

```
document.getElementById("demo").style.display = "block";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_show" %}

{% hint style="warning" %}
### Bilasizmi?

JavaScript va [Java](https://www-w3schools-com.translate.goog/java/default.asp?\_x\_tr\_sl=en&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) kontseptsiyada ham, dizaynda ham, mutlaqo boshqa boshqa tillar hisoblanadi.

JavaScript 1995 yilda Brendan Eich tomonidan ixtiro qilingan va 1997 yilda ECMA standartiga aylandi.

**ECMA-262** standartning rasmiy nomi hisoblansa, **ECMAScript** - tilning rasmiy nomi hisoblanadi.

[Javascript versiyalari »](../js-versiyalari/js-versiyalari.md)
{% endhint %}
