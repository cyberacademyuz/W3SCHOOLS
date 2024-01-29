# Background attachment

### CSS background-attachment <a href="#css-background-attachment" id="css-background-attachment"></a>

`background-attachment` xususiyati backgroundni pastga tushishi yoki qimirlamasligi kerakligini belgilaydi (sahifaning qolgan qismi bilan harakatlanmaydi):&#x20;

{% code title="Bakgrounddagi rasm qimirlamay turishi belgilangan:" %}
```
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  background-attachment: fixed;
}
```
{% endcode %}

{% code title="Bakgrounddagi rasm scroll qilinishi belgilangan:" %}
```
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  background-attachment: scroll;
}
```
{% endcode %}

## CSS background attachment xususiyati

| Xususiyat                                                                               | Ta'rif                                                                                          |
| --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [background-attachment](https://www.w3schools.com/cssref/pr\_background-attachment.asp) | Background rasmi qimirlamasligini yoki sahifaning qolgan qismi bilan harakatlanishini oʻrnatadi |
