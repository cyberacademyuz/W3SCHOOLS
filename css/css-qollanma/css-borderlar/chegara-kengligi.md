# Chegara kengligi

### CSS Border width <a href="#css-border-kengligi" id="css-border-kengligi"></a>

`border-width` xususiyati 4 ta chegaraning kengligini belgilaydi.

Kenglik maxsus o'lchov birliklari (px, pt, cm, em, )  asosida o'zgaritiriladi, yoki 3 ta oldindan belgilangan qiymatlardan biri yordamida beriladi (thin, medium yoki thick:

{% code title="Har xil border kengligini o'zgartirish usullari:" %}
```
p.one {
  border-style: solid;
  border-width: 5px;
}

p.two {
  border-style: solid;
  border-width: medium;
}

p.three {
  border-style: dotted;
  border-width: 2px;
}

p.four {
  border-style: dotted;
  border-width: thick;
}
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (82).png" alt=""><figcaption><p>Natija</p></figcaption></figure>

### Maxsus yon kengliklar <a href="#maxsus-yon-kengliklar" id="maxsus-yon-kengliklar"></a>

`border-width` xususiyati birdan to'rttagacha qiymat qabul qilishi mumkun (tepa chegara uchun, o'ng chegara uchun, pastki chegara uchun va chap chegara uchun)

```
p.one {
  border-style: solid;
  border-width: 5px 20px; /* 5px top and bottom, 20px on the sides */
}

p.two {
  border-style: solid;
  border-width: 20px 5px; /* 20px top and bottom, 5px on the sides */
}

p.three {
  border-style: solid;
  border-width: 25px 10px 4px 35px; /* 25px top, 10px right, 4px bottom and 35px left */
}
```
