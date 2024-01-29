# CSS Foydalanuvchi interfeysi

### CSS User interfeysi

Ushbu bo'limda CSSning quyidagi user interfeys xususiyatlari haqida bilib olasiz:

* `resize`
* `outline-offset`

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar xususiyatni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Xususiyat      | Chrome | Edge | Firefox | Safari | Opera |
| -------------- | ------ | ---- | ------- | ------ | ----- |
| resize         | 4.0    | 79.0 | 5.0     | 4.0    | 15.0  |
| outline-offset | 4.0    | 15.0 | 5.0     | 4.0    | 9.5   |

### CSS O'lchamni o'zgartirish

`resize` xususiyati elementning o'lchamini foydalanuvchi tomonidan o'zgartirish mumkinligini belgilaydi.

![](<../../.gitbook/assets/image (432).png>)

Quyidagi kod foydalanuvchiga `<div>` elementining kengligini o'zgartirish imkonini beradi:

```
div {
  resize: horizontal;
  overflow: auto;
}
```

Quyidagi misol esa foydalanuvchiga `<div>` elementining balandligini o'zgartirish imkonini beradi:

```
div {
  resize: vertical;
  overflow: auto;
}
```

Quyidagi misol foydalanuvchiga `<div>` elementining balandligini va kengligini oʻzgartirish imkonini beradi:

```
div {
  resize: both;
  overflow: auto;
}
```

Ko'p brauzerlarda standart tarzda `<textarea>` elementinig o'lchamini o'zgartirish mumkin. Bu yerda o'lchamni o'zgartirishni o'chirish uchun `resize` xususiyatidan foydalandik:

```
textarea {
  resize: none;
}
```

### CSS Outline offset

`outline-offset` xususiyati outline  va elementning chegarasi o'rtasida bo'sh joy qo'shadi.

<figure><img src="../../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma:** Outline borderdan farq qiladi! Borderdan farqli o'laroq, outline element chegarasidan tashqarida chiziladi va boshqa kontentga qisman o'tishi mumkin. Bundan tashqari, outline element o'lchamlarining bir qismi EMAS; outline kengligi elementning umumiy kengligi va balandligiga tasir qilmaydi.
{% endhint %}

Quyidagi misolda chegara va outlie orasiga bo'sh joy qo'shish uchun `outline-offset` xususiyatidan foydalanilgan:

```
div.ex1 {
  margin: 20px;
  border: 1px solid black;
  outline: 4px solid red;
  outline-offset: 15px;
}

div.ex2 {
  margin: 10px;
  border: 1px solid black;
  outline: 5px dashed blue;
  outline-offset: 5px;
}
```

### CSSning user interfeys xususiyatlari

Quyidagi jadvalda user interfeysning barcha xususiyatlari keltirilgan:

| Xususiyat                                                                                                                                                       | Ta'rif                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [outline-offset](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_outline-offset.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Adds space between an outline and the edge or border of an element |
| [resize](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_resize.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                 | Specifies whether or not an element is resizable by the user       |
