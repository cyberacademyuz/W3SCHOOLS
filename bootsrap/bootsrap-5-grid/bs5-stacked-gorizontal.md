# BS5 Stacked/Gorizontal

### Gridga misol: Ustama utlikdan-gorizontalgacha

Kattaroq qurilmalarda gorizontal holatga o'tishdan oldin, juda kichik qurilmalarda ustam ust turuvchi sodda grid tizimini yarataylik.

Quyidagi misolda oddiy “stacked-to-gorizontal” ikki ustunli layout ko‘rsatilgan, ya’ni u barcha ekranlarda 50% ga 50% bo‘linadi, juda kichik ekranlar esa bundan mustasno, ular avtomatik tarzda ustam ust bo'lib olishadi (100%):

<figure><img src="../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

{% code title="Misol: stacked-to-gorizontal" %}
```
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
{% endcode %}

{% hint style="warning" %}
`.col-sm-*` classlaridagi raqamlar `<div>` qancha ustundan iborat bo'lishi kerakligini ko'rsatadi (12 tadan). Shunday qilib, `.col-sm-1` 1ta ustunni, `.col-sm-4` 4ta ustunni, `.col-sm-6` 6 ta ustunni va boshqalarni o'z ichiga oladi.

**Maslahat:** Sahifadagi ustunlarning umumiy soni 12 ta ekanligiga yoki undan kamligiga ishonch hosil qiling. (barcha 12 ta ustundan foydalanish shart emas).
{% endhint %}

**Maslahat:** `.container-fluid` classini `.container`ga oʻzgartirish orqali har qanday toʻliq kenglikdagi layoutni belgilangan kenglikdagi moslashuvchan layoutga aylantirishingiz mumkin:

{% code title="Misol: Javob beruvchi konteyner" %}
```
<div class="container">
  <div class="row">
    <div class="col-sm-6">
      <p>Lorem ipsum...</p>
    </div>
    <div class="col-sm-6">
      <p>Sed ut perspiciatis...</p>
    </div>
  </div>
</div>
```
{% endcode %}

### Avtomatik tartib ustunlari

Bootstrap 5 da barcha qurilmalar uchun bir xil kenglikdagi ustunlar yaratishning oson yo‘li mavjud: `.col-size-*`dan raqamni olib tashlash kifoya va `col-size` classidan faqat ma’lum miqdordagi `col` elementlarida foydalaning. Bootstrap o'zi qancha ustun borligini aniqlaydi va har bir ustun bir xil kenglikga ega bo'ladi. O'lcham classlari (`sm`, `md` va boshqalar) ustunlar qachon moslashuvchan bo'lishini belgilaydi:

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

<figure><img src="../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>
