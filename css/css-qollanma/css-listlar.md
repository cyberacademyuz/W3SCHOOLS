# CSS Listlar

<figure><img src="../../.gitbook/assets/image (507).png" alt=""><figcaption></figcaption></figure>

### HTML Listlar va CSS xususiyatlari <a href="#html-listlar-va-css-xususiyatlari" id="html-listlar-va-css-xususiyatlari"></a>

HTMLda ikki xil asosiy ro'yhat turi bor:

* tartiblangan ro'yhat (`<ol>`) - Ro'yhatdagi qiymatlar raqamlar yoki harflar bilan belgilanadi.
* tartiblanmagan ro'yhat (`<ul>`) - Ro'yhatdagi qiymatlar kichkina qora belgi bilan belgilangan bo'ladi

CSSning ro'yhat xususiyatlari quyidagilarni amalga oshirish imkonini beradi:

* Tartiblangan ro'yhatlar uchun turli xil ro'yxat element belgilarini o'rnatish
* Tartiblanmagan ro'yhatlar uchun turli xil ro'yxat element belgilarini o'rnatish
* Ro'yxat element belgilari sifatida rasm belgilash
* Ro'yhat va ro'yhatdagi qiymatlar uchun bacground rang berish

### Turli xil ro'yhat element belgilarida <a href="#har-xil-markerlardan-foydalanish" id="har-xil-markerlardan-foydalanish"></a>

`list-style-type` xususiyati ro'yhat element belgilarining ko'rinishini o'zgartiradi.

Quyidagi misolda ro'yhat element belgilarining ba'zilari ko'rsatilgan:

```
ul.a {
  list-style-type: circle;
}

ul.b {
  list-style-type: square;
}

ol.c {
  list-style-type: upper-roman;
}

ol.d {
  list-style-type: lower-alpha;
}
```

**Note:** Ushbu qiymatlarning ba'zilari tartiblangan, ba'zilari esa tartiblanmagan ro'yhatlar uchun

### Ro'yhat elementining belgisi sifatida rasm <a href="#rasmni-list-markeri-sifatida-ishlatish" id="rasmni-list-markeri-sifatida-ishlatish"></a>

`list-style-image` xususiyati rasmni ro'yhat elementining belgisi sifatida foydalanish imkonini beradi

```
ul {
  list-style-image: url('sqpurple.gif');
}
```

### Ro'yhat element belgisining joylashuvini o'zgartirish <a href="#list-markerlarning-joylashuvini-ozgartirish" id="list-markerlarning-joylashuvini-ozgartirish"></a>

`list-style-position` xususiyati ro'yhat element belgisining joylashuvini belgilaydi

"`list-style-position: outside;`" ro'yhat elementining belgilarini ro'yhatdan tashqarida turishini anglatadi. Ro'yhat elementidagi har bir qatorining boshi vertikal tarzda joylashadi. Bu standart:

![](<../../.gitbook/assets/image (469).png>)

"`list-style-position: inside;`" belgilarini ro'yhatning ichida turishini anglatadi. ro'yhat elementining belgilari endi matnning bir qismi bo'lgani uchun u matnning boshida turadi va matn biroz suriladi:

![](<../../.gitbook/assets/image (503).png>)

```
ul.a {
  list-style-position: outside;
}

ul.b {
  list-style-position: inside;
}
```

### Standart qoidalarni olib tashlash <a href="#standart-qoidalarni-olib-tashlash" id="standart-qoidalarni-olib-tashlash"></a>

`list-style-type:none` xususiyati belgilarni olib tashlash uchun kerak bo'ladi. Bundan tashqari, ro'yhatning o'zini **margin** va **padding** qiymatlari borligini eslab qoling. Ularni olib tashlash uchun `margin: 0;` va `padding: 0;` xususiyatlarini `<ul>`, `<ol>` ga berish kerak.

```
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
```

### List qisqartmasi <a href="#list-qisqartmasi" id="list-qisqartmasi"></a>

`list-style` xususiyati qisqartma shakldagi xususiyat hisoblanib, ro'yhatning barcha xususiyatlarini bir qatorda yozish imkonini beradi.

```
ul {
  list-style: square inside url("sqpurple.gif");
}
```

`list-style` xususiyatidan foydalanayotganda xususiyat qiymatlarini bir tartibda joylashtirish kerak:

* `list-style-type` (agar `list-style-image` berilgan bo'lsayu, ammo biror sababga ko'ra rasmni ko'rsatib bo'lmasa, ushbu xususiyatning qiymati ko'rsatiladi)
* `list-style-position` (Ro'yhat elementining belgilarini kontent ichida yoki tashqarida bo'lishini belgilaydi)
* `list-style-image` (rasmni ro'yhat elementining belgisi sifatida belgilaydi)

Agarda yuqoridagi qiymatlardan biri berilmasa, standart qiymat olinadi.

## Ro'yhatga ranglar bilan stil berish <a href="#listga-ranglar-bilan-stil-berish" id="listga-ranglar-bilan-stil-berish"></a>

Ro'yhatlarni yanada qiziqarliroq bo'lishi uchun ularga ranglar bilan ham stil bera olamiz.

`<ol>` yoki `<ul>` tegiga qo'shilgan har qanday narsa butun ro'yxatga ta'sir qiladi, `<li>` tegiga qo'shilgan xususiyatlar esa alohida ro'yxat elementlariga ta'sir qiladi:

```
ol {
  background: #ff9999;
  padding: 20px;
}

ul {
  background: #3399ff;
  padding: 20px;
}

ol li {
  background: #ffe5e5;
  color: darkred;
  padding: 5px;
  margin-left: 35px;
}

ul li {
  background: #cce5ff;
  color: darkblue;
  margin: 5px;
}
```

<figure><img src="../../.gitbook/assets/image (523).png" alt=""><figcaption></figcaption></figure>

## Ko'proq misollar

<mark style="color:green;">Chap tomonda qizil chegarali ro'yxat</mark>\
Ushbu misolda chap tomonida qizil rangli chegaraga ega ro'yhat tuzish ko'rsatilgan.

<mark style="color:green;">To'liq uzunlikdagi chegarali ro'yxat</mark>\
Ushbu misolda belgilarsiz chegarali ro'yhat yaratish ko'rsatilgan.

<mark style="color:green;">Ro'yxatlar uchun barcha turli xil list-item belgilari</mark>\
Ushbu misolda CSS-dagi turli xil ro'yxat elementlarining barchasi ko'rsatilgan.

### CSSning barcha ro'yhat xususiyatlari <a href="#barcha-css-list-xususiyatlari" id="barcha-css-list-xususiyatlari"></a>

| Xususiyat                                                                           | Ta'rif                                              |
| ----------------------------------------------------------------------------------- | --------------------------------------------------- |
| [list-style](https://www.w3schools.com/cssref/pr\_list-style.asp)                   | Barcha xususiyatlarni bitta deklaratsiyaga jamlaydi |
| [list-style-image](https://www.w3schools.com/cssref/pr\_list-style-image.asp)       | list markeriga rasm qo'yib beradi                   |
| [list-style-position](https://www.w3schools.com/cssref/pr\_list-style-position.asp) | Markerlar qayerda turishini belgilaydi              |
| [list-style-type](https://www.w3schools.com/cssref/pr\_list-style-type.asp)         | Markerning turini belgilaydi                        |
