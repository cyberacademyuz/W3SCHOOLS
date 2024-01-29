# CSS Chegara rasmlari

<figure><img src="../../.gitbook/assets/image (794).png" alt=""><figcaption></figcaption></figure>

### CSS border-image xususiyati <a href="#css-border-image-xususiyati" id="css-border-image-xususiyati"></a>

`border-image` xususiyati oddiy chegara o'rniga rasmli chegara yaratish imkonini beradi.

Xususiyatning uchta bo'limi bor:

1. Border uchun ishlatiladigan rasm
2. Rasmni qayeri kesilishi kerakligi
3. O'rta qismlarni takrorlash yoki cho'zish kerakligini aniqlaydi

Biz quyidagi rasmdan foydalanamiz (border.png nomli)

![](<../../.gitbook/assets/image (824).png>)

`border-image` xususiyati rasmni oladi va uni tic-tac-toe taxtasi kabi to'qqiz qismga ajratadi. Keyin burchaklarni burchaklarga to'g'irlab joylashtiradi va o'rtadagi qismlar belgilaganingizdek takrorlanadi yoki cho'ziladi.

**Eslatma:** `border-image` ishlashi uchun, elementga `border` xususiyati berilishi kerak.

Pastda, o'rtadagi qism takrorlangan border keltirilgan:

<figure><img src="../../.gitbook/assets/image (835).png" alt=""><figcaption></figcaption></figure>

```
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 30 round;
}
```

Quyidada esa o'rta qismi cho'zilgan border keltirilgan:

<figure><img src="../../.gitbook/assets/image (777).png" alt=""><figcaption></figcaption></figure>

Kodi:

```
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 30 stretch;
}
```

{% hint style="warning" %}
**Maslahat:** `border-image` xususiyati aslida `border-image-source`, `border-image-slice`, `border-image-width`, `border-image-outset` va `border-image-repeat` xususiyatlarini qisqartmasi hisoblanadi.
{% endhint %}

### CSS border-image - Turlicha kesish qiymatlari <a href="#css-border-image-har-xil-kesish-qiymatlarida" id="css-border-image-har-xil-kesish-qiymatlarida"></a>

Turlicha kesish qiymatlari chegaraning ko'rinishini butunlay o'zgartiradi:

1 - Misol:

<figure><img src="../../.gitbook/assets/image (821).png" alt=""><figcaption></figcaption></figure>

2 - Misol:

<figure><img src="../../.gitbook/assets/image (814).png" alt=""><figcaption></figcaption></figure>

3 - Misol:

<figure><img src="../../.gitbook/assets/image (839).png" alt=""><figcaption></figcaption></figure>

Mana ularning kodi:

```
#borderimg1 {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 50 round;
}

#borderimg2 {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 20% round;
}

#borderimg3 {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 30% round;
}
```

### CSS ning border-image xususiyatlari <a href="#css-border-image-xususiyatlari" id="css-border-image-xususiyatlari"></a>

| Xususiyat                                                                                 | Ta'rif                                                                         |
| ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| [border-image](https://www.w3schools.com/cssref/css3\_pr\_border-image.asp)               | Barcha border-image-\* bo'lgan xususiyatlarning qisqartmasi                    |
| [border-image-source](https://www.w3schools.com/cssref/css3\_pr\_border-image-source.asp) | Border sifatida ishlatiladigan rasmning qanday bo'lishi kerakligini belgilaydi |
| [border-image-slice](https://www.w3schools.com/cssref/css3\_pr\_border-image-slice.asp)   | Border rasm qanday kesilishi kerakligini belgilaydi                            |
| [border-image-width](https://www.w3schools.com/cssref/css3\_pr\_border-image-width.asp)   | border rasmning uzunligini qancha bo'lishini belgilaydi                        |
| [border-image-outset](https://www.w3schools.com/cssref/css3\_pr\_border-image-outset.asp) | Border Rasmi maydoni borderdan tashqariga chiqadigan miqdorini belgilaydi      |
| [border-image-repeat](https://www.w3schools.com/cssref/css3\_pr\_border-image-repeat.asp) | Border rasm takrorlanishi kerakmi yoki cho'zilishi kerakmi belgilaydi          |
