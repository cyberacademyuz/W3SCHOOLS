# CSS Matn effektlari

### CSS Text Overflow, Word Wrap, Line Breaking qoidalari va Writing Modes <a href="#css-text-overflow-word-wrap-line-breaking-qoidalari-va-writing-modes" id="css-text-overflow-word-wrap-line-breaking-qoidalari-va-writing-modes"></a>

Ushbu bo'limda quyidagi xususiyatlar haqida o'rganasiz:

* `text-overflow`
* `word-wrap`
* `word-break`
* `writing-mode`

### CSS Text Overflow <a href="#css-text-overflow" id="css-text-overflow"></a>

CSSning `text-overflow` xususiyati element kengligidan o'tib ko'rinmay qolgan kontent foydalanuvchiga qanday bildirilishi kerakligini ifodalaydi.

U kesilib qolishi mumkin:

![](<../../.gitbook/assets/image (224).png>)

yoki u ellips shaklida ko'rsatilishi mumkin (...):

![](<../../.gitbook/assets/image (641).png>)

Uning CSS kodi:

```
p.test1 {
  white-space: nowrap;
  width: 200px;
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: clip;
}

p.test2 {
  white-space: nowrap;
  width: 200px;
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

Quyidagi misolda element ustiga sichqonchani olib borganingizda overflow bo'lgan kontentni qanday koʻrsatish mumkinligi koʻrsatilgan:

```
div.test:hover {
  overflow: visible;
}
```

### CSS Word Wrap <a href="#css-word-wrap" id="css-word-wrap"></a>

CSSning `word-wrap` xususiyati uzun so'zlarni bo'lish va keyingi qatorga o'tkazish imkonini beradi.

Agar so'z juda uzun bo'lsa, u chegaradan tashqariga chiqib ketadi:

![](<../../.gitbook/assets/image (638).png>)

`word-wrap` xususiyati matnni wrap qilishga majburlash imkonini beradi – hatto bu soʻzning oʻrtasidan boʻlinib qolishini bildirsa ham:

![](<../../.gitbook/assets/image (238).png>)

Uning CSS kodlari:

```
p {
  word-wrap: break-word;
}
```

### CSS Word Break <a href="#css-word-break" id="css-word-break"></a>

CSSning `word-break` xususiyati qatorni bo'lish qoidalarini belgilaydi.

![](<../../.gitbook/assets/image (532).png>)

Uning CSS kodlari:

```
p.test1 {
  word-break: keep-all;
}

p.test2 {
  word-break: break-all;
}
```

### CSS Writing Mode <a href="#css-writing-mode" id="css-writing-mode"></a>

CSSning `writing-mode` xususiyati matn qatorlar gorizontal yoki vertikal tarzda joylashtirilishini belgilaydi.

Some text with a span element with a ![](<../../.gitbook/assets/image (645).png>)writing-mode.

Quyidagi misolda turli xil `writing-mode` qoidalari ko'rsatilgan:

```
p.test1 {
  writing-mode: horizontal-tb;
}

span.test2 {
  writing-mode: vertical-rl;
}

p.test2 {
  writing-mode: vertical-rl;
}
```

### CSS ning matn effektlariga bog'liq xususiyatlari <a href="#css-text-effect-xususiyatlari" id="css-text-effect-xususiyatlari"></a>

Quyidagi jadvalda CSSning matn effeklariga tegishli xususiyatlar keltirilgan:

| Xususiyat                                                                     | Ta'rif                                                                                               |
| ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| [text-justify](https://www.w3schools.com/cssref/css3\_pr\_text-justify.asp)   | Tegishli matn qanday tekislanishi va oraliqlanishi kerakligini belgilaydi                            |
| [text-overflow](https://www.w3schools.com/cssref/css3\_pr\_text-overflow.asp) | Ko'rsatilmagan to'lib-toshgan kontent foydalanuvchiga qanday signal berilishi kerakligini belgilaydi |
| [word-break](https://www.w3schools.com/cssref/css3\_pr\_word-break.asp)       | CJK bo'lmagan skriptlar uchun qatorlarni ajratish qoidalarini belgilaydi                             |
| [word-wrap](https://www.w3schools.com/cssref/css3\_pr\_word-wrap.asp)         | Uzun so'zlarni uzish va keyingi qatorga o'tkazish imkonini beradi                                    |
| [writing-mode](https://www.w3schools.com/cssref/css3\_pr\_writing-mode.asp)   | Matn satrlari gorizontal yoki vertikal ravishda joylashtirilishini belgilaydi                        |
