# BS5 XLarge

### Extra Large Grid misoli

|                        | XSmall  | Small      | Medium     | Large      | Extra Large | XXL         |
| ---------------------- | ------- | ---------- | ---------- | ---------- | ----------- | ----------- |
| **Class qo'shimchasi** | `.col-` | `.col-sm-` | `.col-md-` | `.col-lg-` | `.col-xl-`  | `.col-xxl-` |
| **Ekran kengligi**     | <576px  | >=576px    | >=768px    | >=992px    | >=1200px    | >=1400px    |

Oldingi bo'limda kichik, o'rta va katta ekranli qurilmalar uchun classlar bilan grid bo'yicha bir nechta misol keltirdik. Biz ikkita div (ustun) ishlatdik va ularga kichik qurilmalarda 25%/75%, oʻrtacha ekranli qurilmalarda 50%/50% va katta ekranli qurilmalarda 33%/66% boʻlinish berdik:

```
<div class="col-sm-3 col-md-6 col-lg-4">....</div>
<div class="col-sm-9 col-md-6 col-lg-8">....</div>
```

Ammo xlarge ekranli qurilmalarda dizayn 20%/80% holatida yaxshiroq ko'rinadi.

{% hint style="warning" %}
Xlarge ekrali qurilmalar ekranining kengligi 1200px va undan katta bo'ladi.
{% endhint %}

Xlarge ekranli qurilmalar uchun `.col-xl-*` classlaridan foydalanamiz:

```
<div class="col-sm-3 col-md-6 col-lg-4 col-xl-2">....</div>
<div class="col-sm-9 col-md-6 col-lg-8 col-xl-10">....</div>
```

Quyidagi misol kichik ekranli qurilmalarda dizaynni 25%/75% va o'rta ekranli qurilmalarda 50%/50%,  katta ekranli qurilmalarda 33%/66%, xlarge va xxlarge ekranli qurilmalarda 20%/80% qilib bo'ladi. Juda kichik ekranli qurilmalarda u avtomatik tarzda ustma ust bo'lib joylashadi (100%):

<figure><img src="../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

```
<div class="container-fluid">
  <div class="row">
    <div class="col-sm-3 col-md-6 col-lg-4 col-xl-2">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-sm-9 col-md-6 col-lg-8 col-xl-10">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

{% hint style="warning" %}
**Maslahat:** Sahifadagi ustunlarning umumiy soni 12 ta ekanligiga ishonch hosil qiling.
{% endhint %}

### Faqat XLarge-dan foydalanish

Quyidagi misolda faqat `.col-xl-6` classini (`.col-lg-*` yoki  `.col-md-*` siz) beramiz. Bu xlarge va XXL ekranli qurilmalarda elementning 50%/50% ko'rinishida bo'linishini bildiradi. Biroq, kichik va juda kichik ekranli qurilmalar uchun u vertikal tarzda joylashadi. (100%):

<pre><code>&#x3C;div class="container-fluid">
<strong>  &#x3C;div class="row">
</strong><strong>    &#x3C;div class="col-xl-6">
</strong><strong>      &#x3C;p>Lorem ipsum...&#x3C;/p>
</strong><strong>    &#x3C;/div>
</strong><strong>    &#x3C;div class="col-xl-6">
</strong><strong>      &#x3C;p>Sed ut perspiciatis...&#x3C;/p>
</strong>    &#x3C;/div>
  &#x3C;/div>
&#x3C;/div>
</code></pre>

### Avtomatik layout ustunlari

Bootstrap 5 da barcha qurilmalar uchun bir xil kenglikdagi ustunlar yaratishning oson yo‘li mavjud: `.col-xl-*`dan raqamni olib tashlash kifoya va `col-xl` classidan faqat ma’lum miqdordagi `col` elementlarida foydalaning. Bootstrap o'zi qancha ustun borligini aniqlaydi va har bir ustun bir xil kenglikga ega bo'ladi.

Agar ekran o'lchami 1**200px** dan kichik bo'lsa, ustunlar gorizontal tarzda joylashadi:

```
<!-- Two columns: 50% width on xlarge and up-->
<div class="row">
  <div class="col-xl">1 of 2</div>
  <div class="col-xl">2 of 2</div>
</div>

<!-- Four columns: 25% width on xlarge and up -->
<div class="row">
  <div class="col-xl">1 of 4</div>
  <div class="col-xl">2 of 4</div>
  <div class="col-xl">3 of 4</div>
  <div class="col-xl">4 of 4</div>
</div>
```

<figure><img src="../../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure>
