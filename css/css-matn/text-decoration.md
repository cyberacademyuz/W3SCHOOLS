# Text decoration

## <mark style="color:green;">Matn dekoratsiyasi</mark> <a href="#matn-dekoratsiyasi" id="matn-dekoratsiyasi"></a>

Ushbu bo'limda quyidagi xususiyatlar haqida bilib olasiz:

* <mark style="color:red;">`text-decoration-line`</mark>
* <mark style="color:red;">`text-decoration-color`</mark>
* <mark style="color:red;">`text-decoration-style`</mark>
* <mark style="color:red;">`text-decoration-thickness`</mark>
* <mark style="color:red;">`tex-decoration`</mark>

## <mark style="color:green;">Matnga dekoratsiya chizig'ini qo'shish</mark> <a href="#matnga-dekoratsiya-chizigini-qoshish" id="matnga-dekoratsiya-chizigini-qoshish"></a>

<mark style="color:red;">`text-decoration-line`</mark> xususiyati matnga dekoratsiya chizig'ini qo'shish uchun ishlatiladi.

**Maslahat:** Ushbu xususiyatda bittadan ortiq qiymat ishlata olasiz, masalan, ham <mark style="color:red;">`underline`</mark> ham <mark style="color:red;">`strike-through`</mark>ni bir vaqtda bitta element uchun qo'llashingiz mumkin.

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  text-decoration-line: overline;
}

h2 {
  text-decoration-line: line-through;
}

h3 {
  text-decoration-line: underline;
}

p {
  text-decoration-line: overline underline;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-decoration-line" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Note:** <mark style="color:red;">`underline`</mark> dekoratsiyasidan foydalanish har doim ham tavsiya qilinmaydi, sababi uni foydalanuvchilar link deb o'ylashligi mumkin.
{% endhint %}

## <mark style="color:green;">Matn dekoratsiyasiga rang berish</mark> <a href="#matn-dekoratsiyasiga-rang-berish" id="matn-dekoratsiyasiga-rang-berish"></a>

<mark style="color:red;">`text-decoration-color`</mark> xususiyati matn dekoratsiyasiga rang berish uchun ishlatiladmessage = "hello world"

{% tabs %}
{% tab title="Ruby" %}
```css
h1 {
  text-decoration-line: overline;
  text-decoration-color: red;
}

h2 {
  text-decoration-line: line-through;
  text-decoration-color: blue;
}

h3 {
  text-decoration-line: underline;
  text-decoration-color: green;
}

p {
  text-decoration-line: overline underline;
  text-decoration-color: purple;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-decoration-line" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Matn dekoratsiyasining stilini o'zgartirish</mark> <a href="#matn-dekoratsiyasini-stilini-ozgartirish" id="matn-dekoratsiyasini-stilini-ozgartirish"></a>

<mark style="color:red;">`text-decoration-style`</mark> xususiyati matn dekoratsiyasining stilini o'zgartirish uchun ishlatiladi

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  text-decoration-line: underline;
  text-decoration-style: solid;
}

h2 {
  text-decoration-line: underline;
  text-decoration-style: double;
}

h3 {
  text-decoration-line: underline;
  text-decoration-style: dotted;
}

p.ex1 {
  text-decoration-line: underline;
  text-decoration-style: dashed;
}

p.ex2 {
  text-decoration-line: underline;
  text-decoration-style: wavy;
}

p.ex3 {
  text-decoration-line: underline;
  text-decoration-color: red;
  text-decoration-style: wavy;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-decoration-style" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Matn dekoratsiyasining qalinligini belgilash</mark> <a href="#matn-dekoratsiyasini-qalinligini-belgilash" id="matn-dekoratsiyasini-qalinligini-belgilash"></a>

<mark style="color:red;">`text-decoration-thickness`</mark> orqali dekoratsiyaning qalinligini o'zgartira olasiz.

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  text-decoration-line: underline;
  text-decoration-thickness: auto;
}

h2 {
  text-decoration-line: underline;
  text-decoration-thickness: 5px;
}

h3 {
  text-decoration-line: underline;
  text-decoration-thickness: 25%;
}

p {
  text-decoration-line: underline;
  text-decoration-color: red;
  text-decoration-style: double;
  text-decoration-thickness: 5px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-decoration-thickness" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">text-decoration qisqartmasi</mark> <a href="#text-decoration-qisqartmasi" id="text-decoration-qisqartmasi"></a>

text-decoration qisqartmasi quyidagilarni bir qatorda yozish imkonini beradi:

* <mark style="color:red;">`text-decoration-line`</mark> (majburiy)
* <mark style="color:red;">`text-decoration-color`</mark> (ixtiyoriy)
* <mark style="color:red;">`text-decoration-style`</mark> (ixtiyoriy)
* <mark style="color:red;">`text-decoration-thickness`</mark> (ixtiyoriy)

{% tabs %}
{% tab title="CSS" %}
```scss
h1 {
  text-decoration: underline;
}

h2 {
  text-decoration: underline red;
}

h3 {
  text-decoration: underline red double;
}

p {
  text-decoration: underline red double 5px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-decoration" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">Kichik maslahat</mark> <a href="#kichik-maslahat" id="kichik-maslahat"></a>

HTML-dagi barcha liklarning tagiga standart tarzda pastki chiziqchizilgan bo'lsadi. Ba'zan havolalar tagiga chizilmagan holatda yaratilganligini ko'rasiz. <mark style="color:red;">`text-decoration: none;`</mark> havolalardan pastki chiziqni olib tashlash uchun ishlatiladi, masalan:

{% tabs %}
{% tab title="CSS" %}
```css
a {
  text-decoration: none;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-decoration_link" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">CSSning barcha text-decoration xususiyatlari</mark> <a href="#barcha-css-text-decoration-xususiyatlari" id="barcha-css-text-decoration-xususiyatlari"></a>

| Xususiyat                                                                                             | Ta'rif                                                                                                         |
| ----------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| [text-decoration](https://www.w3schools.com/cssref/pr\_text\_text-decoration.asp)                     | <mark style="color:red;">`text-decoration`</mark>ning barcha xususiyatlarini bir qatorda yozishga imkon beradi |
| [text-decoration-color](https://www.w3schools.com/cssref/css3\_pr\_text-decoration-color.asp)         | matn dekoratsiyasining rangini belgilaydi                                                                      |
| [text-decoration-line](https://www.w3schools.com/cssref/css3\_pr\_text-decoration-line.asp)           | Qanday text-decoration ishlatilishi kerakligini belgilaydi (underline, overline, etc.)                         |
| [text-decoration-style](https://www.w3schools.com/cssref/css3\_pr\_text-decoration-style.asp)         | Text-decoration ni stilini belgilaydi (solid, dotted, etc.)                                                    |
| [text-decoration-thickness](https://www.w3schools.com/cssref/pr\_text\_text-decoration-thickness.asp) | Text-decoration ni qalinligini belgilaydi                                                                      |
