---
description: >-
  CSS Selektori nomi bilan ham aytib turibdi, siz bezak bermoqchi bo'lgan HTML
  elementlarini belgilaydi.
---

# CSS Selektorlar

## CSS Selektorlari <a href="#css-selektorlari-2" id="css-selektorlari-2"></a>

CSS Selektorlar siz still bermoqchi bo'lgan HTML elementlarini "topish" (yoki tanlash) uchun ishlatiladi.

Biz CSS selektorlarini beshta kategoriyaga bo'la olamiz:

* Oddiy selektorlar (elementlarni teg nomi, id-si va classiga qarab topadi)
* [Kombinator](css-kombinatorlar.md) selektorlar (elementlarni ular orasidagi ma'lum munosabatiga qarab tanlaydi)
* [Pseudo-class selektorlar](css-pseudo-class.md) (elementlarni ma'lum bir holatga qarab tanlaydi)
* [Pseudo-elementlar selektorlari](css-pseudo-element.md) (elementni ma'lum bir qismini tanlaydi va still beradi)
* [Attribut selektorlari](css-atrr-selektorlari.md) (elementlarni attribut nomiga yoki attribut qiymatiga qarab belgilaydi)

Ushbu sahifada asosan boshlang'ich CSS selektorlari tushuntirilgan.

## CSS element selektori <a href="#css-element-selektori" id="css-element-selektori"></a>

Element selektori HTML elementlarini nomiga qarab tanlaydi.message = "hello world"

{% tabs %}
{% tab title="CSS" %}
Ushbu misolda barcha <mark style="color:red;">`<p>`</mark> elementlari o'rtada turadi va qizil rangda bo'ladi:

```css
p {
  text-align: center;
  color: red;
}
```
{% endtab %}
{% endtabs %}

## <mark style="color:green;">CSS id selektori</mark> <a href="#css-id-selektori" id="css-id-selektori"></a>

<mark style="color:red;">`id`</mark> selektori elementni tanlash uchun HTML elementining <mark style="color:red;">`id`</mark> atributidan foydalanadi.

Elementning id-si sahifada bitta bo'ladi, shuning uchun <mark style="color:red;">`id`</mark> selektori bitta unikal elementni tanlash uchun ishlatiladi!

id-ga ega elementni tanlash uchun xesh (#) belgisini va undan keyin elementning id nomini yozing.

{% tabs %}
{% tab title="CSS" %}
Ushbu misoldagi css kod `id="para1"` attributiga ega elementga qo'llaniladi:

```css
#para1 {
  text-align: center;
  color: red;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_syntax_id" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Note:** id hech qachon raqam bilan boshlanmaydi!
{% endhint %}

## <mark style="color:green;">CSS class selektori</mark> <a href="#css-klass-selektori" id="css-klass-selektori"></a>

Class selektori HTML elemntlarini <mark style="color:red;">`class`</mark> attributiga qarab tanlaydi.

Class attributiga ega elementlarni tanlash uchun nuqta (.) belgisini va undan keyin class nomini yozing.

{% tabs %}
{% tab title="CSS" %}
Ushbu misoldagi css kod <mark style="color:red;">`class="center"`</mark> ga ega barcha HTML elementlarining rangizni qizil qiladi va uni markazga to'g'irlaydi:

```css
.center {
  text-align: center;
  color: red;
}
```

[https://www.w3schools.com/css/tryit.asp?filename=trycss\_syntax\_class](https://www.w3schools.com/css/tryit.asp?filename=trycss\_syntax\_class)
{% endtab %}
{% endtabs %}

Bundan tashqari, classni faqat maxsus HTML elementlariga ta'sir qilishi kerakligini belgilashingiz mumkin.

{% tabs %}
{% tab title="CSS" %}
Ushbu misolda faqatgina class="center" ga ega

elementlari tanlangan va stil qiymatlari qizil va joylashuvi o'rtaga o'zgartirilgan:

```css
p.center {
  text-align: center;
  color: red;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_syntax_element_class" %}
{% endtab %}
{% endtabs %}

HTML elementlari bittadan ortiq classlarni o'z ichiga olishi mumkin.

{% tabs %}
{% tab title="CSS" %}
Ushbu misolda <mark style="color:red;">`<p>`</mark> elementi bir vaqtni o'zida <mark style="color:red;">`class="center"`</mark> va <mark style="color:red;">`class="large"`</mark> larni jamlamoqda:

```html
<p class="center large">This paragraph refers to two classes.</p>
```
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Note:** Class nomi raqam bilan boshlanmaydi!
{% endhint %}

### <mark style="color:green;">CSS Universal selektor</mark> <a href="#css-universal-selektori" id="css-universal-selektori"></a>

Universal selektor sahifadagi barcha HTML elementlarini belgilaydi.

{% tabs %}
{% tab title="CSS" %}
CSS qoidasiga ko'ra quyidagi misolda barcha HTML elementlari tanlanadi:

```css
* {
  text-align: center;
  color: blue;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_syntax_element_class2" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">CSS Guruhlash selektorlari</mark> <a href="#css-guruhlash-selektorlari" id="css-guruhlash-selektorlari"></a>

Guruhlash selektori bir xil css kodlari bilan berilgan barcha HTML elementlarini tanlaydi.

Quyidagi CSS kodga e'tiboringizni qarating (**h1**, **h2** va **p** elementlariga bir xil still qiymatlari berilgan):

```css
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```

Bunday uzun kodni guruhlash selektorlari yordamida qisqartirishingiz mumkin.

Guruh selektorlaridan foydalanish uchun har bir element nomidan keyin vergul orqali ajratish kerak.

{% tabs %}
{% tab title="CSS" %}
```css
h1, h2, p {
  text-align: center;
  color: red;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_grouping" %}
{% endtab %}
{% endtabs %}

### Barcha oddiy CSS selektorlari <a href="#barcha-oddiy-css-selektorlari" id="barcha-oddiy-css-selektorlari"></a>

| Selektor              | Misol      | Ta'rif                                                                                                                        |
| --------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------- |
| _#id_                 | #firstname | <mark style="color:red;">`id="firstname"`</mark> attributiga ega elementni tanlaydi                                           |
| _.class_              | .intro     | class="intro" ga ega elementlarni tanlaydi                                                                                    |
| _element.class_       | p.intro    | Faqatgina <mark style="color:red;">`class="intro"`</mark> ga ega <mark style="color:red;">`<p>`</mark> elementlarini tanlaydi |
| \*                    | \*         | Barcha elementlarni tanlaydi                                                                                                  |
| _element_             | p          | Barcha <mark style="color:red;">`<p>`</mark> elementlarini tanlaydi                                                           |
| _element,element,..._ | div, p     | Barcha <mark style="color:red;">`<div>`</mark> va <mark style="color:red;">`<p>`</mark> elementlarini tanlaydi                |
