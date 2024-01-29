# CSS object-position

CSSning `object-position` xususiyati `<img>` yoki `<video>` ning konteyner ichida qanday joylashishi kerakligini belgilash uchun ishlatiladi.

### Rasm

Parijda tushurilgan 400x300 pikselli quyidagi rasmga qarang:

![Parij](https://www.w3schools.com/css/paris.jpg)

Endi, tomonlar nisbatini saqlash va berilgan o'lchamni to'ldirish uchun `object-fit: cover;` dan foydalanamiz. Biroq, rasm quyidagi kabi mos keladigan tarzda kesiladi:

![](<../../.gitbook/assets/image (834).png>)

```
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
}
```

### object-position xususiyatidan foydalanish

Deylik, rasmning ko'rinib turgan qismi biz xohlagandek joylashtirilmagan. Rasmni o'zimiz xoxlagandek joylashtirish uchun `object-position` xususiyatidan foydalanamiz.

Bu yerda rasmdagi katta eski bino o'rtada ko'rsatilishi uchun `object-position` xususiyatidan foydalanamiz:

![](<../../.gitbook/assets/image (226).png>)

```
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
  object-position: 80% 100%;
}
```

Bu yerda biz rasmdagi mashhur Eyfel minorasi o'ratada ko'rinishi uchun`object-position` xususiyatidan foydalanamiz:

![](<../../.gitbook/assets/image (533).png>)

```
img {
  width: 200px;
  height: 300px;
  object-fit: cover;
  object-position: 15% 100%;
}
```

### CSSning `object-*` xususiyatlari

Quyidagi jadvalda CSSning `object-*` xususiyatlari keltirilgan:

| Xususiyat                                                                                                                                                          | Ta'rif                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| [object-fit](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_object-fit.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)            | Specifies how an \<img> or \<video> should be resized to fit its container                                 |
| [object-posititon](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_object-position.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Specifies how an \<img> or \<video> should be positioned with x/y coordinates inside its "own content box" |
