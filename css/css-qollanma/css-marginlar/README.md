# CSS Marginlar

Marginlar berilgan chegaralarning tashqarisidagi elementlar atrofida bo'sh joy hosil qilish uchun ishlatiladi.

<figure><img src="../../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin_intro" %}

## <mark style="color:green;">CSS Marginlar</mark> <a href="#css-margin" id="css-margin"></a>

CSSning <mark style="color:red;">`margin`</mark> xususiyatlari elementlar atrofida, belgilangan chegaraning tashqi qismida bo'sh joy hosil qilish uchun ishlatiladi

CSS yordamida marginlarni boshqara olasiz. Elementning har bir tomoni (tepa, o'ng, pastki va chap) uchun alohida margin berish xususiyatlari mavjud.

## <mark style="color:green;">Margin - Alohida tomonlar</mark> <a href="#margin-individual-tomonlarda" id="margin-individual-tomonlarda"></a>

CSS elementning har bir tomoniga margin berish uchun bir nechta xususiyatlarga ega:

* <mark style="color:red;">`margin-top`</mark>
* <mark style="color:red;">`margin-right`</mark>
* <mark style="color:red;">`margin-bottom`</mark>
* <mark style="color:red;">`margin-left`</mark>

Barcha margin xususiyatlari quyidagi qiymatlarni o'z ichiga oladi:

* <mark style="color:red;">`auto`</mark> - marginni brauzerning o'zi hisoblaydi
* <mark style="color:red;">`length`</mark> - margin qiymatlari px, pt, cm, va hokazolar asosida belgilanadi
* <mark style="color:red;">`%`</mark> - margin qiymatlarini o'z ichiga olgan elementlarning kengligini % da hisoblaydi
* <mark style="color:red;">`inherit`</mark> - ota elementdagi qiymatni meros qilib oladi

**Maslahat:** Negativ qiymatlarga ruxsat beriladi

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`<p>`</mark> elementining barcha tomoniga turli xil margin o'rnatish:

```css
p {
  margin-top: 100px;
  margin-bottom: 100px;
  margin-right: 150px;
  margin-left: 80px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin_sides" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Margin - qisqarma xususiyat</mark> <a href="#margin-qisqartmasi" id="margin-qisqartmasi"></a>

Marginning barcha xususiyatlarini bitta xususiyat ichida bir qatorda yozish mumkin.

<mark style="color:red;">`margin`</mark> xususiyati marginning quyidagi xususiyatlarini qisqartirib bera oladi:

* <mark style="color:red;">`margin-top`</mark>
* <mark style="color:red;">`margin-right`</mark>
* <mark style="color:red;">`margin-bottom`</mark>
* <mark style="color:red;">`margin-left`</mark>

Ular mana bunday ishlaydi:

Agarda <mark style="color:red;">`margin`</mark> xususiyatida 4 ta qiymat bo'lsa:

* **margin: 25px 50px 75px 100px;**
  * tepa qism margini 25px
  * o'ng tomon margini 50px
  * pastki qism margini 75px
  * chap tomon margini 100px

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`margin`</mark> qisqartmasini 4 ta qiymat bilan ishlatish:

```css
p {
  margin: 25px 50px 75px 100px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin_shorthand_4val" %}
{% endtab %}
{% endtabs %}

Agar <mark style="color:red;">`margin`</mark> xususiyatida 3 ta qiymat bo'lsa:

* **margin: 25px 50px 75px;**
  * tepa qism margini 25px
  * o'ng va chap tomon margini 50px
  * pastki qism margini 75px

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`margin`</mark> qisqartmasini 3 ta qiymat bilan ishlatish:

```css
p {
  margin: 25px 50px 75px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin_shorthand_4val" %}
{% endtab %}
{% endtabs %}

Agar <mark style="color:red;">`margin`</mark> xususiyatida 2 ta qiymat bo'lsa:

* **margin: 25px 50px;**
  * tepa va pastki qism margini 25px
  * o'ng va chap tomon margini 50px

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`margin`</mark> qisqartmasini 2 ta qiymat bilan ishlatish:

```css
p {
  margin: 25px 50px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin_shorthand_3val" %}
{% endtab %}
{% endtabs %}

Agar <mark style="color:red;">`margin`</mark> xususiyatida bitta qiymat bo'lsa:

* **margin: 25px;**
  * barcha tomonlardagi margin 25px

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`margin`</mark> qisqartmasini 1 ta qiymat bilan ishlatish:

```css
p {
  margin: 25px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin_shorthand_1val" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Auto qiymati</mark> <a href="#auto-qiymati" id="auto-qiymati"></a>

Elementni konteyner ichida gorizontal tarzda o'rtaga olib kelish uchun margin xususiyatini avtomati auto  qilishingiz mumkin.

Keyin element belgilangan kenglikni egallaydi va qolgan bo'sh joy chap va o'ng narginlar orasida teng ravishda bo'linadi.

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`margin: auto;`</mark> dan foydalanish:

```css
div {
  width: 300px;
  margin: auto;
  border: 1px solid red;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin_auto" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Inherit qiymati</mark> <a href="#inherit-qiymati" id="inherit-qiymati"></a>

Bu misoldagi <mark style="color:red;">`<p class="ex1">`</mark> elementi ota element hisoblangan <mark style="color:red;">`<div>`</mark> elementidan chap tomon marginining qiymatini meros qilib oladi:

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`inherit`</mark> qiymatidan foydalanish:

```css
div {
  border: 1px solid red;
  margin-left: 100px;
}

p.ex1 {
  margin-left: inherit;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin-left_inherit" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">Barcha CSS margin xususiyatlari</mark> <a href="#barcha-css-margin-xususiyatlari" id="barcha-css-margin-xususiyatlari"></a>

| Xususiyat                                                               | Ta'rif                                                              |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [margin](https://www.w3schools.com/cssref/pr\_margin.asp)               | Marginning barcha xususiyatlarini bir qatorda yozishga imkon beradi |
| [margin-bottom](https://www.w3schools.com/cssref/pr\_margin-bottom.asp) | Elementning pastki qismiga margin beradi                            |
| [margin-left](https://www.w3schools.com/cssref/pr\_margin-left.asp)     | Elementning chap tomoniga margin beradi                             |
| [margin-right](https://www.w3schools.com/cssref/pr\_margin-right.asp)   | Elementning o'ng tomoniga margin beradi                             |
| [margin-top](https://www.w3schools.com/cssref/pr\_margin-top.asp)       | Elementning tepa qismiga margin beradi                              |
