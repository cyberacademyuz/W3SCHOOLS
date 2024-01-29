# BS5 Large

### Katta gridga misoli

|                        | XSmall  | Small      | Medium     | Large      | Extra Large | XXL         |
| ---------------------- | ------- | ---------- | ---------- | ---------- | ----------- | ----------- |
| **Class qo'shimchasi** | `.col-` | `.col-sm-` | `.col-md-` | `.col-lg-` | `.col-xl-`  | `.col-xxl-` |
| **Ekran kengligi**     | <576px  | >=576px    | >=768px    | >=992px    | >=1200px    | >=1400px    |

Oldingi bo'limda kichik va o'rta ekranli qurilmalar uchun classlar bilan grid bo'yicha bir nechta misol keltirdik. Biz ikkita div (ustun) ishlatdik va ularga kichik qurilmalarda 25%/75%, oʻrtacha ekranli qurilmalarda esa 50%/50% boʻlinish berdik:

Oldingi bo'limda kichik qurilmalar uchun classlar va grid bo'yicha bir nechta misol keltirdik. Biz ikkita div (ustun) ishlatdik va ularga 25%/75% bo'linish berdik:

```
<div class="col-sm-3 col-md-6">....</div>
<div class="col-sm-9 col-md-6">....</div>
```

Ammo katta ekranli qurilmalarda dizayn 33%/66%  holatida yaxshiroq ko'rinadi.

{% hint style="warning" %}
Katta ekrali qurilmalar ekranining kengligi 992px-dan 1199px-gacha bo'ladi.
{% endhint %}

Katta ekranli qurilmalar uchun `.col-lg-*` classlaridan foydalanamiz:

```
<div class="col-sm-3 col-md-6 col-lg-4">....</div>
<div class="col-sm-9 col-md-6 col-lg-8">....</div>
```

Endi Bootstrap "kichik o'lchamlarda -sm- bo'lgan classlarga qarang va ulardan foydalaning. O'rta o'lchamda esa -md- bo'lgan classlarga qarang va ulardan foydalaning. Katta o'lchamda -lg- bo'lgan classlarga qarang va foydalaning" deb aytadi.

Quyidagi misol kichik ekranli qurilmalarda dizaynni 25%/75% va o'rta ekranli qurilmalarda 50%/50%,  katta, xlarge va xxlarge ekranli qurilmalarda 33%/66% qilib bo'linadi. Juda kichik ekranli qurilmalarda u avtomatik tarzda ustma ust bo'lib joylashadi (100%):

```
.col-sm-3 .col-md-6 .col-lg-4.col-sm-9 .col-md-6 .col-lg-8
```

```
<div class="container-fluid">
  <div class="row">
    <div class="col-sm-3 col-md-6 col-lg-4">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-sm-9 col-md-6 col-lg-8">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

{% hint style="warning" %}
**Maslahat:** Sahifadagi ustunlarning umumiy soni 12 ta ekanligiga yoki undan kamligiga ishonch hosil qiling. (barcha 12 ta ustundan foydalanish shart emas).
{% endhint %}

### Faqat large-dan foydalanish

Quyidagi misolda faqat `.col-lg-6` classini (`.col-md-*` yoki  `.col-sm-*` siz) beramiz. Bu katta, juda katta va XXL ekranli qurilmalarda elementning 50%/50% ko'rinishida bo'linishini bildiradi. Biroq, kichik va juda kichik ekranli qurilmalar uchun u vertikal tarzda joylashadi. (100%):

```
<div class="container-fluid">
  <div class="row">
    <div class="col-lg-6">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-lg-6">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

### Avtomatik layout ustunlari

Bootstrap 5 da barcha qurilmalar uchun bir xil kenglikdagi ustunlar yaratishning oson yo‘li mavjud: `.col-lg-*`dan raqamni olib tashlash kifoya va `col-lg` classidan faqat ma’lum miqdordagi `col` elementlarida foydalaning. Bootstrap o'zi qancha ustun borligini aniqlaydi va har bir ustun bir xil kenglikga ega bo'ladi.

Agar ekran o'lchami **992px** dan kichik bo'lsa , ustunlar gorizontal tarzda joylashadi:

```
<!-- Two columns: 50% width on large and up-->
<div class="row">
  <div class="col-lg">1 of 2</div>
  <div class="col-lg">2 of 2</div>
</div>

<!-- Four columns: 25% width on large and up -->
<div class="row">
  <div class="col-lg">1 of 4</div>
  <div class="col-lg">2 of 4</div>
  <div class="col-lg">3 of 4</div>
  <div class="col-lg">4 of 4</div>
</div>
```
