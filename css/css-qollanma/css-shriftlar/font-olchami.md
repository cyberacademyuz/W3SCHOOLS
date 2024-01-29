# Font o'lchami

### Font Size

`font-size` xususiyati matnning o'lchamini belgilaydi.

Matn o'lchamini boshqara olish web dizaynda muhim sanaladi. Biroq, paragraflarni sarlavhalarga o'xshatish yoki sarlavhalarni paragraflarga o'xshatish uchun shrift o'lchamini o'zgartirishdan foydalanmaslik kerak.

Har doim sarlavhalar uchun \<h1> - \<h6> va paragraflar uchun \<p> kabi to'g'ri HTML teglardan foydalaning**.**

font-size qiymati mutlaq (absolute) yoki nisbiy (relative) o'lcham bo'lsihi mumkin.

Mutlaq (absolute) o'lcham:

* Matnga maxsus o'lcham beradi
* Foydalanuvchiga barcha brauzerlarda matn hajmini o'zgartirishga ruxsat bermaydi (ba'zi sabablarga ko'ra yomon)
* Absalyut o'lcham qulay qachonki haqiqiy razmer aniq bo'lsa.

Nisbiy (relative) o'lcham:

* Atrofdagi elementlarga nisbatan o'lchamni o'rnatadi
* Foydalanuvchilarga matn o'lchamini o'zgartirishga ruxsat beradi

{% hint style="warning" %}
**Note:** Agar shrift o'lchamini bermasangiz, oddiy matn uchun, masalan paragraflar uchun standart o'lcham 16px (16px=1em) bo'ladi.
{% endhint %}

### Shrift o'lchamini pixelda berish <a href="#font-razmerini-pixel-larda-berish" id="font-razmerini-pixel-larda-berish"></a>

Agar shrift o'lchamini pixelda bersangiz, u matn o'lchamini to'liq boshqarish imkoniyatini beradi.

```
h1 {
  font-size: 40px;
}

h2 {
  font-size: 30px;
}

p {
  font-size: 14px;
}
```

**Maslahat:** Pikseldan foydalansangiz, butun sahifa o'lchamini o'zgartirish uchun zoom vositasidan foydalanishingiz mumkin.

### Shrift o'lchamini `em` orqali berish <a href="#font-razmerini-em-larda-berish" id="font-razmerini-em-larda-berish"></a>

Foydalanuvchilarga matn o'lchamini kattalashtirishga ruxsat berish uchun, ko'p dasturchilar piksel o'rniga **em**dan foydalanishadi.

**1em** joriy shrift o'lchamiga teng. Brauzerlarda standart matn o'lchami 16px. Shunday qilib, **1em**ning standart o'lchami **16px**.

**px**ni **em**ga hisoblash uchun quyidagi formuladan foydalaniladi: `px/16 = em`

```
h1 {
  font-size: 2.5em; /* 40px/16=2.5em */
}

h2 {
  font-size: 1.875em; /* 30px/16=1.875em */
}

p {
  font-size: 0.875em; /* 14px/16=0.875em */
}
```

Yuqoridagi misolda em bilan berilgan matn o'lchami oldingi misolimizda foydalanilgan pixellar o'lchamlariga teng. Lekin, em o'lchamlarini barcha brauzerlarda moslashtirish imkoniyati mavjud.

Afsuski, Internet Explorer-ning eski versiyalarida haligacha muammolar bor. Matn kattalashtirganda keragidan ko'p kattalshib ketadi va kichiklashtirilganda keragidan ko'p kichrayib ketadi.

### Foiz va Em kombinatsiyasidan foydalanish <a href="#foiz-va-em-kombinatsiyasidan-foydalanish" id="foiz-va-em-kombinatsiyasidan-foydalanish"></a>

`<body>` elementi uchun standart shriftni foizda belgilash barcha brauzerlarda bu muammoni hal qiladi.

```
body {
  font-size: 100%;
}

h1 {
  font-size: 2.5em;
}

h2 {
  font-size: 1.875em;
}

p {
  font-size: 0.875em;
}
```

Endi kodimiz yaxshi ishlaydi! Endi u barcha brauzerlarda bir xil o'lchamda bo'ladi va barchasida zoom qilish va o'lchamni o'zgartirish imkoniyatini beradi.

### Moshlashuvchan shrift o'lchami <a href="#adaptiv-font-razmeri" id="adaptiv-font-razmeri"></a>

Matn o'lchamini `vw` birligi bilan o'rnatish mumkin, bu "viewport width" degan ma'noni bildiradi.

Bu holatda matn o'lchami brauzer oynasiga qarab o'zgaradi.

<figure><img src="../../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

```
<h1 style="font-size:10vw">Hello World</h1>
```

{% hint style="warning" %}
Viewport - bu brauzer oynasining o'lchami hisoblanadi. 1vw = **viewport width**ning 1%i. Agar viewport 50 sm bo'lsa, 1vw 0,5 sm bo'ladi.
{% endhint %}
