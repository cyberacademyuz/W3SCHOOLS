# CSS Maskalash

Maskalash yordamida elementning qismlarini qisman yoki to'liq yashirish maqsadida element ustiga joylashtirish uchun niqob qatlamini yaratasiz.

### CSS mask-image xususiyati

CSSning `mask-image` xususiyati niqob qatlamining rasmini belgilaydi.

Maska layerining rasmi PNG, SVG, gradient yoki SVG \<mask> elementi bo'lishi mumkin.

### Brauzerning qo'llab-quvvatlashi

**Eslatma:** Ko'p brauzerlar maskalanishni qisman qo'llab-quvvatlaydi. Ko'pgina brauzerlarda standart xususiyatga qo'shimcha tarzda `-webkit-` prefiksidan foydalanishingiz kerak bo'ladi.

Quyidagi jadvaldagi raqamlar xususiyatni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi. `-webkit-`dan keyingi raqamlar prefiks bilan ishlaydigan birinchi versiyani ko'rsatadi.

| Xususiyat  | Chrome       | Edge          | Firefox | Safari       | Opera         |
| ---------- | ------------ | ------------- | ------- | ------------ | ------------- |
| mask-image | 4.0 -webkit- | 79.0 -webkit- | 53.0    | 4.0 -webkit- | 15.0 -webkit- |

### Rasmdan maska qatlarmi sifatida foydalanish

PNG yoki SVG rasmdan maska qatlami sifatida foydalanishda, maska qatlamining rasmini berish uchun `url()` qiymatidan foydalaning.

Maska rasmi shaffof yoki yarim shaffof maydonga ega bo'lishi kerak. Qora rang to'liq shaffoflikni bildiradi.

Biz foydalanadigan maska rasmi (PNG rasm):

![W3Schools.com](https://www.w3schools.com/css/w3logo.png)

Bu Italiyadagi Cinque Terreda olingan surat:

![](<../../.gitbook/assets/image (243).png>)

Endi maska rasmini Cinque Terre rasmi uchun maska qatlami sifatida qo'llaymiz:

![](<../../.gitbook/assets/image (591).png>)

{% code title="Uning kodi:" %}
```
.mask1 {
  -webkit-mask-image: url(w3logo.png);
  mask-image: url(w3logo.png);
  -webkit-mask-repeat: no-repeat;
  mask-repeat: no-repeat;
}
```
{% endcode %}

#### Misol tushuntirish

`mask-image` xususiyati element uchun maska qatlami sifatida foydalaniladigan rasmni belgilaydi.

`mask-repeat` xususiyati maska rasmining takrorlanishini yoki takrorlamaslgini belgilaydi. `no-repeat` qiymati maska rasmi takrorlanmasligini bildiradi (niqob rasmi faqat bir marta ko'rsatiladi).

### Yana bir misol

Agar ushbu `mask-repeat` xususiyatdan foydalanmasak, maska rasmi Cinque Terre rasmi bo'ylab  takrorlanadi:

![](<../../.gitbook/assets/image (248).png>)

Mana manba kodi:

```
.mask1 {
  -webkit-mask-image: url(w3logo.png);
  mask-image: url(w3logo.png);
}
```

### Gradientlardan maska qatlami sifatida foydalanish

CSSning linear va radial gradientlaridan maska qatlami sifatida ham foydalanish mumkin.

#### Linear gradientga misollar

Bu yerda rasm uchun maska qatlami sifatida linear gradientdan foydalanamiz. Ushbu linear gradient yuqoridan (qora) pastgacha (shaffof) boradi:

![](<../../.gitbook/assets/image (111).png>)\
&#x20;

Linear gradientdan maska qatlami sifatida foydalanish:

```
.mask1 {
  -webkit-mask-image: linear-gradient(black, transparent);
  mask-image: linear-gradient(black, transparent);
}
```

Bu yerda rasm uchun maska qatlami sifatida linear gradient va matn maskasidan foydalanamiz:

![](<../../.gitbook/assets/image (610).png>)

{% code title="Maska qatlami sifatida matnni maskalash bilan birga chiziqli gradientdan foydalanish:" %}
```
.mask1 {
  max-width: 600px;
  height: 350px;
  overflow-y: scroll;
  background: url(img_5terre.jpg) no-repeat;
  -webkit-mask-image: linear-gradient(black, transparent);
  mask-image: linear-gradient (black, transparent);
}
```
{% endcode %}

#### Radial gradientga misollar

Bu yerda rasm uchun maska qatlami sifatida radial-gradientdan (doira shaklida) foydalanamiz:

![](<../../.gitbook/assets/image (220).png>)

Maska qatlami sifatida radial gradientdan foydalanish:

```
.mask2 {
  -webkit-mask-image: radial-gradient(circle, black 50%, rgba(0, 0, 0, 0.5) 50%);
  mask-image: radial-gradient(circle, black 50%, rgba(0, 0, 0, 0.5) 50%);
}
```

Bu yerda rasm uchun maska qatlami sifatida radial-gradientdan (ellips shaklida) foydalanamiz:

![](<../../.gitbook/assets/image (345).png>)

Maska qatlami (ellips) sifatida boshqa radial gradientdan foydalanish:

```
.mask3 {
  -webkit-mask-image: radial-gradient(ellipse, black 50%, rgba(0, 0, 0, 0.5) 50%);
  mask-image: radial-gradient(ellipse, black 50%, rgba(0, 0, 0, 0.5) 50%);
}
```

### SVG dan maska qatlami sifatida foydalanish

SVGning `<mask>` elementi maska effektlarini yaratish uchun SVG grafikasi ichida ishlatilishi mumkin.

Bu yerda rasm uchun turli xil maska qatlamlarini yaratish uchun SVGning `<mask>` elementidan foydalanamiz:

![](<../../.gitbook/assets/image (249).png>)

SVGning maska qatlami (uchburchak shaklida yaratilgan):

```
<svg width="600" height="400">
  <mask id="svgmask1">
    <polygon fill="#ffffff" points="200 0, 400 400, 0 400"></polygon>
  </mask>
  <image xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="img_5terre.jpg" mask="url(#svgmask1)"></image>
</svg>Sorry, your browser does not support inline SVG.
```

![](<../../.gitbook/assets/image (640).png>)

SVGning maska qatlami (yulduz shaklida yaratilgan):

```
<svg width="600" height="400">
  <mask id="svgmask2">
    <polygon fill="#ffffff" points="100,10 40,198 190,78 10,78 160,198"></polygon>
  </mask>
  <image xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="img_5terre.jpg" mask="url(#svgmask2)"></image>
</svg>Sorry, your browser does not support inline SVG.
```

![](<../../.gitbook/assets/image (633).png>)

SVGning maska qatlami (doira shaklida shakllangan):

```
<svg width="600" height="400">
  <mask id="svgmask3">
    <circle fill="#ffffff" cx="75" cy="75" r="75"></circle>
    <circle fill="#ffffff" cx="80" cy="260" r="75"></circle>
    <circle fill="#ffffff" cx="270" cy="160" r="75"></circle>
  </mask>
  <image xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="img_5terre.jpg" mask="url(#svgmask3)"></image>
</svg>
```

### CSSning maskalash xususiyatlari

Quyidagi jadvalda CSSning barcha maskalash xususiyatlari keltirilgan:

| Xususiyat                                                                                                                                                     | Ta'rif                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| [mask-image](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_mask-image.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Specifies an image to be used as a mask layer for an element                              |
| [mask-mode](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_mask-mode.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)         | Specifies whether the mask layer image is treated as a luminance mask or as an alpha mask |
| [mask-origin](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_mask-origin.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Specifies the origin position (the mask position area) of a mask layer image              |
| [mask-position](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_mask-position.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Sets the starting position of a mask layer image (relative to the mask position area)     |
| [mask-repeat](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_mask-repeat.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Specifies how the mask layer image is repeated                                            |
| [mask-size](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_mask-size.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)         | Specifies the size of a mask layer image                                                  |
