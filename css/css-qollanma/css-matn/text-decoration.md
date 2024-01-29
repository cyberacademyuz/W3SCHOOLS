# Text decoration

### Matn dekoratsiyasi <a href="#matn-dekoratsiyasi" id="matn-dekoratsiyasi"></a>

Ushbu bo'limda quyidagi xususiyatlar haqida bilib olasiz:

* <mark style="color:red;">`text-decoration-line`</mark>
* <mark style="color:red;">`text-decoration-color`</mark>
* <mark style="color:red;">`text-decoration-style`</mark>
* <mark style="color:red;">`text-decoration-thickness`</mark>
* <mark style="color:red;">`tex-decoration`</mark>

### Matnga dekoratsiya chizig'ini qo'shish <a href="#matnga-dekoratsiya-chizigini-qoshish" id="matnga-dekoratsiya-chizigini-qoshish"></a>

`text-decoration-line` xususiyati matnga dekoratsiya chizig'ini qo'shish uchun ishlatiladi.

**Maslahat:** Ushbu xususiyatda bittadan ortiq qiymat ishlata olasiz, masalan, ham `underline` ham `strike-through` ni bir vaqtda bitta element uchun qo'llashingiz mumkin.

```
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

{% hint style="warning" %}
**Note:** `underline` dekoratsiyasidan foydalanish har doim ham tavsiya qilinmaydi, sababi uni foydalanuvchilar link deb o'ylashligi mumkin.
{% endhint %}

### Matn dekoratsiyasiga rang berish <a href="#matn-dekoratsiyasiga-rang-berish" id="matn-dekoratsiyasiga-rang-berish"></a>

`text-decoration-color` xususiyati matn dekoratsiyasiga rang berish uchun ishlatiladi

```
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

### Matn dekoratsiyasining stilini o'zgartirish <a href="#matn-dekoratsiyasini-stilini-ozgartirish" id="matn-dekoratsiyasini-stilini-ozgartirish"></a>

`text-decoration-style` xususiyati matn dekoratsiyasining stilini o'zgartirish uchun ishlatiladi

```
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

### Matn dekoratsiyasining qalinligini belgilash <a href="#matn-dekoratsiyasini-qalinligini-belgilash" id="matn-dekoratsiyasini-qalinligini-belgilash"></a>

`text-decoration-thickness` orqali dekoratsiyaning qalinligini o'zgartira olasiz.

```
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

### text-decoration qisqartmasi <a href="#text-decoration-qisqartmasi" id="text-decoration-qisqartmasi"></a>

text-decoration qisqartmasi quyidagilarni bir qatorda yozish imkonini beradi:

* `text-decoration-line` (majburiy)
* `text-decoration-color` (ixtiyoriy)
* `text-decoration-style` (ixtiyoriy)
* `text-decoration-thickness` (ixtiyoriy)

```
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

### Kichik maslahat <a href="#kichik-maslahat" id="kichik-maslahat"></a>

HTML-dagi barcha liklarning tagiga standart tarzda pastki chiziqchizilgan bo'lsadi. Ba'zan havolalar tagiga chizilmagan holatda yaratilganligini ko'rasiz. `text-decoration: none;` havolalardan pastki chiziqni olib tashlash uchun ishlatiladi, masalan:

```
a {
  text-decoration: none;
}
```

### CSSning barcha text-decoration xususiyatlari <a href="#barcha-css-text-decoration-xususiyatlari" id="barcha-css-text-decoration-xususiyatlari"></a>

| Xususiyat                                                                                             | Ta'rif                                                                                 |
| ----------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| [text-decoration](https://www.w3schools.com/cssref/pr\_text\_text-decoration.asp)                     | `text-decoration` ning barcha xususiyatlarini bir qatorda yozishga imkon beradi        |
| [text-decoration-color](https://www.w3schools.com/cssref/css3\_pr\_text-decoration-color.asp)         | matn dekoratsiyasining rangini belgilaydi                                              |
| [text-decoration-line](https://www.w3schools.com/cssref/css3\_pr\_text-decoration-line.asp)           | Qanday text-decoration ishlatilishi kerakligini belgilaydi (underline, overline, etc.) |
| [text-decoration-style](https://www.w3schools.com/cssref/css3\_pr\_text-decoration-style.asp)         | Text-decoration ni stilini belgilaydi (solid, dotted, etc.)                            |
| [text-decoration-thickness](https://www.w3schools.com/cssref/pr\_text\_text-decoration-thickness.asp) | Text-decoration ni qalinligini belgilaydi                                              |
