# O'zgaruvchilarni override qilish

### Global oʻzgaruvchini lokal oʻzgaruvchi orqali bekor qilish

Oldingi sahifada global o'zgaruvchilarga butun hujjat bo'ylab murojaat qilish/ishlatish mumkinligini bilib oldik, lokal o'zgaruvchilar esa faqat e'lon qilingan selektor ichida ishlatilishi mumkin.

Oldingi sahifadagi misolga qarang:

```
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

body {
  background-color: var(--blue);
}

h2 {
  border-bottom: 2px solid var(--blue);
}

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

Ba'zan o'zgaruvchilarni faqat sahifaning ma'lum bir qismida o'zgartirishni xohlaymiz.

Button elementi uchun boshqacharoq ko'k rang bermoqchimiz deb tasavvur qilaylik. Keyin button selektori ichida `--blue` o'zgaruvchini qayta e'lon qilamiz. Ushbu selektor ichida `var(--blue)` dan foydalansak, u bu yerda e'lon qilingan lokal `--blue` o'zgaruvchisining qiymatidan foydalanadi.

Lokal `--blue` o'zgaruvchisi button elementlari uchun global `--blue` o'zgaruvchini bekor qilishini guvohi bo'lamiz:

```
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

body {
  background-color: var(--blue);
}

h2 {
  border-bottom: 2px solid var(--blue);
}

.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
}

button {
  --blue: #0000ff; /* local variable will override global */
  background-color: var(--white);
  color: var(--blue);
  border: 1px solid var(--blue);
  padding: 5px;
}
```

### Yangi loksl o'zgaruvchi qo'shish

Agar o'zgaruvchi faqat bitta joyda ishlatilishi kerak bo'lsa, yangi lokal o'zgaruvchi ham e'lon qilishimiz mumkin edi, masalan:

```
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

body {
  background-color: var(--blue);
}

h2 {
  border-bottom: 2px solid var(--blue);
}

.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
}

button {
  --button-blue: #0000ff; /* new local variable */
  background-color: var(--white);
  color: var(--button-blue);
  border: 1px solid var(--button-blue);
  padding: 5px;
}
```

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar `var()` funksiyani to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Function | Chrome |      |      |     |      |
| -------- | ------ | ---- | ---- | --- | ---- |
| var()    | 49.0   | 15.0 | 31.0 | 9.1 | 36.0 |

### CSS var() funksiyasi

| Xususiyat                                                                                                                               | Ta'rif                              |
| --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| [var()](https://www-w3schools-com.translate.goog/cssref/func\_var.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Inserts the value of a CSS variable |
