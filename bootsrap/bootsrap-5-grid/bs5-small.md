# BS5 Small

### &#x20;Kichik gridga misol

|                        | XSmall  | Small      | Medium     | Large      | Extra Large | XXL         |
| ---------------------- | ------- | ---------- | ---------- | ---------- | ----------- | ----------- |
| **Class qo'shimchasi** | `.col-` | `.col-sm-` | `.col-md-` | `.col-lg-` | `.col-xl-`  | `.col-xxl-` |
| **Ekran kengligi**     | <576px  | >=576px    | >=768px    | >=992px    | >=1200px    | >=1400px    |

Faraz qilaylik, bizda ikkita ustunli oddiy layout bor va ushbu ikki ustunni barcha qurilmalar uchun 25%/75% qilmoqchimiz

{% hint style="warning" %}
Kichik qurilmalarninj ekran kengligi **576px**-dan **767px**-gacha bo'ladi.
{% endhint %}

Kichik qurilmalar uchun `.col-sm-*` classlaridan foydalanamiz.

Ikki ustunimizga quyidagi sinflarni qo'shamiz:

```
<div class="col-sm-3">....</div>
<div class="col-sm-9">....</div>
```

Quyidagi misol kichik (va o'rta, katta, xlarge va xxlarge) qurilmalarda 25%/75% bo'linishiga olib keladi. Juda kichik qurilmalarda u avtomatik tazda ustama ust joylashadi. (100%):

<figure><img src="../../.gitbook/assets/image (649).png" alt=""><figcaption></figcaption></figure>

```
<div class="container-fluid">
  <div class="row">
    <div class="col-sm-3 bg-primary">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-sm-9 bg-dark">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

{% hint style="warning" %}
**Maslahat:** Sahifadagi ustunlarning umumiy soni 12 ta ekanligiga yoki undan kamligiga ishonch hosil qiling. (barcha 12 ta ustundan foydalanish shart emas).
{% endhint %}

33,3%/66,6% bo‘linish uchun `.col-sm-4` va `.col-sm-8` dan foydalanishingiz kerak (50%/50% bo‘linish uchun esa `.col-sm-6` va `.col-6` dan foydalanasiz):

<figure><img src="../../.gitbook/assets/image (254).png" alt=""><figcaption></figcaption></figure>

```
<!-- 33.3/66.6% split: -->
<div class="container-fluid">
  <div class="row">
    <div class="col-sm-4 bg-primary">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-sm-8 bg-dark">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>

<!-- 50%/50% split: -->
<div class="container-fluid">
  <div class="row">
    <div class="col-sm-6 bg-primary">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-sm-6 bg-dark">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

### Avtomatik layot ustunlari

Bootstrap 5 da barcha qurilmalar uchun bir xil kenglikdagi ustunlar yaratishning oson yo‘li mavjud: `.col-sm-*`dan raqamni olib tashlash kifoya va `col-sm` classidan faqat ma’lum miqdordagi `col` elementlarida foydalaning. Bootstrap o'zi qancha ustun borligini aniqlaydi va har bir ustun bir xil kenglikga ega bo'ladi.

Agar ekran o'lchami **576px** dan kichkina bo'lsa, ustunlar gorizontal tarzda joylashadi:

```
<!-- Two columns: 50% width on all screens, except for extra small (100% width) -->
<div class="row">
  <div class="col-sm">1 of 2</div>
  <div class="col-sm">2 of 2</div>
</div>

<!-- Four columns: 25% width on all screens, except for extra small (100% width)-->
<div class="row">
  <div class="col-sm">1 of 4</div>
  <div class="col-sm">2 of 4</div>
  <div class="col-sm">3 of 4</div>
  <div class="col-sm">4 of 4</div>
</div>
```

Keyingi bo'limda o'rtacha ekranli qurilmalar uchun boshqacha foiz qanday qo'shilishi ko'rsatilgan.
