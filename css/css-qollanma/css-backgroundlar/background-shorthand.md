# Background shorthand

## <mark style="color:green;">CSS Background Shorthand (qisqartirmasi)</mark> <a href="#css-background-shorthand-qisqartirmasi" id="css-background-shorthand-qisqartirmasi"></a>

Kodni qisqartirish uchun, barcha background xususiyatlarini bitta qatorga yozish imkoniyati mavjud. U qisqartirma (shorthand) xususiyat deb ataladi.

Mana bunday qilib yozgandan ko'ra:

{% tabs %}
{% tab title="CSS" %}
```css
body {
  background-color: #ffffff;
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```
{% endtab %}
{% endtabs %}

Siz qisqagina <mark style="color:red;">`background`</mark> xususiyatidan foydalanishingiz mumkin:

{% tabs %}
{% tab title="CSS" %}
Bitta qatorni o'zida barcha qiymatlarni berish uchun <mark style="color:red;">`background`</mark> xususiyatidan foydalanish:

```css
body {
  background: #ffffff url("img_tree.png") no-repeat right top;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background_shorthand" %}
{% endtab %}
{% endtabs %}

Ushbu xususiyatdan foydalanishda quyidagi ketma-ketlikka amal qiling:

* <mark style="color:red;">`background-color`</mark>
* <mark style="color:red;">`background-image`</mark>
* <mark style="color:red;">`background-repeat`</mark>
* <mark style="color:red;">`background-attachment`</mark>
* <mark style="color:red;">`background-position`</mark>

Boshqa qiymatlar shu tartibda yozilsa, xususiyat qiymatlaridan birini yozmaslik muhim emas. E'tibor bering, biz yuqoridagi misollarda <mark style="color:red;">`background-attachment`</mark> xususiyatidan foydalanmadik, chunki u qiymatga ega emas.

### <mark style="color:green;">Barcha CSS Background xususiyatlari</mark> <a href="#barcha-css-background-xususiyatlari" id="barcha-css-background-xususiyatlari"></a>

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
