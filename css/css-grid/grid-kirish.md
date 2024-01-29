# Grid Kirish

<figure><img src="../../.gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure>

### Grid Layout

CSSning Grid Layout moduli qatorlar va ustunlar bilan gridga asoslangan layout tizimini qiladi, bu esa float va positioningdan foydalanmasdan veb-sahifalarning dizaynini tuzishni osonlashtiradi.

### Brauzerning qo'llab-quvvatlashi

Grid xususiyatlari barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi.

| Chrome | Edge | Firefox | Safari | Opera |
| ------ | ---- | ------- | ------ | ----- |
| 57.0   | 16.0 | 52.0    | 10     | 44    |

***

### Grid elementlari

Grid layouti bir yoki bir nechta bola elementlarga ega bo'lgan ota elementdan iborat.

```
<div class="grid-container">
  <div class="grid-item">1</div>
  <div class="grid-item">2</div>
  <div class="grid-item">3</div>
  <div class="grid-item">4</div>
  <div class="grid-item">5</div>
  <div class="grid-item">6</div>
  <div class="grid-item">7</div>
  <div class="grid-item">8</div>
  <div class="grid-item">9</div>
</div>
```

<figure><img src="../../.gitbook/assets/image (397).png" alt=""><figcaption></figcaption></figure>

### Displey xususiyati

HTML elementining `display` xususiyati `grid` yoki `inline-grid` qilinganida grid konteyneriga aylanadi.

```
.grid-container {
  display: grid;
}
```

```
.grid-container {
  display: inline-grid;
}
```

Grid konteynerining barcha bola elementlari avtomatik tarzda grid _elementlariga_ aylanadi.

### Grid ustunlari

Grid elementlarining vertikal chiziqlari _ustunlar_ deb ataladi.

![](https://www.w3schools.com/css/grid\_columns.png)

### Grid qatorlari

Grid elementlarining gorizontal chiziqlari _qatorlar_ deb ataladi.

![](https://www.w3schools.com/css/grid\_rows.png)

### Grid gap

Har bir ustun/qator orasidagi bo'sh joylar gap deb ataladi.

![](<../../.gitbook/assets/image (749).png>)

Quyidagi xususiyatlardan biri yordamida gap o'lchamini sozlashingiz mumkin:

* `column-gap`
* `row-gap`
* `gap`

{% code title="column-gap xususiyati ustunlar orasidagi gapni belgilaydi:" %}
```
.grid-container {
  display: grid;
  column-gap: 50px;
}
```
{% endcode %}

{% code title=" row-gap xususiyati qatorlar orasidagi bo'shliqni o'rnatadi:" %}
```
.grid-container {
  display: grid;
  row-gap: 50px;
}
```
{% endcode %}

{% code title="gap xususiyati row-gap va column-gap xususiyatlarning qisqartmasi hisoblanadi:" %}
```
.grid-container {
  display: grid;
  gap: 50px 100px;
}
```
{% endcode %}

{% code title="gap xususiyatidan qatorlar va ustunlar oralig'ini bitta xususiyatda bilan o'rnatish uchun ham foydalanish mumkin:" %}
```
.grid-container {
  display: grid;
  gap: 50px;
}
```
{% endcode %}

### Grid chiziqlari

Ustunlar orasidagi chiziqlar  _ustun chiziqlari_ deyiladi.

Qatorlar orasidagi chiziqlar _qator chiziqlar_ deyiladi.

![](<../../.gitbook/assets/image (736).png>)

Grid elementini grid konteyneriga joylashtirishda qator raqamlariga qarang:

{% code title="Grid elementini 1-ustun qatoriga qo‘ying va 3-ustun qatorida tugasin:" %}
```
.item1 {
  grid-column-start: 1;
  grid-column-end: 3;
}
```
{% endcode %}

{% code title="Grid elementini 1-qatorga qo'ying va 3-qatorda tugasin:" %}
```
.item1 {
  grid-row-start: 1;
  grid-row-end: 3;
}
```
{% endcode %}

### CSSning barcha grid xususiyatlari

| Xususiyat                                                                                                                                                               | Ta'rif                                                                                                                                                                              |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [column-gap](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_column-gap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                 | Specifies the gap between the columns                                                                                                                                               |
| [gap](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_gap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                               | A shorthand property for the _row-gap_ and the _column-gap_ properties                                                                                                              |
| [grid](https://www-w3schools-com.translate.goog/cssref/pr\_grid.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                                   | A shorthand property for the _grid-template-rows, grid-template-columns, grid-template-areas, grid-auto-rows, grid-auto-columns_, and the _grid-auto-flow_ properties               |
| [grid-area](https://www-w3schools-com.translate.goog/cssref/pr\_grid-area.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                         | Either specifies a name for the grid item, or this property is a shorthand property for the _grid-row-start_, _grid-column-start_, _grid-row-end_, and _grid-column-end_ properties |
| [grid-auto-columns](https://www-w3schools-com.translate.goog/cssref/pr\_grid-auto-columns.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)         | Specifies a default column size                                                                                                                                                     |
| [grid-auto-flow](https://www-w3schools-com.translate.goog/cssref/pr\_grid-auto-flow.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | Specifies how auto-placed items are inserted in the grid                                                                                                                            |
| [grid-auto-rows](https://www-w3schools-com.translate.goog/cssref/pr\_grid-auto-rows.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | Specifies a default row size                                                                                                                                                        |
| [grid-column](https://www-w3schools-com.translate.goog/cssref/pr\_grid-column.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                     | A shorthand property for the _grid-column-start_ and the _grid-column-end_ properties                                                                                               |
| [grid-column-end](https://www-w3schools-com.translate.goog/cssref/pr\_grid-column-end.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | Specifies where to end the grid item                                                                                                                                                |
| [grid-column-gap](https://www-w3schools-com.translate.goog/cssref/pr\_grid-column-gap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | Specifies the size of the gap between columns                                                                                                                                       |
| [grid-column-start](https://www-w3schools-com.translate.goog/cssref/pr\_grid-column-start.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)         | Specifies where to start the grid item                                                                                                                                              |
| [grid-gap](https://www-w3schools-com.translate.goog/cssref/pr\_grid-gap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                           | A shorthand property for the _grid-row-gap_ and _grid-column-gap_ properties                                                                                                        |
| [grid-row](https://www-w3schools-com.translate.goog/cssref/pr\_grid-row.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                           | A shorthand property for the _grid-row-start_ and the _grid-row-end_ properties                                                                                                     |
| [grid-row-end](https://www-w3schools-com.translate.goog/cssref/pr\_grid-row-end.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                   | Specifies where to end the grid item                                                                                                                                                |
| [grid-row-gap](https://www-w3schools-com.translate.goog/cssref/pr\_grid-row-gap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                   | Specifies the size of the gap between rows                                                                                                                                          |
| [grid-row-start](https://www-w3schools-com.translate.goog/cssref/pr\_grid-row-start.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | Specifies where to start the grid item                                                                                                                                              |
| [grid-template](https://www-w3schools-com.translate.goog/cssref/pr\_grid-template.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                 | A shorthand property for the _grid-template-rows_, _grid-template-columns_ and _grid-areas_ properties                                                                              |
| [grid-template-areas](https://www-w3schools-com.translate.goog/cssref/pr\_grid-template-areas.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Specifies how to display columns and rows, using named grid items                                                                                                                   |
| [grid-template-columns](https://www-w3schools-com.translate.goog/cssref/pr\_grid-template-columns.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Specifies the size of the columns, and how many columns in a grid layout                                                                                                            |
| [grid-template-rows](https://www-w3schools-com.translate.goog/cssref/pr\_grid-template-rows.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Specifies the size of the rows in a grid layout                                                                                                                                     |
| [row-gap](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_row-gap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                       | Specifies the gap between the grid rows                                                                                                                                             |
