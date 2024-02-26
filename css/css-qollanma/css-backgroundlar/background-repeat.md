# Background repeat

### <mark style="color:green;">background-repeat</mark> <a href="#css-background-image-repeat" id="css-background-image-repeat"></a>

Standart tarzda CSS <mark style="color:red;">`background-image`</mark> xususiyati gorizontal va vertikal tarzda qayta-qayta chiqaradi.

Ba'zi rasmlar faqat gorizontal yoki faqat vertikal tarzda takrorlanishi kerak, aks holda ular g'alati ko'rinadi, masalan:

{% tabs %}
{% tab title="CSS" %}
```css
body {
  background-image: url("gradient_bg.png");
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_gradient1" %}
{% endtab %}
{% endtabs %}

Yuqoridagi rasm faqat gorizontal tarzda takrorlansa (<mark style="color:red;">`background-repeat: repeat-x;`</mark>) fon yaxshiroq ko'rinadi:

{% tabs %}
{% tab title="CSS" %}
```css
body {
  background-image: url("gradient_bg.png");
  background-repeat: repeat-x;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_gradient2" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Maslahat:** Rasmni faqat vertikal taraflama takrormoqchi bo'lsangiz unda <mark style="color:red;">`repeat-y`</mark> qiymatidan foydalaning.
{% endhint %}

## <mark style="color:green;">CSS background-repeat: no-repeat</mark> <a href="#css-background-repeat-no-repeat" id="css-background-repeat-no-repeat"></a>

Backgrounddagi rasmni faqat o'zini takrorlashlarsiz korsatish uchun <mark style="color:red;">`background-repeat`</mark> xususiyatiga <mark style="color:red;">`no-repeat`</mark> qiymatini berish kerak:

{% tabs %}
{% tab title="CSS" %}
Orqafon rasmni bir marta ko'rsatish:

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_norepeat" %}
{% endtab %}
{% endtabs %}

Yuqoridagi misolda backgroundning rasmi matn bilan bir joyda joylashtgan. Biz rasmning joylashuvini o'zgartirishimiz kerak, shunda u matnga xalaqt bermaydi.

## <mark style="color:green;">background-position</mark> <a href="#css-background-position" id="css-background-position"></a>

<mark style="color:red;">`background-position`</mark> xususiyati baclground rasmning joylashuvini belgilash uchun ishlatiladi.

{% tabs %}
{% tab title="CSS" %}
Orqafon rasmning joylashuvini tepa qismning o'ng tomoniga joylashtirish:

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_position" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">CSSning backgound repeat va position xususiyatlari</mark>

| Xususiyat                                                                           | Ta'rif                                                   |
| ----------------------------------------------------------------------------------- | -------------------------------------------------------- |
| [background-position](https://www.w3schools.com/cssref/pr\_background-position.asp) | Background rasmining boshlang'ich joylashuvini o'rnatadi |
| [background-repeat](https://www.w3schools.com/cssref/pr\_background-repeat.asp)     | Background rasm qanday takrorlanishini belgilaydi        |
