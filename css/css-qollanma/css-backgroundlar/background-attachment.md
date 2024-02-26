# Background attachment

## <mark style="color:green;">CSS background-attachment</mark> <a href="#css-background-attachment" id="css-background-attachment"></a>

<mark style="color:red;">`background-attachment`</mark> xususiyati backgroundni pastga tushishi yoki qimirlamasligi kerakligini belgilaydi (sahifaning qolgan qismi bilan harakatlanmaydi):&#x20;

{% tabs %}
{% tab title="CSS" %}
Orqafondagi rasm qimirlamaydigan qilish:

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  background-attachment: fixed;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_attachment" %}
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Ruby" %}
Orqafondagi rasmni scroll bo'ladigan qilish:

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  background-attachment: scroll;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_attachment2" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Background attachment xususiyati</mark>

| Xususiyat                                                                               | Ta'rif                                                                                          |
| --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [background-attachment](https://www.w3schools.com/cssref/pr\_background-attachment.asp) | Background rasmi qimirlamasligini yoki sahifaning qolgan qismi bilan harakatlanishini oʻrnatadi |
