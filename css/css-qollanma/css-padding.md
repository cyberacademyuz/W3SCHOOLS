# CSS Padding

Padding berilgan chegaraning ichqi qismidagi elementlar kontenti atrofida bo'sh joy hosil qilish uchun beriladi.

<figure><img src="../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_padding_intro" %}

## <mark style="color:green;">CSS Padding</mark> <a href="#css-padding" id="css-padding"></a>

CSSning <mark style="color:red;">`padding`</mark> xususiyati berilgan chegaraning ichqi qismidagi elementlar kontenti atrofida bo'sh joy hosil qilish uchun beriladi.

CSS yordamida paddingni boshqara olasiz. Elementning har bir tomoni (tepa, o'ng, pastki va chap) uchun alohida padding berish xususiyatlari mavjud.

### <mark style="color:green;">Padding - Alohida tomonlar</mark> <a href="#padding-individual-tomonlarda" id="padding-individual-tomonlarda"></a>

CSS elementning har bir tomoniga padding berish uchun bir nechta xususiyatlarga ega

* <mark style="color:red;">`padding-top`</mark>
* <mark style="color:red;">`padding-right`</mark>
* <mark style="color:red;">`padding-bottom`</mark>
* <mark style="color:red;">`padding-left`</mark>

Barcha padding xususiyatlari quyidagi qiymatlarni o'z ichiga oladi:

* <mark style="color:red;">`length`</mark> - padding qiymatlari px, pt, cm, va hokazolar asosida belgilanadi
* <mark style="color:red;">`%`</mark> - padding qiymatlarini o'z ichiga olgan elementlarning kengligini % da hisoblaydi
* <mark style="color:red;">`inherit`</mark> - ota elementdagi qiymatni meros qilib oladi

**Maslahat:** Negativ qiymatlarga ruxsat beriladi

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`<p>`</mark> elementning barcha tomonlari uchun turli xil padding berish:

```css
p {
  padding-top: 100px;
  padding-bottom: 100px;
  padding-right: 150px;
  padding-left: 80px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_padding_sides" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Padding qisqartmasi</mark> <a href="#padding-qisqartmasi" id="padding-qisqartmasi"></a>

Paddingning barcha xususiyatlarini bitta xususiyat ichida bir qatorda yozish mumkin.

<mark style="color:red;">`padding`</mark> xususiyati quyidagi padding xususiyatlarini qisqartirib bera oladi:

* <mark style="color:red;">`padding-top`</mark>
* <mark style="color:red;">`padding-right`</mark>
* <mark style="color:red;">`padding-bottom`</mark>
* <mark style="color:red;">`padding-left`</mark>

Ular mana bunday ishlaydi:

Agarda padding xususiyatida 4 ta qiymat bo'lsa:

* **padding: 25px 50px 75px 100px;**
  * tepa qism paddinggi 25px
  * o'ng tomon paddinggi 50px
  * pastki qism paddinggi 75px
  * chap tomon paddinggi 100px

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`padding`</mark>ni 4 ta qiymat bilan birga ishlatish:

```css
p {
  padding: 25px 50px 75px 100px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_padding_shorthand_4val" %}
{% endtab %}
{% endtabs %}

Agar <mark style="color:red;">`padding`</mark> xususiyatida 3 ta qiymat bo'lsa:

* **padding: 25px 50px 75px;**
  * tepa qism paddinggi 25px
  * o'ng va chap tomon paddinggi 50px
  * pastki qism paddinggi 75px

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`padding`</mark> ni 3 ta qiymat bilan birga ishlatish:

```css
p {
  padding: 25px 50px 75px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_padding_shorthand_3val" %}
{% endtab %}
{% endtabs %}

Agar <mark style="color:red;">`padding`</mark> xususiyatida 2 ta qiymat bo'lsa:

* **padding: 25px 50px;**
  * tepa va past ki qsi paddinggi 25px
  * o'ng va chap tomon paddinggi 50px

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`padding`</mark>ni 2 ta qiymat bilan birga ishlatish:

```css
p {
  padding: 25px 50px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_padding_shorthand_2val" %}
{% endtab %}
{% endtabs %}

Agar padding xususiyatida bitta qiymat bo'lsa:

* **padding: 25px;**
  * barcha tomonlardagi padding 25px

{% tabs %}
{% tab title="CSS" %}
<mark style="color:red;">`padding`</mark> qisqartmasini 1 ta qiymat bilan ishlatish:

```css
p {
  padding: 25px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_padding_shorthand_1val" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Padding va element kengligi</mark> <a href="#padding-va-element-kengligi" id="padding-va-element-kengligi"></a>

CSSning <mark style="color:red;">`width`</mark> xususiyati elementning kontent maydonining kengligini belgilaydi. Kontent maydoni - bu elementning padding, border va margin ichidagi qism (quti modeli).

Agar element ma'lum bir kenglikka ega bo'lsa, ushbu elementga qo'shilgan padding elementning umumiy kengligiga qo'shiladi. Bu ko'pincha istalmagan natijani keltirib chiqaradi.

{% tabs %}
{% tab title="CSS" %}
Bu yerda <mark style="color:red;">`<div>`</mark> elementga 300px width berilgan. Lekinelementning haqiqiy kengligi 350px (300px+25px chapki padding + 25px o'ng padding) bo'ladi.

```css
div {
  width: 300px;
  padding: 25px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_padding_width" %}
{% endtab %}
{% endtabs %}

Padding qancha qo'shilishidan qatiy nazar widthni 300px holatida ushlab turish uchun <mark style="color:red;">`box-sizing`</mark> xususiyatidan foydalanish kerak. Bu elementning haqiqiy kengligini saqlab qoladi; Agar  paddingni ko'paytirsangiz, element ichidagi kontentning joyi kamayadi.

{% tabs %}
{% tab title="CSS" %}
Padding qancha qo'shilishidan qatiy nazar widthni 300px holatida ushlab turish uchun box-sizing xususiyatidan foydalanish

```css
div {
  width: 300px;
  padding: 25px;
  box-sizing: border-box;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_padding_width2" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">Ko'proq misollar</mark> <a href="#barcha-css-padding-xususiyatlari" id="barcha-css-padding-xususiyatlari"></a>

[<mark style="color:green;">Chap tomonga padding berish</mark>](https://www.w3schools.com/css/tryit.asp?filename=trycss\_padding-left)\
Ushbu misolda \<p> elementining chap tomoniga padding berish ko'rsatilgan.

[<mark style="color:green;">O'ng tomonga padding berish</mark>](https://www.w3schools.com/css/tryit.asp?filename=trycss\_padding-right)\
Ushbu misolda \<p> elementining o'ng tomoniga padding berish ko'rsatilgan.

[<mark style="color:green;">Tepa qismga padding berish</mark>](https://www.w3schools.com/css/tryit.asp?filename=trycss\_padding-top)\
Ushbu misolda \<p> elementining tepa qismiga padding berish ko'rsatilgan.

[<mark style="color:green;">Pastki qismga padding berish</mark>](https://www.w3schools.com/css/tryit.asp?filename=trycss\_padding-bottom)\
Ushbu misolda \<p> elementining pastki kizmiga padding berish ko'rsatilgan.

### CSSning barcha padding xususiyatlari <a href="#barcha-css-padding-xususiyatlari" id="barcha-css-padding-xususiyatlari"></a>

| Xususiyat                                                                | Ta'rif                                                               |
| ------------------------------------------------------------------------ | -------------------------------------------------------------------- |
| padding                                                                  | paddingning barcha xususiyatlarini bir qatorga yozishga imkon beradi |
| [padding-bottom](https://www.w3schools.com/cssref/pr\_margin-bottom.asp) | Elementning pastki qismiga padding beradi                            |
| [padding-left](https://www.w3schools.com/cssref/pr\_margin-left.asp)     | Elementning chap tomoniga padding beradi                             |
| [padding-right](https://www.w3schools.com/cssref/pr\_margin-right.asp)   | Elementning o'ng tomoniga padding beradi                             |
| [padding-top](https://www.w3schools.com/cssref/pr\_margin-top.asp)       | Elementning tepa qismiga padding beradi                              |
