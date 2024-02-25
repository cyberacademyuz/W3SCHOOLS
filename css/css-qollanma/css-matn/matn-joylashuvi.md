# Matn joylashuvi

## <mark style="color:green;">Matn joylashuvi va matn yo'nalishi</mark> <a href="#matn-joylashuvi-va-matn-yonalishi" id="matn-joylashuvi-va-matn-yonalishi"></a>

Ushbu bo'limda quyidagi xususiyatlar haqida bilib olasiz:

* <mark style="color:red;">`text-align`</mark>
* <mark style="color:red;">`text-align-last`</mark>
* <mark style="color:red;">`direction`</mark>
* <mark style="color:red;">`unicode-bidi`</mark>
* <mark style="color:red;">`vertical align`</mark>

## <mark style="color:green;">Matn joylashuvi</mark> <a href="#matn-joylashuvi" id="matn-joylashuvi"></a>

<mark style="color:red;">`text-align`</mark> xususiyati matnni gorizontal shaklda joylashtirishga yordam beradi.

Matn yo chapga, yo o'ngga, yo o'rtaga joylashtirilgan, yoki butun kenglikni egallashga moslashtirilgan bo'lishi mumkin.

Quyidagi misol o'rtaga, chapga va o'ngga joylashtirilgan matnni ko'rsatadi (agar matn chapdan o'ngga o'qiladigan bo'lsa, unda matn default chapga joylashtiriladi va agar matn o'ngdan chapga o'qiladigan bo'lsa, unda matn default o'ngga joylashtiriladi):

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  text-align: center;
}

h2 {
  text-align: left;
}

h3 {
  text-align: right;
}
```
{% endtab %}
{% endtabs %}

Agar <mark style="color:red;">`text-align`</mark> xususiyatiga "**justify**" beriladigan bo'lsa, har bir satr har bir qatorning kengligiga teng joylashish uchun cho'ziladi hamda chap va o'ng marginlari tekis bo'ladi (jurnal va gazetalardagi kabi):

{% tabs %}
{% tab title="CSS" %}
```css
div {
  text-align: justify;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-align_all" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">text-align-last</mark> <a href="#text-align-last" id="text-align-last"></a>

<mark style="color:red;">`text-align-last`</mark> xususiyati matnning oxiridagi qator qanday joylashishi kerakligini belgilaydi.

{% tabs %}
{% tab title="Ruby" %}
Uchta <mark style="color:red;">`<p>`</mark> elementlarini joylashuvini o'zgartirish:

```css
p.a {
  text-align-last: right;
}

p.b {
  text-align-last: center;
}

p.c {
  text-align-last: justify;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-align-last" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Matn yo'nalishi</mark> <a href="#matn-yonalishi" id="matn-yonalishi"></a>

<mark style="color:red;">`direction`</mark> va <mark style="color:red;">`unicode-bidi`</mark> xususiyatlari matnning yo'nalishini o'zgartirish uchun ishlatiladi:

{% tabs %}
{% tab title="CSS" %}
```css
p {
  direction: rtl;
  unicode-bidi: bidi-override;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text_direction" %}
{% endtab %}
{% endtabs %}

## Vertikal joylashtirish <a href="#vertikal-joylashtirish" id="vertikal-joylashtirish"></a>

<mark style="color:red;">`vertical-align`</mark> xususiyati elementni vertikal joylashtirish uchun yordam beradi:

{% tabs %}
{% tab title="Ruby" %}
Matn ichidagi rasm vertikal joylashtirilayapti:

```css
img.a {
  vertical-align: baseline;
}

img.b {
  vertical-align: text-top;
}

img.c {
  vertical-align: text-bottom;
}

img.d {
  vertical-align: sub;
}

img.e {
  vertical-align: super;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_vertical-align" %}
{% endtab %}
{% endtabs %}

## CSSning matn joylashuvi/yo'nalishi xususiyatlari <a href="#css-matn-joylashtiruviyonalishi-xususiyatlari" id="css-matn-joylashtiruviyonalishi-xususiyatlari"></a>

| Xususiyat                                                                         | Ta'rif                                                                                                                                                                     |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [direction](https://www.w3schools.com/cssref/pr\_text\_direction.asp)             | Matn yo'nalishini belgilaydi                                                                                                                                               |
| [text-align](https://www.w3schools.com/cssref/pr\_text\_text-align.asp)           | Matnni gorizontal joylashuvini to'g'rilashga yordam beradi                                                                                                                 |
| [text-align-last](https://www.w3schools.com/cssref/css3\_pr\_text-align-last.asp) | Matndagi oxirgi satrni joylashuvini belgilaydi.                                                                                                                            |
| [unicode-bidi](https://www.w3schools.com/cssref/pr\_text\_unicode-bidi.asp)       | Bitta hujjatda bir nechta tillarni qo‘llab-quvvatlash uchun matnni bekor qilish kerakligini belgilash yoki qaytarish uchun direction xususiyati bilan birga foydalaniladi. |
| [vertical-align](https://www.w3schools.com/cssref/pr\_pos\_vertical-align.asp)    | Elementni vertikal joylashuvini belgilaydi                                                                                                                                 |
