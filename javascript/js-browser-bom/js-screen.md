# JS Screen

window.screen obyekti foydalanuvchi ekrani haqidagi ma'lumotlarni o'z ichiga oladi.

### Window Screen

`window.screen` obyekti window qo'shimchasisiz ham yozilishi mumkin.

Uning xususiyatlari:

* `screen.width`
* `screen.height`
* `screen.availWidth`
* `screen.availHeight`
* `screen.colorDepth`
* `screen.pixelDepth`

### Window Screen kengligi

`screen.width` xususiyati tashrif buyuruvchi ekranining kengligini piksellarda qaytaradi.

{% code title="Ekranning kengligini piksellarda ko'rsatish:" %}
```
document.getElementById("demo").innerHTML =
"Screen Width: " + screen.width;
```
{% endcode %}

Natija quyidagicha bo'ladi:

```
Screen Width: 1366
```

### Window Screen balandligi

`screen.height` xususiyati tashrif buyuruvchi ekranining balandligini piksellarda qaytaradi.

{% code title="Ekran balandligini piksellarda ko'rsatish:" %}
```
document.getElementById("demo").innerHTML =
"Screen Height: " + screen.height;
```
{% endcode %}

Natija quyidagicha bo'ladi:

```
Screen Height: 768
```

### Window Screen-da mavjud kenglik

`screen.availWidth` xususiyati tashrif buyuruvchi ekranining kenglidan taskbar paneli kabi interfeys xususiyatlari egallab turgan joy o'lchamini ayirib qolgan natijani piksellarda qaytaradi.

{% code title="Ekranning mavjud kengligini piksellarda ko'rsating:" %}
```
document.getElementById("demo").innerHTML =
"Available Screen Width: " + screen.availWidth;
```
{% endcode %}

Natija quyidagicha bo'ladi:

```
Available Screen Width: 1366
```

### Window Screen-da mavjud balanligi

`screen.availHeight` xususiyati tashrif buyuruvchi ekranining balandligidan taskbar paneli kabi interfeys xususiyatlari egallab turgan joy o'lchamini ayirib qolgan natijani piksellarda qaytaradi.

{% code title="Ekranning mavjud balandligini piksellarda ko'rsating:" %}
```
document.getElementById("demo").innerHTML =
"Available Screen Height: " + screen.availHeight;
```
{% endcode %}

Natija quyidagicha bo'ladi:

```
Available Screen Height: 768
```

### Oyna ekranining rang o'tkirligi

&#x20;`screen.colorDepth` xususiyati bitta rangni ko'rsatish uchun ishlatiladigan bitlar sonini qaytaradi.

Barcha zamonaviy kompyuterlar rangni aniqlash uchun 24 bitli yoki 32 bitli qurilmadan foydalanadi:

* 24 bit = 16 777 216 xil "Haqiqiy ranglar"
* 32 bit = 4,294,967,296 xil "o'tkir ranglar"

Eskiroq kompyuterlar 16 bitdan foydalangan: 65 536 xil “Yuqori ranglar”ni ifodalay olgan.

Juda eski kompyuterlar va eski mobil telefonlar 8 bitdan foydalangan: 256 xil "VGA ranglari".

{% code title="Ekranning rang o'tkirligini bitlarda ko'rsating:" %}
```
document.getElementById("demo").innerHTML =
"Screen Color Depth: " + screen.colorDepth;
```
{% endcode %}

Natija quyidagicha bo'ladi:

```
Screen Color Depth: 24
```

{% hint style="warning" %}
HTML-da ishlatiladigan #rrggbb (rgb) qiymatlari "Haqiqiy ranglar" ni bildiradi (16 777 216 xil rang)
{% endhint %}

### Window Screen Pixelga to'yimliligi

`screen.pixelDepth` xususiyati ekranning piksel to'yimliligii qaytaradi.

{% code title="Ekranning piksel chuqurligini bitlarda ko'rsating:" %}
```
document.getElementById("demo").innerHTML =
"Screen Pixel Depth: " + screen.pixelDepth;
```
{% endcode %}

Natija quyidagicha bo'ladi:

```
Screen Pixel Depth: 24
```

{% hint style="warning" %}
Zamonaviy kompyuterlar uchun rang o'tkirligi va piksel to'yimliligi teng.
{% endhint %}
