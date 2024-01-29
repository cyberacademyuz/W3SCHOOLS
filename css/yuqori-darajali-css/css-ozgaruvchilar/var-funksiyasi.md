# var() funksiyasi

### CSS o'zgaruvchilari

`var()` funktsiyasi CSS o'zgaruvchisining qiymatini berish uchun ishlatiladi.

CSS o'zgaruvchilari DOMga murojaat qilish huquqiga ega, ya'ni lokal yoki global qamrovli o'zgaruvchilar yaratishingiz, JavaScript va media querielar asosida o'zgaruvchilarni o'zgartirishingiz mumkin.

Sayt dizaynining ranglarini belgilashda CSS o'zgaruvchilaridan foydalanish afzal. Bita rangni qayta-qayta foydalanish va joylashtirish o'rniga ularni o'zgaruvchilarga joylashtirishingiz mumkin.

### An'anaviy yo'l

Quyidagi misolda cssda ranglar belgilashning odatiy usuli ko'rsatilgan (har bir alohida element uchun foydalaniladigan ranglarni berish orqali):

```
body { background-color: #1e90ff; }

h2 { border-bottom: 2px solid #1e90ff; }

.container {
  color: #1e90ff;
  background-color: #ffffff;
  padding: 15px;
}

button {
  background-color: #ffffff;
  color: #1e90ff;
  border: 1px solid #1e90ff;
  padding: 5px;
}
```

### var() funksiyasining sintaksisi

`var()` funksiyasi CSS o'zgaruvchisining qiymatini berish uchun ishlatiladi.

`var()` funksiyaning sintaksisi quyidagicha:

```
var(--name, value)
```

| Qiymat  | Ta'rif                                                           |
| ------- | ---------------------------------------------------------------- |
| _name_  | Required. The variable name (must start with two dashes)         |
| _value_ | Optional. The fallback value (used if the variable is not found) |

**Eslatma:** O'zgaruvchining nomi ikkita tire (--) bilan boshlanishi kerak va u katta-kichik harflarga farq qiladi

### var() qanday ishlaydi

CSS o'zgaruvchilari global yoki lokal doiraga ega bo'lishi mumkin.

Global o'zgaruvchilarga butun hujjat bo'ylab murojaat qilish/ishlatish mumkin, lokal o'zgaruvchilar esa faqat e'lon qilingan selektor ichida ishlatilishi mumkin.

Global doiradagi o'zgaruvchi yaratish uchun uni `:root` selektori ichida e'lon qiling. <mark style="color:green;">`:root`</mark> selektori hujjatning ildiz elementiga mos keladi.

Lokal doiraga ega o'zgaruvchi yaratish uchun uni ishlatmoqchi bo'lgan selektoringiz ichida e'lon qiling.

Quyidagi misol yuqoridagi misol bilan bir xil, ammo bu yerda biz `var()` funksiyadan foydalanamiz.

Birinchi navbatda ikkita global o'zgaruvchini e'lon qilamiz (--blue va --white). So'ng, o'zgaruvchilar qiymatidan cssda foydalanish uchun `var()` funksiyasidan foydalanamiz:

```
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

body { background-color: var(--blue); }

h2 { border-bottom: 2px solid var(--blue); }

.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
}

button {
  background-color: var(--white);
  color: var(--blue);
  border: 1px solid var(--blue);
  padding: 5px;
}

```

`var()`dan foydalanishning afzalliklari quyidagilardan iborat:

* kodni o'qishni osonlashtiradi (tushunarliroq bo'ladi)
* rang qiymatlarini o'zgartirishni ancha osonlashtiradi

Blue va white rangini lightblue va white rangiga o'zgartirish uchun ikkita o'zgaruvchining qiymatni o'zgartirishingiz kerak:

```
:root {
  --blue: #6495ed;
  --white: #faf0e6;
}

body { background-color: var(--blue); }

h2 { border-bottom: 2px solid var(--blue); }

.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
}

button {
  background-color: var(--white);
  color: var(--blue);
  border: 1px solid var(--blue);
  padding: 5px;
}
```

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar `var()` funksiyani to'liq qo'llab-quvvatlaydigan brauzerlarnik ilk versiyasini ko'rsatadi.

| Funksiya | Chrome | Edge | Firefox | Safari |      |
| -------- | ------ | ---- | ------- | ------ | ---- |
| var()    | 49.0   | 15.0 | 31.0    | 9.1    | 36.0 |

### CSS var() funktsiyasi

| Xususiyat                                                                                                                               | Ta'rif                              |
| --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| [var()](https://www-w3schools-com.translate.goog/cssref/func\_var.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Inserts the value of a CSS variable |
