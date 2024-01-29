# Outline Offset

### CSS outline ofseti <a href="#css-kontur-ofseti" id="css-kontur-ofseti"></a>

Outline-offset xususiyati outline va elementning cheti/chegarasi o'rtasida bo'sh joy qo'shadi. Element va uning outlinelari orasidagi bo'sh joy shaffof bo'ladi.

Quyidagi misolda outline va element chegarasi orasidagi joy 15 px:

<figure><img src="../../../.gitbook/assets/image (506).png" alt=""><figcaption></figcaption></figure>

```
p {
  margin: 30px;
  border: 1px solid black;
  outline: 1px solid red;
  outline-offset: 15px;
}
```

Quyidagi misol element va uning outlinelari orasidagi bo'sh joy shaffof ekanligini ko'rsatadi:

<figure><img src="../../../.gitbook/assets/image (475).png" alt=""><figcaption></figcaption></figure>

```
p {
  margin: 30px;
  background: yellow;
  border: 1px solid black;
  outline: 1px solid red;
  outline-offset: 15px;
}
```

### CSSning barcha outline xususiyatlari <a href="#barcha-css-kontur-xususiyatlari" id="barcha-css-kontur-xususiyatlari"></a>

| Xususiyat                                                                       | Ta'rif                                                                                                    |
| ------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [outline](https://www.w3schools.com/cssref/pr\_outline.asp)                     | outline-width, outline-style va outline-color xususiyatlarini bir deklaratsiyada bajarish imkonini beradi |
| [outline-color](https://www.w3schools.com/cssref/pr\_outline-color.asp)         | Outlinega rang beradi                                                                                     |
| [outline-offset](https://www.w3schools.com/cssref/css3\_pr\_outline-offset.asp) | Outline va elementning cheti yoki chegarasi orasiga bo'sh joy qo'shadi                                    |
| [outline-style](https://www.w3schools.com/cssref/pr\_outline-style.asp)         | Outline stilini belgilaydi                                                                                |
| [outline-width](https://www.w3schools.com/cssref/pr\_outline-width.asp)         | Outline kengligini belgilaydi                                                                             |
