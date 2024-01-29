# Background color

CSS background xususiyatlari elementlarga orqafon effektini berish uchun ishlatiladi.

Ushbu bo'limda CSSning quyidagi background xususiyatlari haqida o'rganasiz:

<figure><img src="../../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

### CSS background-color <a href="#css-background-color" id="css-background-color"></a>

`background-color` xususiyati elementning orqafoniga rang beradi.

{% code title="Sahifaning orqafon rangi quyidagicha beriladi:" %}
```
body {
  background-color: lightblue;
}
```
{% endcode %}

CSS-da rang ko'pincha quyidagilar bilan belgilanadi:

* to'g'ri keladigan rang nomi - "qizil"ga o'xshagan.
* HEX qiymati - #ff0000 kabi.
* RGB qiymati - "rgb(255,0,0)".

Barcha rang nomlarini bilish uchun <mark style="color:green;">CSS rang qiymatlari</mark> sahifasiga qarang.

### Boshqa elementlar <a href="#boshqa-elementlar" id="boshqa-elementlar"></a>

HTML dagi har qanday elementning background rangini o'zgartira olasiz: background

{% code title="Quyida <h1>, <div> va <p> elementlarining background ranglari xar xil qilib o'zgartirilgan:" %}
```
h1 {
  background-color: green;
}

div {
  background-color: lightblue;
}

p {
  background-color: yellow;
}
```
{% endcode %}

### Opacity / Shaffoflik <a href="#shaffofligi" id="shaffofligi"></a>

`opacity` xususiyati elementning shaffofligini belgilaydi. U 0.0 dan 1.0 gacha bo'lgan qiymatlarni qabul qiladi. Qiymat qancha past bo'lsa shaffoflik shuncha yuqori bo'ladi.

<figure><img src="../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

```
div {
  background-color: green;
  opacity: 0.3;
}
```

{% hint style="warning" %}
**Note:** `opacity` xususiyati orqali elementni shaffof qilganda, element ichidagi barcha bola elementlar ham shaffoflikni meros qilib oladi. Bunda matnni to'liq shaffoq qilganda uning ichidagi matn ko'rinmay qoladi.
{% endhint %}

### RGBA yordamida shaffoflik <a href="#rgba-yordamida-shaffoflik" id="rgba-yordamida-shaffoflik"></a>

Yuqorida ko'rgan misolimizdagidek, ichki elementlar shaffoflikni meros qilib olishini xohlamasangiz, RGBA rang qiymatlaridan foydalaning. Quyidagi misol matnni emas faqat background rangining shaffofligini o'zgartiradi:

<figure><img src="../../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

Bizning <mark style="color:green;">CSS Ranglar</mark>i bo'limimizdan RGB rang qiymatlaridan qanday foydalanish kerakligini o'rgandingiz. Qo'shimchasiga RGB dagi rangning shaffofligini belgilovchi alpha kanalga ega RGBA ni ham ko'rib chiqqansiz.

RGBA rangining qiymatlari: rgba(red, green, blue, alpha) lar bilan belgilanadi. Alpha parametriga 0.0 (to'liq shaffof) bo'lgan va 1.0 (to'liq rang) oralig'idagi raqamlar kiritladi.

**Tip:** RGBA ranglari haqida CSS ranglari bo'limimizdan ko'proq ma'lumot olishingiz mumkin.

```
div {
  background: rgba(0, 128, 0, 0.3) /* Green background with 30% opacity */
}
```

## CSSning background color xususiyati

| Xususiyat                                                                     | Ta'rif                                |
| ----------------------------------------------------------------------------- | ------------------------------------- |
| [background-color](https://www.w3schools.com/cssref/pr\_background-color.asp) | Elementning orqafon rangini o'rnatadi |
