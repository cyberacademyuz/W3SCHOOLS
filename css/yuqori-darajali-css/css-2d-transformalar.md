# CSS 2D Transformalar

### CSS 2D Transformlar <a href="#css-2d-transformlar" id="css-2d-transformlar"></a>

CSSning transformlari elementlarni surish, aylantirish, masshtablash va qiyshaytirish imkonini beradi.

2D transformlarni koʻrish uchun sichqonchani quyidagi element ustiga olib boring:

![](<../../.gitbook/assets/image (647).png>)

Ushbu bo'limda CSSning quyidagi xususiyati haqida bilib olasiz:

* `transform`

### Brauzerning qo'llab quvvatlashi <a href="#brauzer-qollab-quvvatlashi" id="brauzer-qollab-quvvatlashi"></a>

Jadvaldagi raqamlar xususiyatni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Xususiyat | Chrome | Edge | Firefox | Safari | Opera |
| --------- | ------ | ---- | ------- | ------ | ----- |
| transform | 36.0   | 10.0 | 16.0    | 9.0    | 23.0  |

### CSS 2D Transform metodlari <a href="#css-2d-transform-metodlari" id="css-2d-transform-metodlari"></a>

CSSning `transform` xususiyati orqali quyidagi 2D transformatsiya metodlaridan foydalanishingiz mumkin:

* `translate()`
* `rotate()`
* `scaleX()`
* `scaleY()`
* `scale()`
* `skewX()`
* `skewY()`
* `skew()`
* `matrix()`

{% hint style="warning" %}
**Maslahat**: Keyingi bo'limda 3D transformatsiyalar haqida bilib olasiz.
{% endhint %}

### translate() metodi <a href="#translate-metodi" id="translate-metodi"></a>

![](<../../.gitbook/assets/image (579).png>)

`Translate()` metodi elementni joriy holatidan (X o'qi va Y o'qi uchun berilgan parametrlarga muvofiq) ko'chiradi.

Quyidagi misol `<div>` elementini joriy holatidan 50px o'ngga va 100px pastga suradi:

```
div {
  transform: translate(50px, 100px);
}
```

### rotate() metodi <a href="#rotate-metodi" id="rotate-metodi"></a>

![](<../../.gitbook/assets/image (219).png>)

`rotate()` metodi elementni ma'lum darajaga qarab soat yo'nalishi bo'yicha yoki teskari yo'nalishda aylantiradi.

Quyidagi misol `<div>` elementini soat yo'nalishi bo'yicha 20 gradusga aylantiradi:

```
div {
  transform: rotate(20deg);
}
```

Manfiy qiymatlardan foydalanish elementni soat yo'nalishining teskari tartibida aylantiradi.

Quyidagi misol `<div>` elementini soatga teskari yo'nalishda 20 gradus aylantiradi:

```
div {
  transform: rotate(-20deg);
}
```

### scale() metodi <a href="#scale-metodi" id="scale-metodi"></a>

![](<../../.gitbook/assets/image (534).png>)

`scale()` metodi element o'lchamini ko'paytiradi yoki kamaytiradi (width va height uchun berilgan parametrlarga muvofiq).

Quyidagi misolda `<div>` elementini asl kengligidan ikki baravar va asl balandligidan uch baravar katta qilinadi:

```
div {
  transform: scale(2, 3);
}
```

Quyidagi misolda `<div>` elementining asl kengligini va balandligini yarmiga qisqartiriladi:

```
div {
  transform: scale(0.5, 0.5);
}
```

### scaleX() metodi <a href="#scalex-metodi" id="scalex-metodi"></a>

`scaleX()` metodi elementning kengligini ko'paytiradi yoki kamaytiradi.

Quyidagi misol `<div>` elementining asl kengligidan ikki baravar katta qiladi:

```
 div {
  transform: scaleX(2);
}
```

Quyidagi misol `<div>` elementini asl kengligining yarmiga qisqartiradi:

```
div {
  transform: scaleX(0.5);
}
```

### scaleY() metod <a href="#scaley-metod" id="scaley-metod"></a>

`scaleY()` metodi element balandligini ko'paytiradi yoki kamaytiradi.

Quyidagi misol `<div>` elementini asl balandligidan uch baravar katta qiladi:

```
div {
  transform: scaleY(3);
}
```

Quyidagi misol `<div>` elementini asl balandligining yarmiga qisqartiradi:

```
 div {
  transform: scaleY(0.5);
}
```

### skewX() metodi <a href="#skewx-metodi" id="skewx-metodi"></a>

`skewX()` metodi elementni X o'qi bo'ylab berilgan burchak bo'yicha buradi.

Quyidagi misol `<div>` elementini X o'qi bo'ylab 20 gradusga buradi:

```
div {
  transform: skewX(20deg);
}
```

### skewY() metodi <a href="#skewy-metodi" id="skewy-metodi"></a>

`skewY()` metodi elementni Y o'qi bo'ylab berilgan burchak bo'yicha buradi.

Quyidagi misol `<div>` elementini Y o'qi bo'ylab 20 gradusga buradi:

```
div {
  transform: skewY(20deg);
}
```

### skew() metodi <a href="#skew-metodi" id="skew-metodi"></a>

`Skew()` metodi elementni X va Y o'qi bo'ylab berilgan burchaklar bo'yicha buradi.

Quyidagi misol `<div>` elementini X o'qi bo'ylab 20 gradusga va Y o'qi bo'ylab 10 gradusga buradi:

```
div {
  transform: skew(20deg, 10deg);
}
```

Agar ikkinchi parametr ko'rsatilmagan bo'lsa, u nol qiymatga ega bo'ladi. Quyidagi misol `<div>` elementini X o'qi bo'ylab 20 gradusga buradi:

```
div {
  transform: skew(20deg);
}
```

### matrix() metodi <a href="#matrix-metodi" id="matrix-metodi"></a>

![](../../.gitbook/assets/transform\_rotate.gif)

`Matrix()` metodi barcha 2D transform metodlarini bittaga birlashtiradi.

`Matrix()` metodi matematik funktsiyalarni o'z ichiga olgan oltita parametrni qabul qiladi, bu  elementlarni aylantirish, masshtablash, surish va burish imkonini beradi.

**Parametrlar:** matrix(scaleX(), skewY(), skewX(), scaleY(), translateX(), translateY())

```
div {
  transform: matrix(1, -0.3, 0, 1, 0, 0);
}
```

### CSSning transform xususiyatlari <a href="#css-transform-xususiyatlari" id="css-transform-xususiyatlari"></a>

Quyidagi jadvalda barcha 2D transform xususiyatlari ko'rsatilgan:

| Xususiyat                                                                           | Ta'rif                                                                    |
| ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| [transform](https://www.w3schools.com/cssref/css3\_pr\_transform.asp)               | Elementga 2D yoki 3D transformni qoʻllaydi                                |
| [transform-origin](https://www.w3schools.com/cssref/css3\_pr\_transform-origin.asp) | Transform qilingan elementlardagi pozitsiyani o'zgartirishga imkon beradi |

### CSSning 2D transform Methods <a href="#css-2d-transform-methods" id="css-2d-transform-methods"></a>

| Funksiya                | Ta'rif                                                                                |
| ----------------------- | ------------------------------------------------------------------------------------- |
| matrix(_n,n,n,n,n,n_)   | Oltita qiymatdan iborat matritsadan foydalangan holda 2D transformatsiyani belgilaydi |
| translate(_x,y_)        | Elementni X va Y o'qi bo'ylab harakatlantirib, 2D aylabnishini belgilaydi             |
| translateX(_n_)         | Elementni X o'qi bo'ylab harakatlantirib, 2D aylanishini belgilaydi                   |
| translateY(_n_)         | Elementni Y o'qi bo'ylab harakatlantirib, 2D aylanishini belgilaydi                   |
| scale(_x,y_)            | Elementlarning kengligi va balandligini o'zgartirib, 2D masshtabni belgilaydi         |
| scaleX(_n_)             | Elementning kengligini o'zgartirib, 2D masshtabni belgilaydi                          |
| scaleY(_n_)             | Element balandligini o'zgartirib, 2D masshtabni belgilaydi                            |
| rotate(_angle_)         | 2D aylanishni belgilaydi, burchak parametrda ko'rsatilgan                             |
| skew(_x-angle,y-angle_) | X va Y o'qi bo'ylab 2D egilish transformatsiyasini belgilaydi                         |
| skewX(_angle_)          | X o'qi bo'ylab 2D egilish transformatsiyasini belgilaydi                              |
| skewY(_angle_)          | Y o'qi bo'ylab 2D egilish transformatsiyasini belgilaydi                              |
