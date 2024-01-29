# Font shorthand

### CSS Font qisqartmasi <a href="#css-font-qisqartmasi" id="css-font-qisqartmasi"></a>

Kodni qisqartirish uchun shrifting barcha alohida xususiyatlarini bitta xususiyatda ko'rsatish ham mumkin.

CSSning `font` qisqartmasi quyidagi xususiyatlarni bir qatorda yozish imkonini beradi:

* `font-style`
* `font-variant`
* `font-weight`
* `font-size/line-height`
* `font-family`

**Note:** `font-size` va `font-family` ning qiymatlarini kiritish majburiy. Agarda ikkalovidan bittasi ishlatilmasa, uning o'rniga default qiymat ishlatiladi.

{% code title="Bir nechta shrift xususiyatlarini bitta deklaratsiyada  o'rnatish uchun fontdan foydalaning:" %}
```
p.a {
  font: 20px Arial, sans-serif;
}

p.b {
  font: italic small-caps bold 12px/30px Georgia, serif;
}
```
{% endcode %}

### Barcha font xususiyatlari <a href="#barcha-font-xususiyatlari" id="barcha-font-xususiyatlari"></a>

| Xususiyat                                                                   | Ta'rif                                                                                |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| [font](https://www.w3schools.com/cssref/pr\_font\_font.asp)                 | Shriftning barcha xususiyatlarini bir qatorda yozishga imkon beradi                   |
| [font-family](https://www.w3schools.com/cssref/pr\_font\_font-family.asp)   | Matn uchun shrift oilasini belgilaydi                                                 |
| [font-size](https://www.w3schools.com/cssref/pr\_font\_font-size.asp)       | Shrift o'lchamini belgilaydi                                                          |
| [font-style](https://www.w3schools.com/cssref/pr\_font\_font-style.asp)     | Matn uchun shrift stilini belgilaydi                                                  |
| [font-variant](https://www.w3schools.com/cssref/pr\_font\_font-variant.asp) | Matn kichik katta harflar orqali tasvirlanishi kerakmi yoki yo'q shuni aniqlashtiradi |
| [font-weight](https://www.w3schools.com/cssref/pr\_font\_weight.asp)        | Shrift qalinligini belgilaydi                                                         |
