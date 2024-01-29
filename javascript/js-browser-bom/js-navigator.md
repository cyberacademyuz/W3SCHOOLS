# JS Navigator

`window.navigator` obyekti tashrif buyuruvchining brauzeri haqidagi ma'lumotlarni o'z ichiga oladi.

### Window Navigator

`window.navigator` obyekti window qo'shimchasisiz ham yozilishi mumkin.

Uning ba'zi metodlari:

* `navigator.cookieEnabled`
* `navigator.appCodeName`
* `navigator.platform`

### Brauzer kukilari

Agar cookie-fayllar yoqilgan bo'lsa, `cookieEnabled` xususiyati "true", qiymatini agar o'chirilgan bo'lsa "false" qiymatini qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML =
"cookiesEnabled is " + navigator.cookieEnabled;
</script>
```

### Brauzer ilovasi nomi

`appName` xususiyati brauzerning ilova nomini qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML =
"navigator.appName is " + navigator.appName;
</script>
```

{% hint style="danger" %}
### Ogohlantirish

Bu xususiyat eng soʻnggi veb-standartda olib tashlangan.

Ko'pgina brauzerlar (IE11, Chrome, Firefox, Safari) Netscape-ni appName sifatida qaytaradi.
{% endhint %}

### Brauzer ilovasining kod nomi

`appCodeName` xususiyati brauzerning ilova kod nomini qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML =
"navigator.appCodeName is " + navigator.appCodeName;
</script>
```

{% hint style="danger" %}
### Ogohlantirish

Bu xususiyat eng soʻnggi veb-standartda olib tashlangan (eskirgan).

Ko'pgina brauzerlar (IE11, Chrome, Firefox, Safari, Opera) Mozilla-ni appCodeName sifatida qaytaradi.
{% endhint %}

### Brauzer dvigateli

`product` xususiyati brauzer mexanizmining product nomini qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML =
"navigator.product is " + navigator.product;
</script>
```

{% hint style="danger" %}
### Ogohlantirish

Bu xususiyat eng soʻnggi veb-standartda olib tashlangan (eskirgan).

Ko'pgina brauzerlar Gecko-ni product sifatida qaytaradi.
{% endhint %}

### Brauzer versiyasi

`appVersion` xususiyati brauzerning versiya ma'lumotlarini qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = navigator.appVersion;
</script>
```

### Brauzer agenti

`userAgent` xususiyati brauzer tomonidan serverga yuborilgan user-agent headerini qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = navigator.userAgent;
</script>
```

{% hint style="danger" %}
### Ogohlantirish

Navigator obyektidagi ma'lumotlar ko'pincha noto'g'ri bo'lishi mumkin.

Navigator obyekti brauzer versiyalarini aniqlash uchun ishlatilmasligi kerak, chunki:

* Turli xil brauzerlar bir xil nomdan foydalanishlari mumkin
* Navigator ma'lumotlari brauzer egasi tomonidan o'zgartirilishi mumkin
* Ba'zi brauzerlar sayt sinovlarini chetlab o'tish uchun o'zlarini noto'g'ri identifikatlashadi
* Brauzerlar brauzerdan keyin chiqarilgan yangi operatsion tizimlar haqida xabar bera olmaydi
{% endhint %}

### Brauzer Platform

`platform` xususiyati brauzer platformasini (operatsion tizimni) qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = navigator.platform;
</script>
```

### Brauzer tili

`language` xususiyat brauzer tilini qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = navigator.language;
</script>
```

### Brauzer onlaynmi ?

Agar brauzer onlayn bo'lsa, `onLine` xususiyat "true" qiymat qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = navigator.onLine;
</script>
```

### Java yoqilganmi?

[Agar Java](https://www-w3schools-com.translate.goog/java/default.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) yoqilgan bo'lsa, `javaEnabled()` metodi true qiymat qaytaradi:

```
<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = navigator.javaEnabled();
</script>
```
