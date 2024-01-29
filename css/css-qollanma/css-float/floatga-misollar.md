# Floatga misollar

Ushbu sahifada **float**ga tegishli ko'plab misollar keltirilgan.

### Qutilar gridi / Bir xil kenglikdagi qutilar <a href="#grid-of-boxes-equal-width-boxes" id="grid-of-boxes-equal-width-boxes"></a>

<figure><img src="../../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

`float` xususiyati orqali kontent qutilarini yonma-yon float qilish (suzdirish) oson:

#### Misol <a href="#misol" id="misol"></a>

```
* {
  box-sizing: border-box;
}

.box {
  float: left;
  width: 33.33%; /* three boxes (use 25% for four, and 50% for two, etc) */
  padding: 50px; /* if you want space between the images */
}
```

{% hint style="warning" %}
**Box-sizing nima ?**

Uchta yonma-yon suzuvchi qutlarni osongina yaratishingiz mumkin. Biroq, har bir qutining kengligini (masalan, padding yoki  borderlari) kattalashtiradigan biror narsa qo'shsangiz, quti buziladi. Box-sizing xususiyati bizga padding va border xususiyatini qutining umumiy kengligiga (va balandligiga) kiritish imkonini beradi, padding quti ichida qolishiga va uning buzilmasligiga ishonch hosil qildiradi.

\
CSS Box o'lchamlari bo'limida Box sizing xususiyati haqida ko'proq o'qishingiz mumkin.
{% endhint %}

### Yonma-yon rasmlar <a href="#yonma-yon-rasmlar" id="yonma-yon-rasmlar"></a>

Qutilar gridi rasmlarni yonma-yon ko'rsatish uchun ham ishlatilishi mumkin:

```
.img-container {
  float: left;
  width: 33.33%; /* three containers (use 25% for four, and 50% for two, etc) */
  padding: 5px; /* if you want space between the images */
}
```

### Bir xil balandlikdagi qutilar <a href="#equal-height-boxes" id="equal-height-boxes"></a>

Oldingi misolda qutilarni qanday qilib bir xil kenglikda yonma-yon float qilishni o'rgandingiz. Biroq, bir xil balandlikdagi float qutilarni yaratish oson emas. Bu muammoni hal qilish uchun, quyidagi misoldagi kabi fixed balandlik qiymatini berish kerak bo'ladi

```
.box {
  height: 500px;
}
```

Biroq, bu holat unchalik moslashuvchan emas. Agar har bir kontentni bir xil o'lchamga keltira olsangiz unda moslashuvchanlik bo'yicha muammo bo'lmaydi. Lekin har doim ham kontent bir xil bo'lmaydi. Agar yuqoridagi misolni mobil telefon orqali ko’rsangiz, ikkinchi box ning kontenti boxdan tashqariga chiqib ketgan bo’ladi. Shu sababli CSS3 da Flexbox xususiyati qo’shilgan. Shunda box qanchalik uzun bo’lsa ham kontent undan chiqib ketmasligini taminlay olasiz:

#### Misol <a href="#misol-3" id="misol-3"></a>

Flexbox yordamida moslashuvchan qutilar yaratamiz:

<figure><img src="../../../.gitbook/assets/image (743).png" alt=""><figcaption></figcaption></figure>

**Maslahat:** Flexbox haqida Flexbox haqidagi modulimiz orqali to’liqroq malumot olasiz

### Navigatsiya menyusi <a href="#navigatsiya-menyusi" id="navigatsiya-menyusi"></a>

Bundan tashqari **float**dan foydalangan holda gorizontal navigatsiya menyusini yasashingiz mumkin:

<figure><img src="../../../.gitbook/assets/image (330).png" alt=""><figcaption></figcaption></figure>

### Web layoutga misol <a href="#web-joylashuv-misoli" id="web-joylashuv-misoli"></a>

`float` yordamida butun boshli sahifanining joylashuvini to'g'rilab chiqish ham ancha mashxur usul hisoblanadi:

<figure><img src="../../../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure>

```
.header, .footer {
  background-color: grey;
  color: white;
  padding: 15px;
}

.column {
  float: left;
  padding: 15px;
}

.clearfix::after {
  content: "";
  clear: both;
  display: table;
}

.menu {
  width: 25%;
}

.content {
  width: 75%;
}
```

### Barcha CSS Float xususiyatlari <a href="#barcha-css-float-xususiyatlari" id="barcha-css-float-xususiyatlari"></a>

| Xususiyat                                                               | Ta'rif                                                                                                                          |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| [box-sizing](https://www.w3schools.com/cssref/css3\_pr\_box-sizing.asp) | Elementning kengligi va balandligi qanday hisoblanishini belgilaydi: ular padding va borderlarni o'z ichiga oladimi yoki yo'qmi |
| [clear](https://www.w3schools.com/cssref/pr\_class\_clear.asp)          | Float element yonida joylashgan element bilan nima sodir bo'lishi kerakligini belgilaydi                                        |
| [float](https://www.w3schools.com/cssref/pr\_class\_float.asp)          | Element o'ng, chap tomonga yoki umuman joylashmasligini belgilaydi.                                                             |
| [overflow](https://www.w3schools.com/cssref/pr\_pos\_overflow.asp)      | Element box dan oshib ketsa nima qilish kerakligini belgilaydi                                                                  |
| [overflow-x](https://www.w3schools.com/cssref/css3\_pr\_overflow-x.asp) | Element box ning chap/o'ng tomonida oshib ketsa nima qilish kerakligini belgilaydi                                              |
| [overflow-y](https://www.w3schools.com/cssref/css3\_pr\_overflow-y.asp) | Element box ning tepa/past tomonida oshib ketsa nima qilish kerakligini belgilaydi                                              |
