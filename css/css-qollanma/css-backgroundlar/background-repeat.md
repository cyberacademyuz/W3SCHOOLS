# Background repeat

### CSS background-repeat <a href="#css-background-image-repeat" id="css-background-image-repeat"></a>

Standart tarzda CSS backgrounddagi rasmni gorizontal va vertikal tarzda qayta-qayta chiqaradi.

Ba'zi rasmlar faqat gorizontal yoki faqat vertikal tarzda takrorlanishi kerak, aks holda ular g'alati ko'rinadi, masalan:

```
body {
  background-image: url("gradient_bg.png");
}
```

Yuqoridagi rasm faqat gorizontal tarzda takrorlansa (`background-repeat: repeat-x;`) fon yaxshiroq ko'rinadi:

```
body {
  background-image: url("gradient_bg.png");
  background-repeat: repeat-x;
}
```

{% hint style="warning" %}
**Maslahat:** Rasmni faqat vertikal taraflama takrormoqchi bo'lsangiz unda "`repeat-y`" qiymatidan foydalaning.
{% endhint %}

### CSS background-repeat: no-repeat <a href="#css-background-repeat-no-repeat" id="css-background-repeat-no-repeat"></a>

Backgrounddagi rasmni faqat o'zini takrorlashlarsiz korsatish uchun `background-repeat` xususiyatiga `no-repeat` qiymatini berish kerak:

{% code title="Background rasmini bir marta ko'rsatish:" %}
```
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
}
```
{% endcode %}

Yuqoridagi misolda backgroundning rasmi matn bilan bir joyda joylashtgan. Biz rasmning joylashuvini o'zgartirishimiz kerak, shunda u matnga xalaqt bermaydi.

### CSS background-position <a href="#css-background-position" id="css-background-position"></a>

`background-position` xususiyati baclground rasmning joylashuvini belgilash uchun ishlatiladi.

{% code title="Background rasmining joylashuvini tepa qismning o'ng tomoniga joylashtirish:" %}
```
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```
{% endcode %}

## CSSning backgound repeat va position xususiyatlari

| Xususiyat                                                                           | Ta'rif                                                   |
| ----------------------------------------------------------------------------------- | -------------------------------------------------------- |
| [background-position](https://www.w3schools.com/cssref/pr\_background-position.asp) | Background rasmining boshlang'ich joylashuvini o'rnatadi |
| [background-repeat](https://www.w3schools.com/cssref/pr\_background-repeat.asp)     | Background rasm qanday takrorlanishini belgilaydi        |
