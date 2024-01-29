# CSS 3D Transformalar

### CSS 3D transformlar <a href="#css-3d-transformlar" id="css-3d-transformlar"></a>

CSS shuningdek 3D transformlarni ham qo'llab-quvvatlaydi.

2D va 3D transformlar oʻrtasidagi farqni koʻrish uchun sichqonchani quyidagi elementlar ustiga olib boring:

![](<../../.gitbook/assets/image (217).png>)

Ushbu bo'limda quyidagi xususiyat haqida o'rganasiz:

* `transform`

### Brazuerning qo'llab-quvvatlashi <a href="#brazuer-qollab-quvvatlashi" id="brazuer-qollab-quvvatlashi"></a>

Jadvaldagi raqamlar xususiyatni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Xususiyat | Chrome | Edge | Firefox | Safari | Opera |
| --------- | ------ | ---- | ------- | ------ | ----- |
| transform | 36.0   | 10.0 | 16.0    | 9.0    | 23.0  |

### 3D Transformlar metodlari <a href="#id-3d-transformlar-metodlari" id="id-3d-transformlar-metodlari"></a>

CSSning `transform` xususiyati orqali quyidagi 3D transformatsiya metodlaridan foydalanishingiz mumkin:

* `rotateX()`
* `rotateY()`
* `rotateZ()`

### rotateX() metodi <a href="#rotatex-metodi" id="rotatex-metodi"></a>

![](<../../.gitbook/assets/image (631).png>)

`rotateX()` metodi elementni X o'qi atrofida berilgan daraja bo'ylab aylantiradi:

```
#myDiv {
  transform: rotateX(150deg);
}
```

### rotateY() metodi <a href="#rotatey-metodi" id="rotatey-metodi"></a>

![](<../../.gitbook/assets/image (261).png>)

`rotateY()` metodi elementni Y o'qi atrofida berilgan daraja bo'ylab aylantiradi:

```
#myDiv {
  transform: rotateY(150deg);
}
```

### rotateZ() metodi <a href="#rotatez-metodi" id="rotatez-metodi"></a>

`rotateZ()` metodi elementni Z o'qi atrofida berilgan daraja bo'ylab aylantiradi:

```
#myDiv {
  transform: rotateZ(90deg);
}
```

### CSSning Transform xususiyatlari <a href="#css-transform-xususiyatlari" id="css-transform-xususiyatlari"></a>

Quyidagi jadvalda barcha 3D transform xususiyatlari ko'rsatilgan:

| Xususiyat                                                                                 | Ta'rif                                                                           |
| ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| [transform](https://www.w3schools.com/cssref/css3\_pr\_transform.asp)                     | Elementga 2D yoki 3D oʻzgartirishni qoʻllaydi                                    |
| [transform-origin](https://www.w3schools.com/cssref/css3\_pr\_transform-origin.asp)       | Transform qilingan elementlardagi pozitsiyani o'zgartirishga imkon beradi        |
| [transform-style](https://www.w3schools.com/cssref/css3\_pr\_transform-style.asp)         | 3D bo'shliqda ichki joylashtirilgan elementlar qanday ko'rsatilishini belgilaydi |
| [perspective](https://www.w3schools.com/cssref/css3\_pr\_perspective.asp)                 | 3D elementlarning qanday ko'rilish perspektivasida bo'lishini belgilaydi         |
| [perspective-origin](https://www.w3schools.com/cssref/css3\_pr\_perspective-origin.asp)   | 3D elementlarning pastki holatini belgilaydi                                     |
| [backface-visibility](https://www.w3schools.com/cssref/css3\_pr\_backface-visibility.asp) | Element ekranga qaramaganda ko'rinib turishi yoki ko'rinmasligini belgilaydi     |

### CSSning 3D Transform Metodlari <a href="#css-3d-transform-metodlari" id="css-3d-transform-metodlari"></a>

| Funksiya                                                      |                                                                                            |
| ------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| <p>matrix3d<br>(<em>n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n</em>)</p> | 16 ta qiymatdan iborat 4x4 matritsadan foydalangan holda 3D transformatsiyasini belgilaydi |
| translate3d(_x,y,z_)                                          | 3D aylanishni belgilaydi                                                                   |
| translateX(_x_)                                               | Faqat X o'qi qiymatidan foydalangan holda 3D aylanishni belgilaydi                         |
| translateY(_y_)                                               | Faqat Y o'qi qiymatidan foydalangan holda 3D aylanishni belgilaydi                         |
| translateZ(_z_)                                               | Faqat Z o'qi qiymatidan foydalangan holda 3D aylanishni belgilaydi                         |
| scale3d(_x,y,z_)                                              | 3D masshtab belgilaydi                                                                     |
| scaleX(_x_)                                                   | X o'qi uchun qiymat berish orqali 3D masshtabni o'zgartirishni belgilaydi                  |
| scaleY(_y_)                                                   | Y o'qi uchun qiymat berish orqali 3D masshtabni o'zgartirishni belgilaydi                  |
| scaleZ(_z_)                                                   | Z o'qi uchun qiymat berish orqali 3D masshtabni o'zgartirishni belgilaydi                  |
| rotate3d(_x,y,z,angle_)                                       | 3D aylanishni belgilaydi                                                                   |
| rotateX(_angle_)                                              | X o'qi bo'ylab 3D aylanishni belgilaydi                                                    |
| rotateY(_angle_)                                              | Y o'qi bo'ylab 3D aylanishni belgilaydi                                                    |
| rotateZ(_angle_)                                              | Z o'qi bo'ylab 3D aylanishni belgilaydi                                                    |
| perspective(_n_)                                              | 3D oʻzgartirilgan element uchun perspektiv koʻrinishni belgilaydi                          |
