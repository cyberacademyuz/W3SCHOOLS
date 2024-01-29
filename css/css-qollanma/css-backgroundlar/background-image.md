# Background image

### CSS Background-image <a href="#css-background-image-2" id="css-background-image-2"></a>

`background-image` xususiyati elementning backgroundiga rasm qo'yish uchun ishlatiladi.

Standart tarzda, rasm qayta qayta takrorlanadi, shuning uchun u butun elementni qamrab oladi.

{% code title="Sahifaning backgroundiga rasm qo'yamiz:" %}
```
body {
  background-image: url("paper.gif");
}
```
{% endcode %}

{% code title="Ushbu misol matn va background rasmning noto'g'ri birikmasini ko'rsatadi. Matnni o'qish qiyin:" %}
```
body {
  background-image: url("bgdesert.jpg");
}
```
{% endcode %}

{% hint style="warning" %}
**Note**: Background image dan foydalanayotganda matnni o'qishga ta'sir qilmaydigan rasmdan foydalaning.
{% endhint %}

Background rasm `<p>` elementi kabi muayyan elementlar uchun ham berilishi mumkin:

```
p {
  background-image: url("paper.gif");
}
```
