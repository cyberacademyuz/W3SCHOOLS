# CSS Bir nechta ustular

### CSS Ko'p ustunli layout

CSS-ning ko'p ustunli layouti gazetalardagi kabi matnning bir nechta ustunlarini osongina ifodalash imkonini beradi:

<figure><img src="../../.gitbook/assets/image (433).png" alt=""><figcaption></figcaption></figure>

### CSSning ko'p ustunli xususiyatlari

Ushbu bo'limda quyidagi xususiyatlar haqida o'rganasiz:

* `column-count`
* `column-gap`
* `column-rule-style`
* `column-rule-width`
* `column-rule-color`
* `column-rule`
* `column-span`
* `column-width`

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar xususiyatni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Xususiyat         | Chrome | Edge | Forefox | Safari | Opera |
| ----------------- | ------ | ---- | ------- | ------ | ----- |
| column-count      | 50.0   | 10.0 | 52.0    | 9.0    | 37.0  |
| column-gap        | 50.0   | 10.0 | 52.0    | 9.0    | 37.0  |
| column-rule       | 50.0   | 10.0 | 52.0    | 9.0    | 37.0  |
| column-rule-color | 50.0   | 10.0 | 52.0    | 9.0    | 37.0  |
| column-rule-style | 50.0   | 10.0 | 52.0    | 9.0    | 37.0  |
| column-rule-width | 50.0   | 10.0 | 52.0    | 9.0    | 37.0  |
| column-span       | 50.0   | 10.0 | 71.0    | 9.0    | 37.0  |
| column-width      | 50.0   | 10.0 | 52.0    | 9.0    | 37.0  |

### CSS Bir nechtali ustunlar yaratish

`column-count` xususiyati elementning bo'linadigan ustunlar sonini belgilaydi.

Quyidagi misolda `<div>` elementidagi matn 3 ta ustunga ajratilgan:&#x20;

```
div {
  column-count: 3;
}
```

### CSS Ustunlar orasida bo'sh joy ochish

`column-gap` xususiyati ustunlar orasidagi bo'sh joyni belgilaydi.

Quyidagi misolda ustunlar orasida 40 pikselli bo'sh joy ochilgan:

```
div {
  column-gap: 40px;
}
```

### CSS Ustun qoidalari

`column-rule-style` xususiyati ustunlar orasidagi still qoidasini belgilaydi:

```
div {
  column-rule-style: solid;
}
```

`column-rule-width` xususiyati ustunlar orasidagi kenglik qoidasini belgilaydi:

```
div {
  column-rule-width: 1px;
}
```

`column-rule-color` xususiyati ustunlar orasidagi ranglar qoidasini belgilaydi:

```
div {
  column-rule-color: lightblue;
}
```

`column-rule` xususiyati yuqoridagi barcha `column-rule-*` xususiyatlarini bir deklaratsiyada berish uchun qisqartma xususiyat hisoblanadi.

Quyidagi misolda ustunlar orasidagi kenglik, still va rang qoidalari `column-rule` orqali beriladi:

```
div {
  column-rule: 1px solid lightblue;
}
```

### Element necha ustunni o'z ichiga olishi kerakligini belgilash

`column-span` xususiyati elementning qancha ustundan iborat bo'lishi kerakligini belgilaydi.

Quyidagi misolda `<h2>` elementi barcha ustunlarga o'tishi mumkinligi belgilanadi:

```
h2 {
  column-span: all;
}
```

### Ustun kengligini belgilash

`column-width` xususiyati ustunlar uchun, optimal kenglikni belgilaydi.

Quyidagi misolda ustunlar uchun optimal kenglik 100px bo'lishi kerakligini ko'rsatilgan:

```
div {
  column-width: 100px;
}
```

### CSS-ning ko'p ustunli xususiyatlari

Quyidagi jadvalda barcha ko'p ustunli xususiyatlar ro'yxati keltirilgan:&#x20;

| Xususiyat                                                                                                                                                             | Ta'rif                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [column-count](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-count.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)           | Specifies the number of columns an element should be divided into  |
| [column-fill](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-fill.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | Specifies how to fill columns                                      |
| [column-gap](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-gap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | Specifies the gap between the columns                              |
| [column-rule](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-rule.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | A shorthand property for setting all the column-rule-\* properties |
| [column-rule-color](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-rule-color.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Specifies the color of the rule between columns                    |
| [column-rule-style](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-rule-style.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Specifies the style of the rule between columns                    |
| [column-rule-width](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-rule-width.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Specifies the width of the rule between columns                    |
| [column-span](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-span.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | Specifies how many columns an element should span across           |
| [column-width](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-width.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)           | Specifies a suggested, optimal width for the columns               |
| [columns](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_columns.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                     | A shorthand property for setting column-width and column-count     |
