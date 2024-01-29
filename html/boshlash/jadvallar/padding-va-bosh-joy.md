---
description: >-
  HTML jadvallari kataklar ichidagi paddingni, kataklar orasidagi bo'sh oraliqni
  belgilashi mumkin.
---

# Padding va bo'sh joy

<figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

HTML jadvali - Kataklarni to'ldirish

Katak paddinglari unig chegarasi va ichidagi kontent orasidagi bo'shliqdir.

Standart holda paddingning qiymati 0 bo'ladi.

Jadval kataklariga padding berish uchun CSSning `padding` xususiyatidan foydalaning:

```
th, td {
  padding: 15px;
}
```

Kontentning faqat tepa qismigagina padding berish uchun padding-top xususiyatidan foydalaning.

Qolganlari esa padding-bottom, padding-left va padding-right xususiyatlaridir:

```
th, td {
  padding-top: 10px;
  padding-bottom: 20px;
  padding-left: 30px;
  padding-right: 40px;
}
```

## HTML jadvali - Katak oralig'i

Katak oralig'i har bir katak orasidagi bo'shliqdir.

Standart holda bo'sh joyning qiymati 2px bo'ladi.

Kataklar orasidagi bo'sh joyni o'zgartirish uchun CSSning `border-spacing` xususiyatini table elementiga bering:

```
table {
  border-spacing: 30px;
}
```
