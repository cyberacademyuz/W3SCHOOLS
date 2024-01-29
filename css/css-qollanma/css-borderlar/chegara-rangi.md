# Chegara rangi

### CSS Chegara rangi <a href="#css-border-rangi" id="css-border-rangi"></a>

`border-color` xususiyati 4 ta chegaraning rangini o'zgartirish uchun ishlatiladi.

Rang quyidagicha qiymatlar bilan qo'yilishi mumkin:

* rang nomi - rang nomiga qarab, masalan "red"
* HEX - HEX qiymatni bildiradi, masalan "#ff0000"
* RGB - RGB qiymatni bildiradi, masalan "rgb(255,0,0)"
* HSL - HSL qiymatini bildiradi, masalan "hsl(0, 100%, 50%)"
* transparent

**Eslatma:** agar `border-color` yozilmagan bo'lsa, u elementning rangini o'ziga meros qilib oladi.

{% code title="Turli chegara ranglarini ko'rsatib berish:" %}
```
p.one {
  border-style: solid;
  border-color: red;
}

p.two {
  border-style: solid;
  border-color: green;
}

p.three {
  border-style: dotted;
  border-color: blue;
}
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (177).png" alt=""><figcaption></figcaption></figure>

### Yon tomon ranglarni belgilash <a href="#yon-tomon-ranglarni-belgilaydi" id="yon-tomon-ranglarni-belgilaydi"></a>

`border-color` xususiyati birdan to'rttagacha qiymat qabul qilishi mumkun (tepa chegara uchun, o'ng chegara uchun, pastki chegara uchun va chap chegara uchun)

```
p.one {
  border-style: solid;
  border-color: red green blue yellow; /* red top, green right, blue bottom and yellow left */
}
```

### HEX qiymatlari <a href="#hex-qiymatlari" id="hex-qiymatlari"></a>

Border ning ranglari Hexadecimal raqamlar bilan ham belgilanishi mumkin:

```
p.one {
  border-style: solid;
  border-color: #ff0000; /* red */
}
```

### RGB qiymatlari <a href="#rgb-qiymatlari" id="rgb-qiymatlari"></a>

yoki RGB qiymatlardan ham foydalanish mumkin:

```
p.one {
  border-style: solid;
  border-color: rgb(255, 0, 0); /* red */
}
```

### HSL qiymatlari <a href="#hsl-qiymatlari" id="hsl-qiymatlari"></a>

Bundan tashqari HSL qiymatlari asosida ham rang berishingiz olasiz:

```
p.one {
  border-style: solid;
  border-color: hsl(0, 100%, 50%); /* red */
}
```

{% hint style="warning" %}
HEX, RGB va HSL qiymatlari haqida <mark style="color:green;">CSS Ranglari</mark> bo'limida ko'proq ma'lumot olishingiz mumkin.
{% endhint %}
