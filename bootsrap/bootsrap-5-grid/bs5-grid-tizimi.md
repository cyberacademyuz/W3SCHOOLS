# BS5 Grid tizimi

### Grid tizimi

Bootstrapning grid tizimi flexbox bilan qurilgan va sahifa bo'ylab 12 tagacha ustun kiritishga ruxsat beradi.

Agar 12 ta ustundan alohida foydalanishni xohlamasangiz, kattaroq ustunlar yaratish uchun ustunlarni birga guruhlashingiz mumkin:

<figure><img src="../../.gitbook/assets/image (560).png" alt=""><figcaption></figcaption></figure>

Grid tizimi moslashuvchan va ustunlar ekran o'lchamiga qarab avtomatik tarzda qayta joylashadi.

Sahifadagi ustunlarning umumiy soni 12 ta ekanligiga yoki undan kamligiga ishonch hosil qiling. (barcha 12 ta ustundan foydalanish shart emas).

### Grid classlari

Bootstrap 5 grid tizimida oltita class bor:

* `.col-` (qo'shimcha kichik qurilmalar - ekran kengligi 576px dan kichikina)
* `.col-sm-` (kichkina qurilmalar - ekran kengligi 576 pikselga teng yoki undan katta)
* `.col-md-` (o'rtacha qurilmalar - ekran kengligi 768 pikselga teng yoki undan katta)
* `.col-lg-` (katta qurilmalar - ekran kengligi 992 pikselga teng yoki undan katta)
* `.col-xl-` (xlarge qurilmalar - ekran kengligi 1200px ga teng yoki undan katta)
* `.col-xxl-` (xxlarge qurilmalari - ekran kengligi 1400px ga teng yoki undan katta)

Yuqoridagi classlar yanada dinamik va moslashuvchan tartiblarni yaratishi uchun birlashtirilishi mumkin.

**Maslahat:** Har bir class kattalashadi, shuning uchun `sm` va `md` uchun bir xil width bermoqchi bo'lsangiz, faqat `sm`ni belgilashingiz kerak.

### Bootstrap 5 gridining asosiy tuzilishi

Quyida Bootstrap 5 gridining asosiy tuzilishi keltirilgan:

```
<!-- Control the column width, and how they should appear on different devices -->
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>

<!-- Or let Bootstrap automatically handle the layout -->
<div class="row">
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
</div>
```

Birinchi misol: qator yarating( `<div class="row">`). Keyin, kerakli miqdorda ustunlar qo'shing (`.col-*-*`classlariga ega teglar bilan). Birinchi yulduz (\*) moslashuvchanlikni bildiradi: sm, md, lg, xl yoki xxl, ikkinchi yulduz esa har bir qator uchun 12 tagacha qo'shilishi kerak bo'lgan raqamni bildiradi.

Ikkinchi misol: har bir `col`ga raqam berish o'rniga, bir hil kenglikdagi ustunlar yaratish uchun bootstrapga joylashuvni boshqarishga ruxsat bering: ikkita "col" elementida = har bir `col` uchun 50% width, uchta "col"da esa har bir `col` uchun 33,33% width. To'rtta "col"da  25% width va hkz. Ustunlarni moslashuvchan qilish uchun `.col-sm|md|lg|xl|xxl`dan ham foydalanishingiz mumkin.

### Grid imkoniyatlari

Quyidagi jadvalda Bootstrap 5 grid tizimining turli ekran o'lchamlarida qanday ishlashi ko'rsatilgan:

|                           | Juda kichik (<576px)                       | Kichik (>=576px)                                                                                   | O'rtacha(>=768px)                                                                                  | Katta (>=992px)                                                                                    | Juda katta (>=1200px)                                                                              | XXL (>=1400px)                                                                                     |
| ------------------------- | ------------------------------------------ | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Class qo'shimchasi**    | `.col-`                                    | `.col-sm-`                                                                                         | `.col-md-`                                                                                         | `.col-lg-`                                                                                         | `.col-xl-`                                                                                         | `.col-xxl-`                                                                                        |
| Grid harakati             | Har doim gorizontal                        | Yonma yon turishdan boshlanadi, agar ekran kichiklik qilsa breakpoint qismdan ustma ust joylashadi | Yonma yon turishdan boshlanadi, agar ekran kichiklik qilsa breakpoint qismdan ustma ust joylashadi | Yonma yon turishdan boshlanadi, agar ekran kichiklik qilsa breakpoint qismdan ustma ust joylashadi | Yonma yon turishdan boshlanadi, agar ekran kichiklik qilsa breakpoint qismdan ustma ust joylashadi | Yonma yon turishdan boshlanadi, agar ekran kichiklik qilsa breakpoint qismdan ustma ust joylashadi |
| Konteyner uzunligi        | Mavjud emas (auto)                         | 540px                                                                                              | 720px                                                                                              | 960px                                                                                              | 1140px                                                                                             | 1320px                                                                                             |
| ... uchun mos             | Tugmali telefonlar                         | Sensor ekranalr                                                                                    | Planshetlar                                                                                        | Notebooklar                                                                                        | Notebooklar va PC-lar                                                                              | Notebooklar va PC-lar                                                                              |
| **Ustunlar soni**         | 12                                         | 12                                                                                                 | 12                                                                                                 | 12                                                                                                 | 12                                                                                                 | 12                                                                                                 |
|                           | 1.5rem (Ustunning har bir tomonida .75rem) | 1.5rem (Ustunning har bir tomonida .75rem)                                                         | 1.5rem (Ustunning har bir tomonida .75rem)                                                         | 1.5rem (Ustunning har bir tomonida .75rem)                                                         | 1.5rem (Ustunning har bir tomonida .75rem)                                                         | 1.5rem (Ustunning har bir tomonida .75rem)                                                         |
| **Nestable**              | Ha                                         | Ha                                                                                                 | Ha                                                                                                 | Ha                                                                                                 | Ha                                                                                                 | Ha                                                                                                 |
| **Offsetlar**             | Ha                                         | Ha                                                                                                 | Ha                                                                                                 | Ha                                                                                                 | Ha                                                                                                 | Ha                                                                                                 |
| **Ustunlarni tartiblash** | **Ha**                                     | **Ha**                                                                                             | **Ha**                                                                                             | **Ha**                                                                                             | **Ha**                                                                                             | **Ha**                                                                                             |
