---
description: >-
  CSS qisqartmasi Cascading Style Sheets degan ma'noni anglatadi. CSS ko'p
  ishlarni tejaydi. U bilan bir vaqtning o'zida bir nechta veb-sahifalar
  tartibini boshqarishi mumkin.
---

# CSS

![](<../../.gitbook/assets/image (311).png>)

## CSS nima ?

CSS veb-sahifa dizaynini o'zgartirish uchun ishlatiladi.

CSS yordamida rangni, shriftni, matn o'lchamini, elementlar orasidagi masofani, elementlar qanday joylashishini, orqa fondagi rasmi yoki orqa fon ranglari qanday bo'lishi, turli qurilmalar va ekran o'lchamlari uchun qanday ko'rinishini boshqarishingiz mumkin.

{% hint style="warning" %}
**Maslahat: Kaskad** so'zi ota elementga berilgan stillar uning ichidagi barcha bola elementlariga ham tasir qilishini anglatadi. Agar siz bodyning matn rangini "ko'k" rang qilsangiz, sahifadagi barcha sarlavhalar, paragraflar va body ichidagi boshqa matn elementlari ham bir xil rangda bo'ladi (boshqa rang bermaguningizgacha)!
{% endhint %}

## CSSdan foydalanish

CSSni HTMLsahifaga 3 xil yo'l bilan qo'shiladi:

* Inline - HTML elementlari ichida style attributidan foydalanib
* Internal - `<head>` qismda \<style> elementidan foydalanib
* External - Tashqi CSS faylni ulash uchun `<link>` elementidan foydalanib

CSSni ulashning keng tarqalgan usuli stillarni tashqi CSS fayllarda saqlashdir. Lekin biz bu qo'llanmada **inline** va **internal** usullaridan foydalanamiz, chunki uni ko'rsatib berish va o'zingiz ham sinab ko'rishingiz osonroq bo'ladi.

## Inline CSS

Inline CSS aynan bir elementga, uning o'ziga xos stil berish uchun ishlatiladi.

Inline CSS elementning `style` atributidan foydalanadi.

Quyidagi misol,\<h1> elementning matn rangini ko'k va \<p> elementning matn rangini qizil rangga o'zgartiradi:

```
<h1 style="color:blue;">A Blue Heading</h1>

<p style="color:red;">A red paragraph.</p>
```

## Internal CSS

Internal CSS bitta HTML sahifaga xos stilni aniqlash uchun ishlatiladi.

Internal CSS HTML sahifaning \<head> qismida \<style> elementining ichida yoziladi.

Quyidagi misol ushbu sahifadagi barcha  \<h1> elementlarning matn rangini ko‘k rangga va barcha \<p> elementlarning matn rangini esa qizil rangga o'zgartiradi. Bundan tashqari, sahifaning orqa fon ranggi "**powderblue**" rangi bilan ko'rsatiladi:

```
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

## External CSS

Bir qancha HTML sahifalarga stil berish uchun external CSSdan foydalaniladi.

Tashqi stillardan foydalanish uchun har bir HTML sahifning `<head>` qismiga havola qoʻshing:

```
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

Tashqi stillar istalgan matn muharririda yozilishi mumkin. Stillar yoziladigan faylda hech qanday HTML kod bo'lmaydi va .css kengaytmasi bilan saqlanishi kerak.

"styles.css" fayli quyidagicha ko'rinadi:

```
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

## CSS ranglar, shriftlar va o'lchamlar

Bu qismda tez-tez ishlatiladigan ba'zi CSS xususiyatlarini ko'rsatamiz. Keyinchalik esa ular haqida ko'proq bilib olasiz.

CSSning `color` xususiyati matn rangi qanday bo'lishi kerakligini belgilaydi.

CSSning `font-family` xususiyati matn shrifti qanday bo'lishi kerakligini  belgilaydi.

CSSning `font-size` xususiyati matn o'lchami qanday bo'lishi kerakligini  belgilaydi.

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

## CSS Border

CSSning `border` xususiyati HTML elementining atrofidagi chegarasini ifodalaydi.

**Maslahat**: Deyarli barcha HTML elementlari uchun chegara belgilashingiz mumkin.

{% code title="CSSning border xususiyatidan foydalaning:" %}
```
p {
  border: 2px solid powderblue;
}
```
{% endcode %}

## CSS Padding

CSSning `padding` xususiyati matn va uning chegara o'rtasidagi bo'sh joyni bildiradi.

{% code title="CSSning border va padding xususiyatidan foydalanish" %}
```
p {
  border: 2px solid powderblue;
  padding: 30px;
}
```
{% endcode %}

## CSS Margin

CSSning `margin` xususiyati chegaraning tashqi tomonidagi bo'sh joyni bildiradi.

{% code title="CSSning border va margin xususiyatidan foydalaning" %}
```
p {
  border: 2px solid powderblue;
  margin: 50px;
}
```
{% endcode %}

## Tashqi CSSni ulash

Tashqi stillarni, uning to'liq URL manzili yoki veb-sahifa fayliga nisbatan ichki joylashuv yo'li bilan ulash mumkin.

### Misollar

{% code title="Bu misolda CSS faylning to'liq URLini ulashdan foydalanilgan" %}
```
<link rel="stylesheet" href="https://www.w3schools.com/html/styles.css">
```
{% endcode %}

{% code title="Ushbu misolda joriy veb-saytdagi html papkasida joylashgan CSS fayl ulangan: " %}
```
<link rel="stylesheet" href="/html/styles.css">
```
{% endcode %}

{% code title="Ushbu misolda joriy sahifa bilan bir xil papkada joylashgan CSS fayl ulangan:" %}
```
<link rel="stylesheet" href="styles.css">a
```
{% endcode %}

## Bo'lim xulosasi

* Inline stillar uchun HTMLda `style` attributidan foydalaniladi
* Internal CSS uchun HTMLda `<style>` elementidan foydalaniladi
* External CSS faylni ulash uchun HTMLda `<link>` elementidan foydalaniladi
* Mantnning rangini o'zgartirish uchun CSSning `color` xususiyatidan foydalaniladi
* Mantnning shriftini o'zgartirish uchun CSSning `font-family` xususiyatidan foydalaniladi
* Mantnning o'lchamini o'zgartirish uchun CSSning `font-size` xususiyatidan foydalaniladi
* Chegara berish uchun CSSning `border` xususiyatidan foydalaniladi
* Chegara ichida bo'sh joy berishda uchun CSSning `padding` xususiyatidan foydalaniladi
* Chegaraning tashqi qismida bo'sh joy berish uchun CSSning `margin` xususiyatidan foydalaniladi

## HTML stil teglari

| Teg      | Tavsif                                                  |
| -------- | ------------------------------------------------------- |
| \<style> | HTML sahifa uchun still ma'lumotlarini ifodalaydi       |
| \<link>  | Sahifa va tashqi resurs o'rtasini bog'lashni ifodalaydi |



