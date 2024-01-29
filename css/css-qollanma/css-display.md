# CSS Display

`display` xususiyati layoutlarni boshqarish uchun CSS da o'ta muhim hisoblanadi.

### Display xususiyati <a href="#display-xususiyati" id="display-xususiyati"></a>

`display` xususiyati elementning qanday ko'rsatilishi kerakligini belgilaydi

Har bir HTML elementning qaysi elementligiga ko'ra standard `display` qiymati bo'ladi. Bu qiymatlar asosan **block** va **inline**lar hisoblanadi.

<figure><img src="../../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

### Block elementlar <a href="#block-elementlar" id="block-elementlar"></a>

Block darajasidagi elementlar har doim yangi qatordan boshlanadi va barcha bo'sh joyni egallaydi (qo'lidan kelganicha chap va o'ng tomonga cho'ziladi).

<figure><img src="../../.gitbook/assets/image (537).png" alt=""><figcaption></figcaption></figure>

Block elementlarga misollar:

* \<div>
* \<h1> - \<h6>
* \<p>
* \<form>
* \<header>
* \<footer>
* \<section>

### Inline elementlar <a href="#inline-elementlar" id="inline-elementlar"></a>

Inline elementlar yangi qatordan boshlanmaydi va barcha bo'sh joyni olmasdan o'ziga kerakli joyni egallaydi.

Bu ![](<../../.gitbook/assets/image (489).png>)paragraf

Inline elementlarga misollar:

* \<span>
* \<a>
* \<img>

### Display: none; <a href="#display-none" id="display-none"></a>

`display: none;` odatda JavaScript yordamida elementlarni o'chirmasdan yoki qayta yaratmasdan turib yashirish va ko'rsatish uchun ishlatiladi. Buni qanday qilishni bilmoqchi bo'lsangiz, ushbu sahifadagi ohirgi misolimizni ko'rib chiqing.

`<script>` elementi standart `display:none;` dan foydalanadi

### Standart display qiymatining ustidan yozish <a href="#standart-display-qiymatini-ustidan-yozish" id="standart-display-qiymatini-ustidan-yozish"></a>

Aytib o'tilganidek, har bir elementning o'ziga xos `display` qiymati bo'ladi. Biroq, ularni ustidan boshqa qiymatlarni ham bera olasiz.

**Inline** elementni blok elementiga o'zgartirish yoki aksini qilish orqali web sahifangizni yanada chiroyli qilishda  foyda berishi mumkin va shu bilan birga veb-standartlarga ham rioya qiling.

Buning eng ko'p uchraydigan misoli `<li>` elementlarini gorizontal holatga keltirilish:

```
li {
  display: inline;
}
```

{% hint style="warning" %}
**Note:** Elementga `display` xususiyatini berish faqatgina elementning qanday ko'rsatilishini o'zgartiradi, uning qanday element ekanligini emas. `display: block;` berilgan inline element ichida boshqa block elementlarga ruhsat berilmaydi.
{% endhint %}

Quyidagi misolda `<span>` elementi blok holatiga o'zgartirilgan:

```
span {
  display: block;
}
```

Quyidagi misolda `<a>` elementlari **blok** holatiga o'zgartirilgan:

```
a {
  display: block;
}
```

### Elementni berkitish - display: none; yoki visibility:hidden; ? <a href="#elementni-berkitish-uchun-display-none-qilish-kerakmi-yoki-visibilityhidden" id="elementni-berkitish-uchun-display-none-qilish-kerakmi-yoki-visibilityhidden"></a>

<figure><img src="../../.gitbook/assets/image (445).png" alt=""><figcaption></figcaption></figure>

Elementni yashirish uchun `displey` xususiyatining qiymatini `none` qilish orqali amalga oshirilishi mumkin. Element yashiriladi va sahifada element yo'qdek ko'rsatiladi:

```
h1.hidden {
  display: none;
}
```

`visibility:hidden;` ham elementni yashiradi.

Ammo, element bo'sh qo'lgan joyni egallab turaveradi. Element yashiriladi, lekin baribir joylashuvga ta'sir qiladi:

```
h1.hidden {
  visibility: hidden;
}
```

Ko'proq misollar

<mark style="color:green;">`displey none;`</mark> <mark style="color:green;"></mark><mark style="color:green;">va</mark> <mark style="color:green;"></mark><mark style="color:green;">`visibility: hidden;`</mark> <mark style="color:green;"></mark><mark style="color:green;">o'rtasidagi farqlar</mark>\
Bu misolda `display: none;` va `visibility: hidden;` ko'rsatib berilgan

<mark style="color:green;">Kontentni ko'rsatish uchun JavaScript bilan birgalikda CSS-dan foydalanish</mark>\
Ushbu misolda elementni bosish orqali kontentni ko'rsatish uchun CSS va JavaScript-dan qanday foydalanish ko'rsatib berilgan.

### CSSning display/visibility xususiyatlari <a href="#css-displayvisibility-xususiyatlari" id="css-displayvisibility-xususiyatlari"></a>

| Xususiyat                                                                | Ta'rif                                              |
| ------------------------------------------------------------------------ | --------------------------------------------------- |
| [display](https://www.w3schools.com/cssref/pr\_class\_display.asp)       | Element qanday tasvirlanishi kerakligini belgilaydi |
| [visibility](https://www.w3schools.com/cssref/pr\_class\_visibility.asp) | Element ko'rinishi kerakmi yo'qmi belgilaydi        |
