# CSS Height/Weight

CSS ning `height` va `width` xususiyatlari elementning balandligi va kengligini belgilash uchun ishlatiladi.

CSSning `max-width` xususiyati elementning maksimal kengligini belgilash uchun ishlatiladi.

<figure><img src="../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

### CSS da balandlik va kenglikni belgilash <a href="#css-da-balandlik-va-kenglikni-belgilash" id="css-da-balandlik-va-kenglikni-belgilash"></a>

CSSning `height` va `width` xususiyatlari elementning balandligi va kengligini belgilash uchun ishlatiladi.

`height` va `width` xususiyatlari o'zini ichiga padding, border va marginlarni olmaydi. U elementning padding, border va margin ichidagi maydonning balandligini va kengligini o'rnatadi.

### CSS height va width qiymatlari <a href="#css-height-va-width-qiymatlari" id="css-height-va-width-qiymatlari"></a>

height va width xususiyatlari quyidagi qiymatlarni o'ziga olishi mumkin:

* auto - default qiymat. Brauzer o'zi height va width qiymatlarini hisoblaydi
* length - height/width larni px, cm va hokazolar asosida belgilanadi
* % - O'z ichiga olgan blockning height/width qiymatlarini foizda belgilaydi
* initial - height/width ga default qiymat beradi
* inherit - height/width qiymatlari ota elementdan meros qilib olinadi.

### CSS height va widthga misollar <a href="#misol" id="misol"></a>

![](<../../.gitbook/assets/image (731).png>)

{% code title="<div> elementining balandligi va kenglini berish:" %}
```
div {
  height: 200px;
  width: 50%;
  background-color: powderblue;
}
```
{% endcode %}

![](<../../.gitbook/assets/image (482).png>)

{% code title="Boshqa bir <div> elementining balandligi va kenglini berish:" %}
```
div {
  height: 100px;
  width: 500px;
  background-color: powderblue;
}
```
{% endcode %}

**Note:** height va width xususiyatlari padding, border yoki marginlarni o'z ichiga olmayasligini yodda saqlang! Ular elementning padding, border va margin ichidagi maydonning balandligi/kengligini o'rnatadi!

### Max-width ni berish <a href="#max-width-ni-belgilash" id="max-width-ni-belgilash"></a>

`max-width` xususiyati elementning maksimal kengligini belgilash uchun ishlatiladi.

max-widthning uzunlik qiymatlari, px, cm va hokazolar orqali belgilanishi yoki o'z ichidagi blokning foizida belgilanishi, yoki umuman belgilamasligi ham mumkin. (Bu default. Maksimal kenglik yo'qligini bildiradi.)

Yuqoridagi `<div>` bilan bog'liq muammo shundaki, agar brauzer oynasi element kengligidan (500px) kichiklashganda yuzaga keladi. Keyin brauzer sahifaga gorizontal gorizontal scrollbar qo'shadi.

`max-width` dan foydalanish esa brauzerning kichik oynalar bilan ishlashini yaxshilaydi.

**Tip:** Brauzer oynasini 500px dan kichiklashtiring va ikkita divda qanday o'zgarish bo'lishini guvohi bo'ling!

![](<../../.gitbook/assets/image (184).png>)

**Note:** Agar biror bir sabab tufayli ikkala `width` hamda `max-width` xususiyatlaridan bir elementda foydalanishingizga to'g'ri kelsa va `width` qiymati `max-width` dan katta bo'lsa, `max-width` ishlatiladi va `width` qabul qilinmaydi.

{% code title="Bu <div> ning height qiymati 100px va max-width qiymati 500px:" %}
```
div {
  max-width: 500px;
  height: 100px;
  background-color: powderblue;
}
```
{% endcode %}

### O'zingiz sinab ko'ring - misollar

[<mark style="color:green;">Elementlarning balandligi va kengligini o'rnatish</mark>](https://www.w3schools.com/css/tryit.asp?filename=trycss\_dim\_height)\
Ushbu misol turli elementlarning balandligi va kengligini qanday o'rnatishni ko'rsatadi.

<mark style="color:green;">Rasmning balandligi va kengligini foiz yordamida berish</mark>\
Ushbu misol rasmning balandligi va kengligini foiz qiymatidan foydalanib o'rnatishni ko'rsatadi.

<mark style="color:green;">Elementning minimal kengligi va maksimal kengligini berish</mark>\
Ushbu misol px qiymatidan foydalanib elementning minimal kengligi va maksimal kengligini qanday o'rnatishni ko'rsatadi.

<mark style="color:green;">Elementning minimal balandligi va maksimal balandligini berish</mark>\
Ushbu misol px qiymatidan foydalanib elementning minimal balandligi va maksimal balandligini qanday o'rnatishni ko'rsatadi.

### CSSning barcha o'lchash xususiyatlari <a href="#barcha-css-olchash-xususiyatlari" id="barcha-css-olchash-xususiyatlari"></a>

| Xususiyat                                                              | Ta'rif                                       |
| ---------------------------------------------------------------------- | -------------------------------------------- |
| [height](https://www.w3schools.com/cssref/pr\_dim\_height.asp)         | Elementning balandligini belgilaydi          |
| [max-height](https://www.w3schools.com/cssref/pr\_dim\_max-height.asp) | Elementning maksimal balandliigni belgilaydi |
| [max-width](https://www.w3schools.com/cssref/pr\_dim\_max-width.asp)   | Elementning maksimal kengligini belgilaydi   |
| [min-height](https://www.w3schools.com/cssref/pr\_dim\_min-height.asp) | Elementning minimal balandligini belgilaydi  |
| [min-width](https://www.w3schools.com/cssref/pr\_dim\_min-width.asp)   | Elementning minimal kengligini belgilaydi    |
| [width](https://www.w3schools.com/cssref/pr\_dim\_width.asp)           | Elementning kengligini belgilaydi            |
