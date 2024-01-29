# CSS Flex konteyneri

### Ota element (konteyner)

Oldingi bo'limda aytib o'tganimizdek, mana bu uchta moslashuvchan **element**ga ega moslashuvchan **konteyner** (ko'k maydon):

<figure><img src="../../../.gitbook/assets/image (371).png" alt=""><figcaption></figcaption></figure>

Moslashuvchan konteyner `display`quyidagi xususiyatni o'rnatish orqali moslashuvchan bo'ladi:

Moslashuvchan konteyner `displey` xususiyatining qiymatiga `flex` berish orqali moslashuvchan bo'ladi:

```
.flex-container {
  display: flex;
}
```

Flex konteyner xususiyatlari:

* <mark style="color:red;">`flex-direction`</mark>
* <mark style="color:red;">`flex-wrap`</mark>
* <mark style="color:red;">`flex-flow`</mark>
* <mark style="color:red;">`justify-content`</mark>
* <mark style="color:red;">`align-items`</mark>
* <mark style="color:red;">`align-content`</mark>

### flex-direction xususiyati

`flex-direction` xususiyati konteyner flex elementlarni qaysi yo'nalishda joylashtirishni belgilaydi.

<figure><img src="../../../.gitbook/assets/image (746).png" alt=""><figcaption></figcaption></figure>

{% code title="column qiymati flex elementlarni vertikal ravishda (yuqoridan pastga) joylashtiradi:" %}
```
.flex-container {
  display: flex;
  flex-direction: column;
}
```
{% endcode %}

{% code title="column-reverse qiymati flex elementlarni vertikal ravishda (lekin pastdan yuqoriga) joylashtiradi:" %}
```
.flex-container {
  display: flex;
  flex-direction: column-reverse;
}
```
{% endcode %}

{% code title="row qiymati flex elementlarni vertikal ravishda (chapdan o'ngga) joylashtiradi:" %}
```
.flex-container {
  display: flex;
  flex-direction: row;
}
```
{% endcode %}

{% code title="row qiymati flex elementlarni vertikal ravishda (o'ngdan chapga) joylashtiradi:" %}
```
.flex-container {
  display: flex;
  flex-direction: row-reverse;
}
```
{% endcode %}

### flex-wrap xususiyati

`flex-wrap` xsusiyati flex elementlarning wrap bo'lishi yoki wrap bo'lmasligini belgilaydi.

Quyidagi misollarda `flex-wrap`xususiyatni yaxshiroq ko'rsatib berish uchun 12 ta moslashuvchan element mavjud.

<figure><img src="../../../.gitbook/assets/image (737).png" alt=""><figcaption></figcaption></figure>

{% code title="warp qiymati, kerak bo'lganida, flex elementlarini wrap bo'lishini bildiradi:" %}
```
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
```
{% endcode %}

{% code title="nowrap qiymati, kerak bo'lganida, flex elementlarini wrap qilinmasligini bildiradi:" %}
```
.flex-container {
  display: flex;
  flex-wrap: nowrap;
}
```
{% endcode %}

{% code title="warp-reverse qiymati, kerak bo'lganida, flex elementlarini teskari tartibda wrap bo'lishini bildiradi:" %}
```
.flex-container {
  display: flex;
  flex-wrap: wrap-reverse;
}
```
{% endcode %}

### flex-flow xususiyati

&#x20;xususiyai va xususiyatlarni o'rnatish uchun stenok xususiyatdir.

flex-flow xususiyati `flex-direction` va `flex-wrap` xususiyatlarini berish uchun qisqartma xususiyatdir.

{% code title="flex-flow xususiyati flex-direction va flex-wrap xususiyatlarini berish uchun qisqartma xususiyatdir." %}
```
.flex-container {
  display: flex;
  flex-flow: row wrap;
}
```
{% endcode %}

### flex-content xususiyati

`justify-content` xususiyati flex elementlarni joylashtirish uchun ishlatiladi:

<figure><img src="../../../.gitbook/assets/image (422).png" alt=""><figcaption></figcaption></figure>

{% code title="center qiymati flex elementlarni konteynerning o'rtasiga joylashtiradi:" %}
```
.flex-container {
  display: flex;
  justify-content: center;
}
```
{% endcode %}

{% code title="flex-start qiymati flex elementlarni konteynerning boshlanish qismiga joylashtiradi (standart):" %}
```
.flex-container {
  display: flex;
  justify-content: flex-start;
}
```
{% endcode %}

{% code title="flex-end qiymati flex elementlarni konteynerning ohiriga joylashtiradi:" %}
```
.flex-container {
  display: flex;
  justify-content: flex-end;
}
```
{% endcode %}

{% code title="space-around qiymati moslashuvchan elementlarni, ularning qatoridan avval, qatorining o'rtasiga va ohiriga bo'sh joy qo'ygan holda ko'rsatadi." %}
```
.flex-container {
  display: flex;
  justify-content: space-around;
}
```
{% endcode %}

{% code title="space-between qiymati flex elementlarni ketma ketliklar orasini bo'sh joy bilan ko'rsatadi:" %}
```
.flex-container {
  display: flex;
  justify-content: space-between;
}
```
{% endcode %}

### align-items xususiyati

`align-items` xususiyati flex elementlarni joylashtirish uchun ishlatiladi.

<figure><img src="../../../.gitbook/assets/image (378).png" alt=""><figcaption></figcaption></figure>

Ushbu misollar orqali `align-items` xususiyatini yaxshiroq ko'rsatib berish uchun 200px balandlikdagi konteynerdan foydalanamiz.

{% code title="center qiymati flex elementlarni turgan joyidan tepadan pastga nisbatan konteynerning o'rtasiga joylashtiradi:" %}
```
.flex-container {
  display: flex;
  height: 200px;
  align-items: center;
}
```
{% endcode %}

{% code title="flex-start qiymati flex elementlarni konteynerning tepasiga joylashtiradi:" %}
```
.flex-container {
  display: flex;
  height: 200px;
  align-items: flex-start;
}
```
{% endcode %}

{% code title="flex-end qiymati flex elementlarni turgan joyidan tepadan pastga nisbatan konteynerning pastki qismiga joylashtiradi:" %}
```
.flex-container {
  display: flex;
  height: 200px;
  align-items: flex-end;
}
```
{% endcode %}

{% code title="stretch qiymati konteynerdagi bo'sh joyni to'ldirish uchun fkex elementlarni cho'zadi. (standart qiymat):" %}
```
.flex-container {
  display: flex;
  height: 200px;
  align-items: stretch;
}
```
{% endcode %}

{% code title="baseline qiymati flex elementlarni ularning markaziy chizig'iga tekislab joylashtiradi." %}
```
.flex-container {
  display: flex;
  height: 200px;
  align-items: baseline;
}
```
{% endcode %}

**Eslatma:** misolda elementlar matnning markaziy chizig'iga mos kelishini ko'rsatish uchun turli shrift o'lchamidan foydalaniladi:

<figure><img src="../../../.gitbook/assets/image (520).png" alt=""><figcaption></figcaption></figure>

### Align-content xususiyati

`align-content` xususiyati flex qatorlarni tekislash uchun ishlatiladi.

<figure><img src="../../../.gitbook/assets/image (428).png" alt=""><figcaption></figcaption></figure>

Ushbu misollar orqali `align-content` xususiyatini yaxshiroq ko'rsatib berish uchun `flex-wrap` xususiyati `wrap` qilingan **600px**-li baland konteynerdan foydalanamiz.

{% code title="space-between qiymati moslashuvchan qatorlarni ularning orasida bir xil o'lchamga ega bo'lgam bo'sh joy bilan ko'rsatadi:" %}
```
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: space-between;
}
```
{% endcode %}

{% code title="space-around qiymati moslashuvchan qatorlarni, ulardagi elementdan avval, element o'rtasiga va ohiriga bo'sh joy qo'ygan holda ko'rsatadi." %}
```
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: space-around;
}
```
{% endcode %}

{% code title="Stretch qiymati qolgan joyni egallab olish uchun moslashuvchan qatorlarni cho'zadi (standart qiymat)" %}
```
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: stretch;
}
```
{% endcode %}

{% code title="center qiymati moslashuvchan qatorlarni konteynerning o'rtasidan ko'rsatadi:" %}
```
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: center;
}
```
{% endcode %}

{% code title="flex-start qiymati moslashuvchan qatorlarni konteynerning eng boshida ko'rsatadi:" %}
```
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: flex-start;
}
```
{% endcode %}

{% code title="flex-end qiymati moslashuvchan qatorlarni konteynerning ohiridan ko'rsatadi:" %}
```
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: flex-end;
}
```
{% endcode %}

### Eng o'rtaga joylashtirish

Quyidagi misolda cssdagi keng tarqalgan muammosini hal qilamiz ya'ni: elementni sahifaning o'rtasiga joylashtirish.

<figure><img src="../../../.gitbook/assets/image (437).png" alt=""><figcaption></figcaption></figure>

**Yechim:**`justify-content` va `align-items`xususiyatlarning qiymatini `center` qiling shunda moslashuvchan element konteynerning eng o'rtasiga keladi:

```
.flex-container {
  display: flex;
  height: 300px;
  justify-content: center;
  align-items: center;
}
```

### CSS Flexbox konteyner xususiyatlari

Quyidagi jadvalda flexbox konteynerning barcha xususiyatlari keltirilgan:

| Xususiyat                                                                                                                                                         | Ta'rif                                                                                                                                  |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| [align-content](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_align-content.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Modifies the behavior of the flex-wrap property. It is similar to align-items, but instead of aligning flex items, it aligns flex lines |
| [align-items](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_align-items.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)         | Vertically aligns the flex items when the items do not use all available space on the cross-axis                                        |
| [display](https://www-w3schools-com.translate.goog/cssref/pr\_class\_display.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                | Specifies the type of box used for an HTML element                                                                                      |
| [flex-direction](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_flex-direction.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Specifies the direction of the flexible items inside a flex container                                                                   |
| [flex-flow](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_flex-flow.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | A shorthand property for flex-direction and flex-wrap                                                                                   |
| [flex-wrap](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_flex-wrap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | Specifies whether the flex items should wrap or not, if there is not enough room for them on one flex line                              |
| [justify-content](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_justify-content.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Horizontally aligns the flex items when the items do not use all available space on the main-axis                                       |
