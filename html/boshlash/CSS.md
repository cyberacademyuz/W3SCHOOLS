---
description: >-
  CSS qisqartmasi, Cascading Style Sheets degan ma'noni anglatadi. CSS ko'p
  ishlarni tejaydi. U bilan bir vaqtning o'zida bir nechta veb-sahifalar
  tartibini boshqarishi mumkin.
---

# CSS

![](<../../.gitbook/assets/image (311).png>)

## <mark style="color:green;">CSS nima ?</mark>

CSS veb-sahifa dizaynini o'zgartirish uchun ishlatiladi.

CSS yordamida rangni, shriftni, matn o'lchamini, elementlar orasidagi masofani, elementlar qanday joylashishini, orqa fondagi rasmi yoki orqa fon ranglari qanday bo'lishi, turli qurilmalar va ekran o'lchamlari uchun qanday ko'rinishini boshqarishingiz mumkin.

{% hint style="warning" %}
**Maslahat: Kaskad** so'zi ota elementga berilgan stillar uning ichidagi barcha bola elementlariga ham tasir qilishini anglatadi. Agar siz bodyning matn rangini "ko'k" rang qilsangiz, sahifadagi barcha sarlavhalar, paragraflar va body ichidagi boshqa matn elementlari ham bir xil rangda bo'ladi (boshqa rang bermaguningizgacha)!
{% endhint %}

## <mark style="color:green;">CSSdan foydalanish</mark>

CSSni HTMLsahifaga 3 xil yo'l bilan qo'shiladi:

* Inline - HTML elementlari ichida <mark style="color:red;">`style`</mark> attributidan foydalanib
* Internal - <mark style="color:red;">`<head>`</mark> qismda <mark style="color:red;">`<style>`</mark> elementidan foydalanib
* External - Tashqi CSS faylni ulash uchun <mark style="color:red;">`<link>`</mark> elementidan foydalanib

CSSni ulashning keng tarqalgan usuli stillarni tashqi CSS fayllarda saqlashdir. Lekin biz bu qo'llanmada **inline** va **internal** usullaridan foydalanamiz, chunki uni ko'rsatib berish va o'zingiz ham sinab ko'rishingiz osonroq bo'ladi.

## <mark style="color:green;">Inline CSS</mark>

Inline CSS aynan bir elementga, uning o'ziga xos stil berish uchun ishlatiladi.

Inline CSS elementning <mark style="color:red;">`style`</mark> atributidan foydalanadi.

Quyidagi misol, <mark style="color:red;">`<h1>`</mark> elementidagi matn rangini ko'k va <mark style="color:red;">`<p>`</mark> elementidagi matn rangini qizil rangga o'zgartiradi:

```html
<h1 style="color:blue;">A Blue Heading</h1>

<p style="color:red;">A red paragraph.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_inline" %}

## <mark style="color:green;">Internal CSS</mark>

Internal CSS bitta HTML sahifaga xos stilni aniqlash uchun ishlatiladi.

Internal CSS HTML sahifaning <mark style="color:red;">`<head>`</mark> qismida <mark style="color:red;">`<style>`</mark> elementining ichida yoziladi.

Quyidagi misol ushbu sahifadagi barcha <mark style="color:red;">`<h1>`</mark> elementlarning matn rangini ko‘k rangga va barcha <mark style="color:red;">`<p>`</mark> elementlarning matn rangini esa qizil rangga o'zgartiradi. Bundan tashqari, sahifaning orqa fon ranggi "**powderblue**" rangi bilan ko'rsatiladi:

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {background-color: powderblue;}
h1   {color: blue;}
p    {color: red;}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_internal" %}

## <mark style="color:green;">External CSS</mark>

Bir qancha HTML sahifalarga stil berish uchun external CSSdan foydalaniladi.

Tashqi stillardan foydalanish uchun har bir HTML sahifning <mark style="color:red;">`<head>`</mark> qismiga havola qoʻshing:

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_external" %}

Tashqi stillar istalgan matn muharririda yozilishi mumkin. Stillar yoziladigan faylda hech qanday HTML kod bo'lmaydi va .css kengaytmasi bilan saqlanishi kerak.

"styles.css" fayli quyidagicha ko'rinadi:

```css
body {
  background-color: powderblue;
}
h1 {
  color: blue;
}
p {
  color: red;
}
```

{% hint style="warning" %}
**Maslahat:** Tashqi stillar yordamida bitta faylni o'zgartirish orqali butun veb-sayt ko'rinishini o'zgartirishingiz mumkin!
{% endhint %}

## <mark style="color:green;">CSS ranglar, shriftlar va o'lchamlar</mark>

Bu qismda tez-tez ishlatiladigan ba'zi CSS xususiyatlarini ko'rsatamiz. Keyinchalik esa ular haqida ko'proq bilib olasiz.

CSSning <mark style="color:red;">`color`</mark> xususiyati matn rangi qanday bo'lishi kerakligini belgilaydi.

CSSning <mark style="color:red;">`font-family`</mark> xususiyati matn shrifti qanday bo'lishi kerakligini belgilaydi.

CSSning <mark style="color:red;">`font-size`</mark> xususiyati matn o'lchami qanday bo'lishi kerakligini belgilaydi.

{% code title="CSSning color, font-family va font-size xususiyatlaridan foydalaning" %}
```html
<!DOCTYPE html>
<html>
<head>
<style>
h1 {
  color: blue;
  font-family: verdana;
  font-size: 300%;
}
p {
  color: red;
  font-family: courier;
  font-size: 160%;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_fonts" %}

## <mark style="color:green;">CSS Border</mark>

CSSning <mark style="color:red;">`border`</mark> xususiyati HTML elementining atrofidagi chegarasini ifodalaydi.

**Maslahat**: Deyarli barcha HTML elementlari uchun chegara belgilashingiz mumkin.

{% code title="CSSning border xususiyatidan foydalaning:" %}
```css
p {
  border: 2px solid powderblue;
}
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_borders" %}

## <mark style="color:green;">CSS Padding</mark>

CSSning <mark style="color:red;">`padding`</mark> xususiyati matn va uning chegara o'rtasidagi bo'sh joyni bildiradi.

{% code title="CSSning border va padding xususiyatidan foydalanish" %}
```css
p {
  border: 2px solid powderblue;
  padding: 30px;
}
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_padding" %}

## <mark style="color:green;">CSS Margin</mark>

CSSning `margin` xususiyati chegaraning tashqi tomonidagi bo'sh joyni bildiradi.

{% code title="CSSning border va margin xususiyatidan foydalaning" %}
```css
p {
  border: 2px solid powderblue;
  margin: 50px;
}
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_margin" %}

## <mark style="color:green;">Tashqi CSS faylni ulash</mark>

Tashqi stillarni, uning to'liq URL manzili yoki veb-sahifa fayliga nisbatan ichki joylashuv yo'li bilan ulash mumkin.

> Bu misolda CSS faylning to'liq URLini ulashdan foydalanilgan
>
> ```html
> <link rel="stylesheet" href="https://www.w3schools.com/html/styles.css">
> ```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_external_url" %}

> Ushbu misolda joriy veb-saytdagi html papkasida joylashgan CSS fayl ulangan:
>
> ```html
> <link rel="stylesheet" href="/html/styles.css">
> ```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_external_relative" %}

> Ushbu misolda joriy sahifa bilan bir xil papkada joylashgan CSS fayl ulangan:
>
> ```html
> <link rel="stylesheet" href="styles.css">
> ```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_css_external" %}

## <mark style="color:green;">Bo'lim xulosasi</mark>

* Inline stillar uchun HTMLda <mark style="color:red;">`style`</mark> attributidan foydalaniladi
* Internal CSS uchun HTMLda <mark style="color:red;">`<style>`</mark> elementidan foydalaniladi
* External CSS faylni ulash uchun HTMLda <mark style="color:red;">`<link>`</mark> elementidan foydalaniladi
* Mantnning rangini o'zgartirish uchun CSSning <mark style="color:red;">`color`</mark> xususiyatidan foydalaniladi
* Mantnning shriftini o'zgartirish uchun CSSning <mark style="color:red;">`font-family`</mark> xususiyatidan foydalaniladi
* Mantnning o'lchamini o'zgartirish uchun CSSning <mark style="color:red;">`font-size`</mark> xususiyatidan foydalaniladi
* Chegara berish uchun CSSning <mark style="color:red;">`border`</mark> xususiyatidan foydalaniladi
* Chegara ichida bo'sh joy berishda uchun CSSning <mark style="color:red;">`padding`</mark> xususiyatidan foydalaniladi
* Chegaraning tashqi qismida bo'sh joy berish uchun CSSning <mark style="color:red;">`margin`</mark> xususiyatidan foydalaniladi

## <mark style="color:green;">HTML stil teglari</mark>

| Teg      | Tavsif                                                  |
| -------- | ------------------------------------------------------- |
| \<style> | HTML sahifa uchun still ma'lumotlarini ifodalaydi       |
| \<link>  | Sahifa va tashqi resurs o'rtasini bog'lashni ifodalaydi |
