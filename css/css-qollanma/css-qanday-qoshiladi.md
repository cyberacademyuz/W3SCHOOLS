---
description: >-
  Browser CSS kodini o'qiganida HTML hujjatni shu ma'lumotlarga muvofiq
  formatlaydi.
---

# CSS qanday qo'shiladi

## <mark style="color:green;">CSSni ulashning 3 xil usuli</mark> <a href="#css-ni-qoshishni-3-xil-usuli" id="css-ni-qoshishni-3-xil-usuli"></a>

CSS ni qo'shishni 3 xil usuli mavjud:

* External CSS (Tashqi CSS)
* Internal CSS (Ichki CSS)
* Inline CSS (Bir qatordagi CSS)

### External CSS (Tashqi CSS) <a href="#external-css-tashqi-css" id="external-css-tashqi-css"></a>

Tashqi stillar yordamida butun sayt dizaynini bitta faylning o'zida o'zgartira olasiz!

Har bir HTML sahifasining head qismida tashqi CSS fayl <mark style="color:red;">`<link>`</mark> tegi orqali ulangan bo'lishi kerak.

{% tabs %}
{% tab title="HTML" %}
Tashqi stillar <mark style="color:red;">`<head>`</mark> tegining ichida <mark style="color:red;">`<link>`</mark> elementi bilan HTML sahifaga ulanadi:

```html
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_howto_external" %}
{% endtab %}
{% endtabs %}

Tashqi CSS fayllar har qanday matn tahrirlovchi dastur orqali yozilishi va _**.css**_ kengaytmasi bilan saqlanishi mumkin.

Tashqi CSS fayllar o'zida hech qanday HTML teglarini saqlamaydi.

Quyida "**mystyle.css**" fayli qanday ko'rinishi keltirilgan:

{% tabs %}
{% tab title="CSS" %}
{% code title="mystyle.css" %}
```css
body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

{% hint style="danger" %}
**Eslatma**: Xususiyat qiymati (20) va qisqarma (px) o'rtasida bo'sh joy qo'shmang:

Xato (bo'sh joy): <mark style="color:red;">`margin-left: 20 px;`</mark>

To'g'ri (bo'sh joysiz): <mark style="color:red;">`margin-left: 20px;`</mark>
{% endhint %}

## <mark style="color:green;">Internal CSS (Ichki CSS)</mark> <a href="#internal-css-ichki-css" id="internal-css-ichki-css"></a>

Internal CSS (Ichki CSS) bitta HTML sahifasigagina bezak berish kerak bo'lganda ishlatiladi

Ichki CSS \<style> tegi ichida yoziladi va u ham head bo'limida joylashadi.

{% tabs %}
{% tab title="Ruby" %}
Ichki CSS <mark style="color:red;">`<style>`</mark> tegi ichida yoziladi va u ham <mark style="color:red;">`<head>`</mark> bo'limida joylashadi:

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_howto_internal" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Inline CSS (Bir qatordagi CSS)</mark> <a href="#inline-css-bir-qatordagi-css" id="inline-css-bir-qatordagi-css"></a>

Inline CSS bitta elementga unikal still berish uchun ishlatiladi.

Inline CSSdan foydalanish uchun kerakli elementga `style` attributini qo'shing. Style atributi har qanday CSS xususiyatini o'z ichiga olishi mumkin.

{% tabs %}
{% tab title="HTML" %}
Inline stillar tegishli elementning <mark style="color:red;">`style`</mark> atributida yoziladi:

```html
<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

</body>
</html>
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_howto_inline" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Maslahat:** Inline css stylesheetning ko'pgina afzalliklarini yo'qotadi. Ushbu usuldan kamdan kam holatda foydalaning.
{% endhint %}

## <mark style="color:green;">Bir nechta stylesheetlar</mark> <a href="#bir-nechta-ulanish-usullarini-birlashtirish" id="bir-nechta-ulanish-usullarini-birlashtirish"></a>

Agar bitta selektor (element) uchun ba'zi xususiyatlar turli stylesheetlarda berilgan bo'lsa, oxirgi o'qilgan stylesheetdagi qiymatdan foydalaniladi.

{% code title="Tasavvur qiling, quyidagi kod <h1> elementi uchun tashqi CSS faylida yozilgan:" %}
```css
h1 {
  color: navy;
}
```
{% endcode %}

{% code title="Keyin, tasavvur qiling quyidagi kod ichki CSS orqali <h1> uchun yozilgan:" %}
```css
h1 {
  color: orange;   
}
```
{% endcode %}

{% tabs %}
{% tab title="HTML" %}
Agarda Internal CSS, External CSS ulanishdian keyin yozilgan bo'lsa, unda <mark style="color:red;">`<h1>`</mark>"olovrang" bo'lib qoladi:

```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
<style>
h1 {
  color: orange;
}
</style>
</head>
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_howto_multiple" %}
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="HTML" %}
Agarda Internal CSS <mark style="color:red;">`<link>`</mark> tegidan oldin yozilgan bo'lsa unda External CSS ning qiymatlari hisobga olinib <mark style="color:red;">`<h1>`</mark> elementlari "ko'k rang" bo'lib qoladi:

```html
<head>
<style>
h1 {
  color: orange;
}
</style>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_howto_multiple2" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Kaskadlash tartibi</mark>

HTML element uchun bir nechta stil qiymatlari berilsa qaysi biri ishlatiladi ?

Barcha sahifadagi stillar quyidagi ketma-ketlikda ishlaydi:

1. Inline stil (HTML elementining ichidagi CSS qiymatlari)
2. External va Inline CSS (Head bo'limidagi)
3. Browser ni defolt holatidagi

Shunday qilib, inline still yuqori ustuvorlikka ega va tashqi va ichki stillarini hamda brauzerning standart sozlamalarini bekor qiladi.
