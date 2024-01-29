# CSS Padding

Padding berilgan chegaraning ichqi qismidagi elementlar kontenti atrofida bo'sh joy hosil qilish uchun beriladi.

<figure><img src="../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

## CSS Padding <a href="#css-padding" id="css-padding"></a>

CSSning `padding` xususiyati berilgan chegaraning ichqi qismidagi elementlar kontenti atrofida bo'sh joy hosil qilish uchun beriladi.

CSS yordamida paddingni boshqara olasiz. Elementning har bir tomoni (tepa, o'ng, pastki va chap) uchun alohida padding berish xususiyatlari mavjud.

### Padding - Alohida tomonlar <a href="#padding-individual-tomonlarda" id="padding-individual-tomonlarda"></a>

CSS elementning har bir tomoniga padding berish uchun bir nechta xususiyatlarga ega

* padding-top
* padding-right
* padding-bottom
* padding-left

Barcha padding xususiyatlari quyidagi qiymatlarni o'z ichiga oladi:

* uzunlik - padding qiymatlari px, pt, cm, va hokazolar asosida belgilanadi
* % - padding qiymatlarini o'z ichiga olgan elementlarning kengligini % da hisoblaydi
* inherit - ota elementdagi qiymatni meros qilib oladi

**Maslahat:** Negativ qiymatlarga ruxsat beriladi

{% code title="<p> elementning barcha tomonlari uchun turli xil padding berish:" %}
```
p {
  padding-top: 100px;
  padding-bottom: 100px;
  padding-right: 150px;
  padding-left: 80px;
}
```
{% endcode %}

### Padding qisqartmasi <a href="#padding-qisqartmasi" id="padding-qisqartmasi"></a>

Paddingning barcha xususiyatlarini bitta xususiyat ichida bir qatorda yozish mumkin.

`padding` xususiyati quyidagi padding xususiyatlarini qisqartirib bera oladi:

* padding-top
* padding-right
* padding-bottom
* padding-left

Ular mana bunday ishlaydi:

Agarda padding xususiyatida 4 ta qiymat bo'lsa:

* **padding: 25px 50px 75px 100px;**
  * tepa qism paddinggi 25px
  * o'ng tomon paddinggi 50px
  * pastki qism paddinggi 75px
  * chap tomon paddinggi 100px

{% code title="padding qisqartmasini 4 ta qiymat bilan ishlatish:" %}
```
p {
  padding: 25px 50px 75px 100px;
}
```
{% endcode %}

Agar padding xususiyatida 3 ta qiymat bo'lsa:

* **padding: 25px 50px 75px;**
  * tepa qism paddinggi 25px
  * o'ng va chap tomon paddinggi 50px
  * pastki qism paddinggi 75px

{% code title="padding qisqartmasini 3 ta qiymat bilan ishlatish:" %}
```
p {
  padding: 25px 50px 75px;
}
```
{% endcode %}

Agar padding xususiyatida 2 ta qiymat bo'lsa:

* **padding: 25px 50px;**
  * tepa va past ki qsi paddinggi 25px
  * o'ng va chap tomon paddinggi 50px

{% code title="padding qisqartmasini 2 ta qiymat bilan ishlatish:" %}
```
p {
  padding: 25px 50px;
}
```
{% endcode %}

Agar padding xususiyatida bitta qiymat bo'lsa:

* **padding: 25px;**
  * barcha tomonlardagi padding 25px

{% code title="padding qisqartmasini 1 ta qiymat bilan ishlatish:" %}
```
p {
  padding: 25px;
}
```
{% endcode %}

### Padding va element kengligi <a href="#padding-va-element-kengligi" id="padding-va-element-kengligi"></a>

CSSning `width` xususiyati elementning kontent maydonining kengligini belgilaydi. Kontent maydoni - bu elementning padding, border va margin ichidagi qism (quti modeli).

Agar element ma'lum bir kenglikka ega bo'lsa, ushbu elementga qo'shilgan padding elementning umumiy kengligiga qo'shiladi. Bu ko'pincha istalmagan natijani keltirib chiqaradi.

{% code title="Bu yerda <div> elementga 300px width berilgan. Lekin <div> elementning haqiqiy kengligi 350px (300px+25px chapki padding + 25px o'ng padding) bo'ladi." %}
```
div {
  width: 300px;
  padding: 25px;
}
```
{% endcode %}

Padding qancha qo'shilishidan qatiy nazar widthni 300px holatida ushlab turish uchun `box-sizing` xususiyatidan foydalanish kerak. Bu elementning haqiqiy kengligini saqlab qoladi; Agar  paddingni ko'paytirsangiz, element ichidagi kontentning joyi kamayadi.

{% code title="Padding qancha qo'shilishidan qatiy nazar widthni 300px holatida ushlab turish uchun box-sizing xususiyatidan foydalanish" %}
```
div {
  width: 300px;
  padding: 25px;
  box-sizing: border-box;
}
```
{% endcode %}

### Ko'proq misollar <a href="#barcha-css-padding-xususiyatlari" id="barcha-css-padding-xususiyatlari"></a>

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
