# CSS Counterlar

<figure><img src="../../.gitbook/assets/image (801).png" alt=""><figcaption></figcaption></figure>

CSS hisoblagichlari CSS tomonidan qo'llab-quvvatlanadigan "o'zgaruvchilar" bo'lib, ularning qiymatlari CSS qoidalari orqali oshirilishi mumkin (ularning necha marta ishlatilishini kuzatish uchun). Hisoblagichlar hujjatdagi joylashuviga qarab kontentning ko'rinishini sozlash imkonini beradi.

### Hisoblagichlar yordamida avtomatik raqamlash <a href="#hisoblagichlar-yordamida-avtomatik-raqamlash" id="hisoblagichlar-yordamida-avtomatik-raqamlash"></a>

CSS hisoblagichlari CSS tomonidan qo'llab-quvvatlanadigan "o'zgaruvchilar" bo'lib, ularning qiymatlari CSS qoidalari yordamida oshirilishi mumkin (ularning necha marta ishlatilishini kuzatish uchun).

CSS hisoblagichlari bilan ishlash uchun quyidagi xususiyatlardan foydalanamiz:

* `counter-reset` - hisoblagich yaratadi yoki qayta sozlaydi
* `counter-increment` - hisoblagichdagi qiymatni oshiradi
* `content` - yaratilgan kontentni qo'shadi
* `counter()` yoki `counters()` funksiyasi - hisoblagichning qiymatlarini elementga qo'shadi

CSSning hisoblagichidan foydalanish uchun birinchi bo'lib `counter-reset` yaratilgan bo'lishi kerak.

Quyidagi misolda sahifa uchun hisoblagich yaratiladi (body ichida), keyin har bir `<h2>` elementi uchun hisoblagich qiymati oshiriladi va "Section `<hisoblagich qiymati>`:" har bir `<h2>` elementning boshiga yoziladi:

```
body {
  counter-reset: section;
}

h2::before {
  counter-increment: section;
  content: "Section " counter(section) ": ";
} 
```

### Ichma ich hisoblagichlar <a href="#nesting-counters" id="nesting-counters"></a>

Quyidagi misolda sahifa uchun bitta (section) va har bir `<h1>` uchun ham bitta hisoblagich yaratiladi (subsection). "Section" hisoblagichi har bir `<h1>` elementni "Section `<value of the section counter>.`" ko'rininishida hisoblaydi va "subsection" hisoblagichi esa har bir `<h2>` elementini "`<value of the section counter>.<value of the subsection counter>`" ko'rinishida hisoblaydi.

```
body {
  counter-reset: section;
}

h1 {
  counter-reset: subsection;
}

h1::before {
  counter-increment: section;
  content: "Section " counter(section) ". ";
}

h2::before {
  counter-increment: subsection;
  content: counter(section) "." counter(subsection) " ";
}
```

Hisoblagichlar tartiblangan ro'yxatlar yaratish uchun ham foyda berishi mumkin, chunki hisoblagichning yangi namunasi avtomatik tarzda bola elementlarda yaratiladi. Bu yerda turli darajadagi ichma ichma hisoblagichlar orasiga string kiritish uchun `counters()` funksiyasidan foydalandik:

```
ol {
  counter-reset: section;
  list-style-type: none;
}

li::before {
  counter-increment: section;
  content: counters(section,".") " ";
}
```

### CSSning Counter xususiyatlari <a href="#css-hisoblagich-xususiyatlari" id="css-hisoblagich-xususiyatlari"></a>

| Xususiyat                                                                            | Ta'rif                                                                                |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| [content](https://www.w3schools.com/cssref/pr\_gen\_content.asp)                     | Kontent qo'shish uchun ::before va ::after psevdo-elementlari bilan birga ishlatiladi |
| [counter-increment](https://www.w3schools.com/cssref/pr\_gen\_counter-increment.asp) | Bitta yoki undan ortiq hisoblagich qiymatlarini oshiradi                              |
| [counter-reset](https://www.w3schools.com/cssref/pr\_gen\_counter-reset.asp)         | Yangitdan yoki qaytadan hisoblagichlarni yaratadi                                     |
| [counter()](https://www.w3schools.com/cssref/func\_counter.asp)                      | Olib kelingan hisoblagichning qiymatini qaytaradi                                     |
