# Background shorthand

### CSS Background Shorthand (qisqartirmasi) <a href="#css-background-shorthand-qisqartirmasi" id="css-background-shorthand-qisqartirmasi"></a>

Kodni qisqartirish uchun, barcha background xususiyatlarini bitta qatorga yozish imkoniyati mavjud. U qisqartirma (shorthand) xususiyat deb ataladi.

Mana bunday qilib yozgandan ko'ra:

```
body {
  background-color: #ffffff;
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```

Siz qisqagina `background`  xususiyatidan foydalanishingiz mumkin:

{% code title="Bitta qatorni o'zida barcha qiymatlarni berish uchun background xususiyatidan foydalanish:" %}
```
body {
  background: #ffffff url("img_tree.png") no-repeat right top;
}
```
{% endcode %}

Ushbu xususiyatdan foydalanishda quyidagi ketma-ketlikka amal qiling:

* `background-color`
* `background-image`
* `background-repeat`
* `background-attachment`
* `background-position`

Boshqa qiymatlar shu tartibda yozilsa, xususiyat qiymatlaridan birini yozmaslik muhim emas. E'tibor bering, biz yuqoridagi misollarda `background-attachment` xususiyatidan foydalanmadik, chunki u qiymatga ega emas.

### Barcha CSS Background xususiyatlari <a href="#barcha-css-background-xususiyatlari" id="barcha-css-background-xususiyatlari"></a>

| Xususiyat             | Ta'rif                                                                   |
| --------------------- | ------------------------------------------------------------------------ |
| background            | Barcha background xususiyatlarini bir qator kodda yozish imkonini beradi |
| background-attachment | Background dagi rasmni qotib turadimi yoki skroll bo'ladimi belgilaydi   |
| background-clip       | Fonning bo'yash maydonini belgilaydi                                     |
| background-color      | Fonning rangini belgilaydi                                               |
| background-image      | Fonga qanday rasm qo'yilishini belgilaydi                                |
| background-origin     | fondagi rasmlar qayerda joylashishi kerakligini belgilaydi               |
| background-position   | Fondagi rasm qayerdan boshlab joylashishi kerakligini belgilaydi         |
| background-repeat     | Fondagi rasm qancha marotaba qayta-qayta chiqarilishini ta'minlaydi      |
| background-size       | Fondagi rasmlarni razmerini belgilab beradi.                             |
