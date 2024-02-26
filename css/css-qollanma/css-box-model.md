---
description: Barcha HTML elementlarini qutilar (boxes) deb hisoblash mumkin.
---

# CSS Box Model

## <mark style="color:green;">CSS Box modeli</mark> <a href="#css-box-modeli-2" id="css-box-modeli-2"></a>

CSS-da dizayn va layout haqida gapirilganda "box modeli" atamasi ishlatiladi.

CSSning box modeli har bir HTML elementni o'rab turuvchi muhim quti hisoblanadi. U: marginlar, borderlar, paddinglar va  kontentdan iborat. Quyidagi rasm box model qanday ekanligini ko'rsatmoqda.

<figure><img src="../../.gitbook/assets/image (519).png" alt=""><figcaption></figcaption></figure>

Har bir qismni tushuntirish:

* **Content** - Boxning kontenti ya'ni rasm va yozuv aks etadigan joy
* **Padding** - Kontent atrofidagi bo'sh joy. Padding ko'rinmaydi
* **Border** - Padding va kontent atrofini o'rab turuvchi chegara
* **Margin** - Chegara atrofidagi bo'sh joy. Margin ko'rinmaydi.

Box modeli bizga elementlar atrofida chegara qo'shish va elementlar orasidagi bo'sh joyni aniqlash imkonini beradi.

{% tabs %}
{% tab title="CSS" %}
Box modelni tushuntiruvchi kod:

```css
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_boxmodel" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Elementning kengligi, balandligi</mark> <a href="#elementning-kengligi-balandligi" id="elementning-kengligi-balandligi"></a>

Elementni kengligini va balandligini barcha brauzerlarda bir xilda to'g'ri qo'yish uchun, biz avval box modeli qanday ishlashini bilishimiz kerak.

{% hint style="warning" %}
**Muhim**: CSS orqali elementning width va height xususiyatlarini berganingizda, shunchaki kontent maydonining kengligi va balandligini belgilaysiz. Elementning to'liq o'lchamini hisoblash uchun padding, margin va borderlarni ham qo'shishingiz kerak.
{% endhint %}

{% tabs %}
{% tab title="CSS" %}
Ushbu <mark style="color:red;">`<div>`</mark> elementining umumiy kengligi 350px bo'ladi:

```css
div {
  width: 320px;
  padding: 10px;
  border: 5px solid gray;
  margin: 0;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_boxmodel_width" %}
{% endtab %}
{% endtabs %}

Quyidagicha hisoblangan:

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Elementning umumiy kengligi quyidagicha hisoblanishi kerak:

Elementning umumiy kengligi = width + chap tomondagi padding + o'ng tomondagi padding + chap tomondagi border + o'ng tomondagi border + chap tomondagi margin + o'ng tomondagi margin

Elementning umumiy balandligi quyidagicha hisoblanishi kerak:

Umumiy element balandligi = height + tepa qismdagi padding + pastki qismdagi padding + tepa qismdagi border + pastki qismdagi border + tepa qismdagi margin + pastki qismdagi margin.
