# BS5 Medium

### Medium gridiga misoli

|                        | XSmall  | Small      | Medium     | Large      | Extra Large | XXL         |
| ---------------------- | ------- | ---------- | ---------- | ---------- | ----------- | ----------- |
| **Class qo'shimchasi** | `.col-` | `.col-sm-` | `.col-md-` | `.col-lg-` | `.col-xl-`  | `.col-xxl-` |
| **Ekran kengligi**     | <576px  | >=576px    | >=768px    | >=992px    | >=1200px    | >=1400px    |

Oldingi bo'limda kichik qurilmalar uchun classlar va gridga bo'yicha bir nechta misol keltirdik. Biz ikkita div (ustun) ishlatdik va ularga 25%/75% bo'linish berdik:

```
<div class="col-sm-3">....</div>
<div class="col-sm-9">....</div>
```

Ammo o'rtacha ekranli qurilmalarda dizayn 50%/50% holatida yaxshiroq ko'rinadi.

{% hint style="warning" %}
O'rta ekrali qurilmalar ekranining kengligi 768px-dan 991px-gacha bo'ladi.
{% endhint %}

O'rta ekrali qurilmalar uchun `.col-md-*` classlaridan foydalanamiz:

```
<div class="col-sm-3 col-md-6">....</div>
<div class="col-sm-9 col-md-6">....</div>
```

Endi Bootstrap "kichik o'lchamlarda -sm- bo'lgan classlarga qarang va ulardan foydalaning. O'rta o'lchamda esa -md- bo'lgan classlarga qarang va ulardan foydalaning" deb aytadi.

Quyidagi misol kichik ekranli qurilmalarda elementni 25%/75% va o'rta (katta, xlarge va xxlarge) ekranli qurilmalarda 50%/50% qilib bo'linadi. Juda kichik ekranli qurilmalarda u avtomatik tarzda ustma ust bo'lib joylashadi (100%):

<figure><img src="../../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

```
<div class="container-fluid">
  <div class="row">
    <div class="col-sm-3 col-md-6">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-sm-9 col-md-6">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

{% hint style="warning" %}
**Maslahat:** Sahifadagi ustunlarning umumiy soni 12 ta ekanligiga yoki undan kamligiga ishonch hosil qiling. (barcha 12 ta ustundan foydalanish shart emas).
{% endhint %}

### Faqat mediumdan foydalanish

Quyidagi misolda faqat `.col-md-6` classini (.col-sm-\* holda) beramiz. Bu o'rta, katta, juda katta va XXL ekranli qurilmalarda elementning 50%/50% ko'rinishida bo'linishini bildiradi, chunki class kengayib boradi. Biroq, kichik va juda kichik ekranli qurilmalar uchun u vertikal tarzda joylashadi. (100%):

```
<div class="row">
  <div class="col-md-6">
    <p>Lorem ipsum...</p>
  </div>
  <div class="col-md-6">
    <p>Sed ut perspiciatis...</p>
  </div>
</div>
```

### Avtomatik layot ustunlari

Bootstrap 5 da barcha qurilmalar uchun bir xil kenglikdagi ustunlar yaratishning oson yo‘li mavjud: `.col-md-*`dan raqamni olib tashlash kifoya va `col-md` classidan faqat ma’lum miqdordagi `col` elementlarida foydalaning. Bootstrap o'zi qancha ustun borligini aniqlaydi va har bir ustun bir xil kenglikga ega bo'ladi.

Agar ekran o'lchami **768px** dan kichik bo'lsa, ustunlar gorizontal tarzda joylashadi:

```
code<!-- Two columns: 50% width on medium and up-->
<div class="row">
  <div class="col-md">1 of 2</div>
  <div class="col-md">2 of 2</div>
</div>

<!-- Four columns: 25% width on medium and up -->
<div class="row">
  <div class="col-md">1 of 4</div>
  <div class="col-md">2 of 4</div>
  <div class="col-md">3 of 4</div>
  <div class="col-md">4 of 4</div>
</div>1 / 22 / 2
1/42/43/44 / 4
```

<figure><img src="../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

Keyingi bo'limda katta ekranli qurilmalar uchun boshqacha foiz qanday qo'shilishi ko'rsatilgan.
