# Background image

## <mark style="color:green;">CSS Background-image</mark> <a href="#css-background-image-2" id="css-background-image-2"></a>

<mark style="color:red;">`background-image`</mark> xususiyati elementning backgroundiga rasm qo'yish uchun ishlatiladi.

Standart tarzda, rasm qayta qayta takrorlanadi, shuning uchun u butun elementni qamrab oladi.

{% tabs %}
{% tab title="CSS" %}
Sahifaning backgroundiga rasm qo'yamiz:

```css
body {
  background-image: url("paper.gif");
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image" %}
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="CSS" %}
Ushbu misol matn va background rasmning noto'g'ri birikmasini ko'rsatadi. Matnni o'qish qiyin:

```css
body {
  background-image: url("bgdesert.jpg");
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_bad" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Eslatma**: <mark style="color:red;">`background-image`</mark>dan foydalanayotganda matnni o'qishga ta'sir qilmaydigan rasmdan foydalaning.
{% endhint %}

&#x20;<mark style="color:red;">`<p>`</mark> elementi kabi muayyan elementlar uchun ham orqafon rasm berilishi mumkin:

{% tabs %}
{% tab title="CSS" %}
```css
p {
  background-image: url("paper.gif");
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_p" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">CSSning orqafon rasm xususiyati</mark>

| Xususiyat                                                                     | Ta'rif                             |
| ----------------------------------------------------------------------------- | ---------------------------------- |
| [background-image](https://www.w3schools.com/cssref/pr\_background-image.asp) | Elementning orqafoniga rasm beradi |
