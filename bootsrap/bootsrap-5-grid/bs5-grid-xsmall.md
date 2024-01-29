# BS5 Grid XSmall

### Juda kichik gridga misol

|                        | XSmall  | Small      | Medium     | Large      | Extra Large | XXL         |
| ---------------------- | ------- | ---------- | ---------- | ---------- | ----------- | ----------- |
| **Class qo'shimchasi** | `.col-` | `.col-sm-` | `.col-md-` | `.col-lg-` | `.col-xl-`  | `.col-xxl-` |
| **Ekran kengligi**     | <576px  | >=576px    | >=768px    | >=992px    | >=1200px    | >=1400px    |

Faraz qilaylik, bizda ikkita ustunli oddiy layout bor va ushbu ikki ustunni barcha qurilmalar uchun 25%/75% qilmoqchimiz

Ikkala ustunga quyidagi classlarni qo'shamiz:

```
<div class="col-3">....</div>
<div class="col-9">....</div>
```

Quyidagi misol barcha qurilmalarda (juda kichik, kichik, o'rta, katta, xlarge va xxlarge) 25%/75% bo'linishiga olib keladi.

<figure><img src="../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

```
<div class="container-fluid">
  <div class="row">
    <div class="col-3 bg-primary">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-9 bg-dark">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

{% hint style="warning" %}
**Maslahat:** Sahifadagi ustunlarning umumiy soni 12 ta ekanligiga yoki undan kamligiga ishonch hosil qiling. (barcha 12 ta ustundan foydalanish shart emas).
{% endhint %}

33,3%/66,6% bo‘linish uchun `.col-4` va `.col-8` dan foydalanishingiz kerak (50%/50% bo‘linish uchun esa `.col-6` va `.col-6` dan foydalanasiz):

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

```
<!-- 33.3%/66.6% split -->
<div class="container-fluid">
  <div class="row">
    <div class="col-4 bg-primary">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-8 bg-dark">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>

<!-- 50%/50% split -->
<div class="container-fluid">
  <div class="row">
    <div class="col-6 bg-primary">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-6 bg-dark">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

### Avtomatik layout ustunlari

Bootstrap 5 da barcha qurilmalar uchun bir xil kenglikdagi ustunlar yaratishning oson yo‘li mavjud: `.col-*`dan raqamni olib tashlash kifoya va `col` classidan faqat ma’lum miqdordagi `col` elementlarida foydalaning. Bootstrap o'zi qancha ustun borligini aniqlaydi va har bir ustun bir xil kenglikga ega bo'ladi.

```
<!-- Two columns: 50% width-->
<div class="row">
  <div class="col">1 of 2</div>
  <div class="col">2 of 2</div>
</div>

<!-- Four columns: 25% width-->
<div class="row">
  <div class="col">1 of 4</div>
  <div class="col">2 of 4</div>
  <div class="col">3 of 4</div>
  <div class="col">4 of 4</div>
</div>
```
