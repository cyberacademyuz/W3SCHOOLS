# CSS object-fit

CSSning `object-fit` xususiyati `<img>` yoki `<video>`ni o'zining konteyneriga mos kelishi uchun o'lchamini qanday o'zgartirish kerakligini belgilash uchun ishlatiladi.

### CSS object-fit xususiyati

CSSning `object-fit` xususiyati `<img>` yoki `<video>`ni o'zining konteyneriga mos kelishi uchun o'lchamini qanday o'zgartirish kerakligini belgilash uchun ishlatiladi.

Bu xususiyat kontentga iloji boricha cho'zilish va ko'proq joy egalalsh kabi turli yo'llar bilan konteynerni to'ldirishni aytadi.

Parijda olingan ushbu rasmga qarang. Rasmning kengligi 400px va balandligi 300px:

![Parij](https://www.w3schools.com/css/paris.jpg)

Ammo, rasmning kegligini uning yarm kengligi teng (200px) qilib, balandligini esa bir xil (300 piksel) bo'lishi uchun still bersak, u quyidagicha ko'rinadi:

![](<../../.gitbook/assets/image (360).png>)

```
img {
  width: 200px;
  height: 300px;
}
```

Rasmni 200x300 pikselli konteynerga sig'dirish uchun siqib ko'rsatilayotganining guvohi bo'lamiz (uning tomonlar nisbati buziladi).

Bu yerda `object-fit` xususiyati yodamga keladi. `object-fit` xususiyati quyidagi qiymatlarni qabul qiladi:

* `fill`- Standart qiymat. Rasmning o'lchami berilgan o'lchamni to'ldirish uchun o'zgartiriladi. Kerak bo'lganda, rasm cho'ziladi yoki siqiladi
* `contain`- Rasm o'zining tomonlar nisbatini saqlab qoladi, lekin berilgan o'lchamga mos keladigan darajada o'zgartiriladi
* `cover`- Rasm o'zining tomonlar nisbatini saqlab qoladi va berilgan o'lchamni to'ldiradi. Rasm mos keladigan tarzda kesiladi
* `none`- Rasm o'lchami o'zgartirilmaydi
* `scale-down`- Rasm `none` yoki `contain`ning eng kichik versiyasigacha kichraytirilgan

### object-fit: cover; foydalanish

Agar  `object-fit: cover;` dan foydalansak, rasm o'zining nisbatlarini saqlab qoladi va berilgan o'lchamni to'ldiradi. Rasm mos keladigan qilib kesiladi:

![](<../../.gitbook/assets/image (278).png>)

```
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
}
```

### object-fit: contain; dan foydalanish

Agar `object-fit: contain;` dan foydalansak, rasm o'zining nisbatlarini saqlab qoladi, lekin berilgan o'lchamga mos tarzda o'zgartiriladi:

![](<../../.gitbook/assets/image (607).png>)

```
img {
  width: 200px;
  height: 300px;
  object-fit: contain;
}
```

### object-fit: fill; dan foydalanish

Agar `object-fit: fill;` dan foydalansak rasm berilgan o'lchamni to'ldirishi uchun uning o'lchami o'zgartiriladi. Cho'zilshi kerak bo'sa mos keladigan o'lchamda cho'ziladi yoki siqiladi:

![](<../../.gitbook/assets/image (235).png>)

```
img {
  width: 200px;
  height: 300px;
  object-fit: fill;
}
```

### object-fit: none;dan foydalanish

Agar `object-fit: none;` dan foydalansak rasm o'lchami o'zgarmaydi:

![](<../../.gitbook/assets/image (280).png>)

```
img {
  width: 200px;
  height: 300px;
  object-fit: none;
}
```

### object-fit: scale-down; dan foydalanish

Agar `object-fit: scale-down;` dan foydalansak, rasm `none` yoki `contain`ning eng kichik versiyasigacha qisqartiriladi.

![](<../../.gitbook/assets/image (283).png>)

```
img {
  width: 200px;
  height: 300px;
  object-fit: scale-down;
}
```

### Yana bir misol

Bu yerda bizda ikkita rasm bor va biz ularni brauzer oynasining 50% kengligini va balandligini 100% egallashini xohlaymiz.

Quyidagi misolda biz `object-fit`dan foydalanmaymiz, shuning sababli brauzer oynasining o'lchamini o'zgartirganimizda rasmning nisbati buziladi:

![Norvegiya](https://www.w3schools.com/css/rock600x400.jpg) ![Parij](https://www.w3schools.com/css/paris.jpg)

Keyingi misolda `object-fit: cover;`dan foydalanamiz, shuning sababli brauzer oynasining o'lchamini o'zgartirganimizda, rasmning nisbati buzilmaydi:

![Norvegiya](https://www.w3schools.com/css/rock600x400.jpg) ![Parij](https://www.w3schools.com/css/paris.jpg)

### &#x20;CSSning object-fit xususiyatiga ko'proq misollar

Quyidagi misolda `object-fit` xususiyatida foydalanish mumkin bo'lgan barcha qiymatlar ko'rsatilgan:

```
.fill {object-fit: fill;}
.contain {object-fit: contain;}
.cover {object-fit: cover;}
.scale-down {object-fit: scale-down;}
.none {object-fit: none;}
```

### CSSning `object-*` xususiyatlari

Quyidagi jadvalda CSSning `object-*` xususiyatlari keltirilgan:

| Xususiyat                                                                                                                                                         | Ta'rif                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| [object-fit](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_object-fit.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)           | Specifies how an \<img> or \<video> should be resized to fit its container                                 |
| [object-position](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_object-position.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Specifies how an \<img> or \<video> should be positioned with x/y coordinates inside its "own content box" |
