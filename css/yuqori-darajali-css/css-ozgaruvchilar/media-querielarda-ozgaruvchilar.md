# Media Querielarda o'zgaruvchilar

### Media querielarda o'zgaruvchilardan foydalanish

Endi media querielar ichidagi o'zgaruvchining qiymatini o'zgartiramiz.

{% hint style="warning" %}
**Maslahat:** Media querielar turli qurilmalar (ekranlar, planshetlar, mobil telefonlar va h.k.) uchun turli still qoidalarini belgilashga qaratilgan. <mark style="color:green;">**Media querielar**</mark> boʻlimida koʻproq maʼlumot olishingiz mumkin.
{% endhint %}

Bu yerda birinchi navbatda `.container` classi uchun `--fontsize` nomli yangi lokal o'zgaruvchi e'lon qilamiz. Uning qiymatini **25px** qiladik. Keyin uni `.container` classida ishlatamiz. Keyin, `@media` qoidasini yaratamiz, unda "Brauzerning kengligi **450px** yoki undan kattaroq bo'lsa, `.container` classidagi `--fontsize` o'zgaruvchising qiymatini **50px**ga o'zgartiramiz"

Mana to'liq kod:

```
/* Variable declarations */
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

.container {
  --fontsize: 25px;
}

/* Styles */
body {
  background-color: var(--blue);
}

h2 {
  border-bottom: 2px solid var(--blue);
}

.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
  font-size: var(--fontsize);
}

@media screen and (min-width: 450px) {
  .container {
    --fontsize: 50px;
  }
}
```

`@media` qoidasidagi `--blue` o'zgaruvchisining qiymatini ham o'zgartiradigan yana bir misol:

```
/* Variable declarations */
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

.container {
  --fontsize: 25px;
}

/* Styles */
body {
  background-color: var(--blue);
}

h2 {
  border-bottom: 2px solid var(--blue);
}

.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
  font-size: var(--fontsize);
}

@media screen and (min-width: 450px) {
  .container {
    --fontsize: 50px;
  }
   :root {
    --blue: lightblue;
  }
}
```

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar `var()` funksiyasini to'liq qo'llab-quvvatlaydigan brauzerlarning il versiyasi ko'rsatadi.

| Function |      |      |      |     |      |
| -------- | ---- | ---- | ---- | --- | ---- |
| var()    | 49.0 | 15.0 | 31.0 | 9.1 | 36.0 |

***

### CSS var() funktsiyasi

| Xususiyat                                                                                                                               | Ta'rif                              |
| --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| [var()](https://www-w3schools-com.translate.goog/cssref/func\_var.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Inserts the value of a CSS variable |
