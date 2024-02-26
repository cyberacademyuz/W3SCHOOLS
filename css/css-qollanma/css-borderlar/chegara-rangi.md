# Chegara rangi

## <mark style="color:green;">Chegara rangi</mark> <a href="#css-border-rangi" id="css-border-rangi"></a>

<mark style="color:red;">`border-color`</mark> xususiyati 4 ta chegaraning rangini o'zgartirish uchun ishlatiladi.

Rang quyidagicha qiymatlar bilan qo'yilishi mumkin:

* rang nomi - rang nomiga qarab, masalan "red"
* HEX - HEX qiymatni bildiradi, masalan "#ff0000"
* RGB - RGB qiymatni bildiradi, masalan "rgb(255,0,0)"
* HSL - HSL qiymatini bildiradi, masalan "hsl(0, 100%, 50%)"
* transparent

**Eslatma:** agar <mark style="color:red;">`border-color`</mark> yozilmagan bo'lsa, u elementning rangini o'ziga meros qilib oladi.

{% tabs %}
{% tab title="CSS" %}
Turli chegara ranglarini ko'rsatib berish:

```css
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

Natija:

<figure><img src="../../../.gitbook/assets/image (177).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-color1" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Tomonlarning ranglarini belgilash</mark> <a href="#yon-tomon-ranglarni-belgilaydi" id="yon-tomon-ranglarni-belgilaydi"></a>

<mark style="color:red;">`border-color`</mark> xususiyati birdan to'rttagacha qiymat qabul qilishi mumkun (tepa chegara uchun, o'ng chegara uchun, pastki chegara uchun va chap chegara uchun)

{% tabs %}
{% tab title="CSS" %}
```css
p.one {
  border-style: solid;
  border-color: red green blue yellow; /* red top, green right, blue bottom and yellow left */
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-color2" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">HEX qiymatlari</mark> <a href="#hex-qiymatlari" id="hex-qiymatlari"></a>

Border ning ranglari Hexadecimal raqamlar bilan ham belgilanishi mumkin:

{% tabs %}
{% tab title="C" %}
```css
p.one {
  border-style: solid;
  border-color: #ff0000; /* red */
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-color-hex" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">RGB qiymatlari</mark> <a href="#rgb-qiymatlari" id="rgb-qiymatlari"></a>

Yoki RGB qiymatlardan ham foydalanish mumkin:

{% tabs %}
{% tab title="CSS" %}
```css
p.one {
  border-style: solid;
  border-color: rgb(255, 0, 0); /* red */
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-color-rgb" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">HSL qiymatlari</mark> <a href="#hsl-qiymatlari" id="hsl-qiymatlari"></a>

Bundan tashqari HSL qiymatlari asosida ham rang berishingiz olasiz:

{% tabs %}
{% tab title="CSS" %}
```css
p.one {
  border-style: solid;
  border-color: hsl(0, 100%, 50%); /* red */
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-color-hsl" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
HEX, RGB va HSL qiymatlari haqida <mark style="color:green;">CSS Ranglari</mark> bo'limida ko'proq ma'lumot olishingiz mumkin.
{% endhint %}
