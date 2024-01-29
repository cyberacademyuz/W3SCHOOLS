# CSS Marginlar

Marginlar berilgan chegaralarning tashqarisidagi elementlar atrofida bo'sh joy hosil qilish uchun ishlatiladi.

<figure><img src="../../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

### CSS Marginlar <a href="#css-margin" id="css-margin"></a>

CSSning `margin` xususiyatlari elementlar atrofida, belgilangan chegaraning tashqi qismida bo'sh joy hosil qilish uchun ishlatiladi

CSS yordamida marginlarni boshqara olasiz. Elementning har bir tomoni (tepa, o'ng, pastki va chap) uchun alohida margin berish xususiyatlari mavjud.

### Margin - Alohida tomonlar <a href="#margin-individual-tomonlarda" id="margin-individual-tomonlarda"></a>

CSS elementning har bir tomoniga margin berish uchun bir nechta xususiyatlarga ega:

* margin-top
* margin-right
* margin-bottom
* margin-left

Barcha margin xususiyatlari quyidagi qiymatlarni o'z ichiga oladi:

* auto - marginni brauzerning o'zi hisoblaydi
* uzunlik - margin qiymatlari px, pt, cm, va hokazolar asosida belgilanadi
* % - margin qiymatlarini o'z ichiga olgan elementlarning kengligini % da hisoblaydi
* inherit - ota elementdagi qiymatni meros qilib oladi

**Maslahat:** Negativ qiymatlarga ruxsat beriladi

{% code title="<p> elementining barcha tomoniga turli xil margin o'rnatish:" %}
```
p {
  margin-top: 100px;
  margin-bottom: 100px;
  margin-right: 150px;
  margin-left: 80px;
}
```
{% endcode %}

### Margin - qisqarma xususiyat <a href="#margin-qisqartmasi" id="margin-qisqartmasi"></a>

Marginning barcha xususiyatlarini bitta xususiyat ichida bir qatorda yozish mumkin.

`margin` xususiyati marginning quyidagi xususiyatlarini qisqartirib bera oladi:

* margin-top
* margin-right
* margin-bottom
* margin-left

Ular mana bunday ishlaydi:

Agarda margin xususiyatida 4 ta qiymat bo'lsa:

* **margin: 25px 50px 75px 100px;**
  * tepa qism margini 25px
  * o'ng tomon margini 50px
  * pastki qism margini 75px
  * chap tomon margini 100px

{% code title="margin qisqartmasini 4 ta qiymat bilan ishlatish:" %}
```
p {
  margin: 25px 50px 75px 100px;
}
```
{% endcode %}

Agar `margin` xususiyatida 3 ta qiymat bo'lsa:

* **margin: 25px 50px 75px;**
  * tepa qism margini 25px
  * o'ng va chap tomon margini 50px
  * pastki qism margini 75px

{% code title="margin qisqartmasini 3 ta qiymat bilan ishlatish:" %}
```
p {
  margin: 25px 50px 75px;
}
```
{% endcode %}

Agar `margin` xususiyatida 2 ta qiymat bo'lsa:

* **margin: 25px 50px;**
  * tepa va pastki qism margini 25px
  * o'ng va chap tomon margini 50px

{% code title="margin qisqartmasini 2 ta qiymat bilan ishlatish:" %}
```
p {
  margin: 25px 50px;
}
```
{% endcode %}

Agar `margin` xususiyatida bitta qiymat bo'lsa:

* **margin: 25px;**
  * barcha tomonlardagi margin 25px

{% code title="margin qisqartmasini 1 ta qiymat bilan ishlatish:" %}
```
p {
  margin: 25px;
}
```
{% endcode %}

### Auto qiymati <a href="#auto-qiymati" id="auto-qiymati"></a>

Elementni konteyner ichida gorizontal tarzda o'rtaga olib kelish uchun margin xususiyatini avtomati auto  qilishingiz mumkin.

Keyin element belgilangan kenglikni egallaydi va qolgan bo'sh joy chap va o'ng narginlar orasida teng ravishda bo'linadi.

{% code title="margin: auto; dan foydalanish:" %}
```
div {
  width: 300px;
  margin: auto;
  border: 1px solid red;
}
```
{% endcode %}

### Inherit qiymati <a href="#inherit-qiymati" id="inherit-qiymati"></a>

Bu misoldagi \<p class="ex1"> elementi ota element hisoblangan \<div> elementidan chap tomon marginining qiymatini meros qilib oladi:

{% code title="inherit qiymatidan foydalanish:" %}
```
div {
  border: 1px solid red;
  margin-left: 100px;
}

p.ex1 {
  margin-left: inherit;
}
```
{% endcode %}

### Barcha CSS margin xususiyatlari <a href="#barcha-css-margin-xususiyatlari" id="barcha-css-margin-xususiyatlari"></a>

| Xususiyat                                                               | Ta'rif                                                              |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [margin](https://www.w3schools.com/cssref/pr\_margin.asp)               | Marginning barcha xususiyatlarini bir qatorda yozishga imkon beradi |
| [margin-bottom](https://www.w3schools.com/cssref/pr\_margin-bottom.asp) | Elementning pastki qismiga margin beradi                            |
| [margin-left](https://www.w3schools.com/cssref/pr\_margin-left.asp)     | Elementning chap tomoniga margin beradi                             |
| [margin-right](https://www.w3schools.com/cssref/pr\_margin-right.asp)   | Elementning o'ng tomoniga margin beradi                             |
| [margin-top](https://www.w3schools.com/cssref/pr\_margin-top.asp)       | Elementning tepa qismiga margin beradi                              |
