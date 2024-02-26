# CSS Width/Height

CSS ning <mark style="color:red;">`width`</mark> va <mark style="color:red;">`height`</mark> xususiyatlari elementning balandligi va kengligini belgilash uchun ishlatiladi.

CSSning <mark style="color:red;">`max-width`</mark> xususiyati elementning maksimal kengligini belgilash uchun ishlatiladi.

<figure><img src="../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_height_width_intro" %}

## <mark style="color:green;">CSS da balandlik va kenglikni belgilash</mark> <a href="#css-da-balandlik-va-kenglikni-belgilash" id="css-da-balandlik-va-kenglikni-belgilash"></a>

CSSning <mark style="color:red;">`height`</mark> va <mark style="color:red;">`width`</mark> xususiyatlari elementning balandligi va kengligini belgilash uchun ishlatiladi.

<mark style="color:red;">`height`</mark> va <mark style="color:red;">`width`</mark> xususiyatlari o'zini ichiga <mark style="color:red;">`padding`</mark>, <mark style="color:red;">`border`</mark> va <mark style="color:red;">`margin`</mark>larni olmaydi. U elementning padding, border va margin ichidagi maydonning balandligini va kengligini o'rnatadi.

## <mark style="color:green;">Height va width qiymatlari</mark> <a href="#css-height-va-width-qiymatlari" id="css-height-va-width-qiymatlari"></a>

height va width xususiyatlari quyidagi qiymatlarni o'ziga olishi mumkin:

* <mark style="color:red;">`auto`</mark> - default qiymat. Brauzer o'zi height va width qiymatlarini hisoblaydi
* <mark style="color:red;">length</mark> - height/width larni px, cm va hokazolar asosida belgilanadi
* <mark style="color:red;">`%`</mark> - O'z ichiga olgan blockning height/width qiymatlarini foizda belgilaydi
* <mark style="color:red;">`initial`</mark> - height/width ga default qiymat beradi
* <mark style="color:red;">`inherit`</mark> - height/width qiymatlari ota elementdan meros qilib olinadi.

### <mark style="color:green;">CSS height va widthga misollar</mark> <a href="#misol" id="misol"></a>

![](<../../.gitbook/assets/image (731).png>)

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`<div>`</mark> elementining balandligi va kenglini berish:

```css
div {
  height: 200px;
  width: 50%;
  background-color: powderblue;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_dim_height_width2" %}
{% endtab %}
{% endtabs %}

![](<../../.gitbook/assets/image (482).png>)

{% tabs %}
{% tab title="CSS" %}
Boshqa bir <mark style="color:red;">`<div>`</mark> elementining balandligi va kenglini berish:

```css
div {
  height: 100px;
  width: 500px;
  background-color: powderblue;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_dim_height_width" %}
{% endtab %}
{% endtabs %}

**Note:** `height` va `width` xususiyatlari padding, border yoki marginlarni o'z ichiga olmayasligini yodda saqlang! Ular elementning padding, border va margin ichidagi maydonning balandligi/kengligini o'rnatadi!

## <mark style="color:green;">Max-widthni berish</mark> <a href="#max-width-ni-belgilash" id="max-width-ni-belgilash"></a>

<mark style="color:red;">`max-width`</mark> xususiyati elementning maksimal kengligini belgilash uchun ishlatiladi.

max-widthning uzunlik qiymatlari, px, cm va hokazolar orqali belgilanishi yoki o'z ichidagi blokning foizida belgilanishi, yoki umuman belgilamasligi ham mumkin. (Bu default. Maksimal kenglik yo'qligini bildiradi.)

Yuqoridagi <mark style="color:red;">`<div>`</mark> bilan bog'liq muammo shundaki, agar brauzer oynasi element kengligidan (500px) kichiklashganda yuzaga keladi. Keyin brauzer sahifaga gorizontal gorizontal scrollbar qo'shadi.

<mark style="color:red;">`max-width`</mark> dan foydalanish esa brauzerning kichik oynalar bilan ishlashini yaxshilaydi.

**Tip:** Brauzer oynasini 500px dan kichiklashtiring va ikkita divda qanday o'zgarish bo'lishini guvohi bo'ling!

![](<../../.gitbook/assets/image (184).png>)

**Note:** Agar biror bir sabab tufayli ikkala <mark style="color:red;">`width`</mark> hamda <mark style="color:red;">`max-width`</mark> xususiyatlaridan bir elementda foydalanishingizga to'g'ri kelsa va `width` qiymati <mark style="color:red;">`max-width`</mark> dan katta bo'lsa, <mark style="color:red;">`max-width`</mark> ishlatiladi va <mark style="color:red;">`width`</mark> qabul qilinmaydi.

{% tabs %}
{% tab title="CSS" %}
Bu <mark style="color:red;">`<div>`</mark> ning height qiymati 100px va max-width qiymati 500px:

```css
div {
  max-width: 500px;
  height: 100px;
  background-color: powderblue;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_dim_max_width" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">O'zingiz sinab ko'ring - misollar</mark>

[<mark style="color:green;">Elementlarning balandligi va kengligini o'rnatish</mark>](https://www.w3schools.com/css/tryit.asp?filename=trycss\_dim\_height)\
Ushbu misol turli elementlarning balandligi va kengligini qanday o'rnatishni ko'rsatadi.

<mark style="color:green;">Rasmning balandligi va kengligini foiz yordamida berish</mark>\
Ushbu misol rasmning balandligi va kengligini foiz qiymatidan foydalanib o'rnatishni ko'rsatadi.

<mark style="color:green;">Elementning minimal kengligi va maksimal kengligini berish</mark>\
Ushbu misol px qiymatidan foydalanib elementning minimal kengligi va maksimal kengligini qanday o'rnatishni ko'rsatadi.

<mark style="color:green;">Elementning minimal balandligi va maksimal balandligini berish</mark>\
Ushbu misol px qiymatidan foydalanib elementning minimal balandligi va maksimal balandligini qanday o'rnatishni ko'rsatadi.

## <mark style="color:green;">CSSning barcha o'lchash xususiyatlari</mark> <a href="#barcha-css-olchash-xususiyatlari" id="barcha-css-olchash-xususiyatlari"></a>

| Xususiyat                                                              | Ta'rif                                       |
| ---------------------------------------------------------------------- | -------------------------------------------- |
| [height](https://www.w3schools.com/cssref/pr\_dim\_height.asp)         | Elementning balandligini belgilaydi          |
| [max-height](https://www.w3schools.com/cssref/pr\_dim\_max-height.asp) | Elementning maksimal balandliigni belgilaydi |
| [max-width](https://www.w3schools.com/cssref/pr\_dim\_max-width.asp)   | Elementning maksimal kengligini belgilaydi   |
| [min-height](https://www.w3schools.com/cssref/pr\_dim\_min-height.asp) | Elementning minimal balandligini belgilaydi  |
| [min-width](https://www.w3schools.com/cssref/pr\_dim\_min-width.asp)   | Elementning minimal kengligini belgilaydi    |
| [width](https://www.w3schools.com/cssref/pr\_dim\_width.asp)           | Elementning kengligini belgilaydi            |
