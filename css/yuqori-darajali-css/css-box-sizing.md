# CSS Box sizing

### CSS Box sizing

CSSning `box-sizing` xususiyati elementning umumiy kengligiga va balandligiga padding va chegara kiritish imkonini beradi.

### CSS box-sizing xususiyatisiz

Standart tarzda, elementning kengligi va balandligi quyidagicha hisoblanadi:

width + padding + border = elementning asl kengligi\
height + padding + border = elementning asl balandligi

Bu degani: Elementning kengligini/balandligini berganingizda, element ko'pincha bergan o'lchamdan kattaroq ko'rinadi (chunki elementning chegarasi va paddingi elementga berilgan kenglikga/balandlikga qo'shiladi).

Quyidagi rasmda bir xil width va height berilgan 2 ta `<div>` element ko'rsatilgan:

![](<../../.gitbook/assets/image (396).png>)

![](<../../.gitbook/assets/image (515).png>)

Yuqoridagi 2-ta `<div>` elementi natijada turli o'lchamlarga ega bo'ladi (chunki `<div2>`da padding berilgan):

```
.div1 {
  width: 300px;
  height: 100px;
  border: 1px solid blue;
}

.div2 {
  width: 300px;
  height: 100px;
  padding: 50px;
  border: 1px solid red;
}
```

`box-sizing` xususiyati bu muammoni hal qiladi.

### CSS box-sizing xususiyati bilan

`box-sizing` xususiyati padding va chegarani elementning umumiy kengligi va balandligiga kiritish imkonini beradi.

Agar elementga `box-sizing:border-box;` bersangiz, padding va chegara elementning kengligiga va balandligiga kiritiladi:

![](<../../.gitbook/assets/image (405).png>)

![](<../../.gitbook/assets/image (747).png>)

Yuqoridagiga o'xshash misol, ikkala `<div>` elementiga ham `box-sizing:border-box;` berilgan:

```
.div1 {
  width: 300px;
  height: 100px;
  border: 1px solid blue;
  box-sizing: border-box;
}

.div2 {
  width: 300px;
  height: 100px;
  padding: 50px;
  border: 1px solid red;
  box-sizing: border-box;
}
```

`box-sizing:border-box;`dan foydalanish samarali bo'lgani uchun, ko'p dasturchilar o'z sahifalaridagi barcha elementlarni shu tarzda ishlashini xohlashadi.

Quyidagi kod barcha elementlarni yanada intuitiv tarzda o'lchanishini ta'minlaydi. Ko'p brauzerlar forma elementlari uchun allaqachon `box-sizing: border-box`dan foydalanadi (lekin hammasi ham emas - shuning uchun input va textarealar width: 100% bo'lganida har xil ko'rinadi).

Buni barcha elementlarga qo'llash xavfsiz va oqilona ish:

```
* {
  box-sizing: border-box;
}
```

### CSS Box o'lchami xususiyati

| Xususiyat                                                                                                                                               | Ta'rif                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| [box-sizing](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_box-sizing.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Defines how the width and height of an element are calculated: should they include padding and borders, or not |
