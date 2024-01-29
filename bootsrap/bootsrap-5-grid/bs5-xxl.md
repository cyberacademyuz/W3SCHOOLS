# BS5 XXL

### XXL Gridiga misoli

|                  | XSmall  | Small      | Medium     | Large      | Extra Large | XXL         |
| ---------------- | ------- | ---------- | ---------- | ---------- | ----------- | ----------- |
| **Class prefix** | `.col-` | `.col-sm-` | `.col-md-` | `.col-lg-` | `.col-xl-`  | `.col-xxl-` |
| **Screen width** | <576px  | >=576px    | >=768px    | >=992px    | >=1200px    | >=1400px    |

{% hint style="warning" %}
XXL ekranli qurilmalarning ekran kengligi **1400px**dan katta bo'ladi.
{% endhint %}

Quyidagi misol o'rta, katta va xlarge elranli qurilmalarda dizaynni 50%/50% va XXL ekranli qurilmalarda 25%/75% qilib bo'ladi. Juda kichik ekranli qurilmalarda u avtomatik tarzda ustma ust bo'lib joylashadi (100%):

<figure><img src="../../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

```
<div class="container-fluid">
  <div class="row">
    <div class="col-md-6 col-xxl-3">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-md-6 col-xxl-9">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```

{% hint style="warning" %}
**Maslahat:** Sahifadagi ustunlarning umumiy soni 12 ta ekanligiga ishonch hosil qiling.
{% endhint %}

### Faqat XXL dan foydalanish

Quyidagi misolda faqat `.col-xxl-6` classini (`.col-lg-*` yoki  `.col-md-*` siz) beramiz. Bu xlarge va XXL ekranli qurilmalarda elementning 50%/50% ko'rinishida bo'linishini bildiradi. Biroq, xlarge, katta, o'rtacha, kichik va juda kichik ekranli qurilmalar uchun u vertikal tarzda joylashadi. (100%):

<pre><code>&#x3C;div class="container-fluid">
<strong>  &#x3C;div class="row">
</strong>    &#x3C;div class="col-xxl-6">
<strong>      &#x3C;p>Lorem ipsum...&#x3C;/p>
</strong>    &#x3C;/div>
<strong>    &#x3C;div class="col-xxl-6">
</strong>      &#x3C;p>Sed ut perspiciatis...&#x3C;/p>
<strong>    &#x3C;/div>
</strong>  &#x3C;/div>
<strong>&#x3C;/div>
</strong></code></pre>

### Avtomatik tartib ustunlari

Bootstrap 5 da barcha qurilmalar uchun bir xil kenglikdagi ustunlar yaratishning oson yo‘li mavjud: `.col-xxl-*`dan raqamni olib tashlash kifoya va `col-xxl` classidan faqat ma’lum miqdordagi `col` elementlarida foydalaning. Bootstrap o'zi qancha ustun borligini aniqlaydi va har bir ustun bir xil kenglikga ega bo'ladi.

Agar ekran o'lchami **1400px** dan kichik bo'lsa, ustunlar gorizontal tarzda joylashadi:

```
<!-- Two columns: 50% width on xxl and up-->
<div class="row">
  <div class="col-xxl">1 of 2</div>
  <div class="col-xxl">2 of 2</div>
</div>

<!-- Four columns: 25% width on xxl and up -->
<div class="row">
  <div class="col-xxl">1 of 4</div>
  <div class="col-xxl">2 of 4</div>
  <div class="col-xxl">3 of 4</div>
  <div class="col-xxl">4 of 4</div>
</div>
```

<figure><img src="../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>
