# BS5 Grid asoslari

### Bootstrap 5 Grid tizimi

Bootstrapning grid tizimi flexbox asosida tuzilgan va sahifa bo'ylab 12 tagacha ustun kiritishga ruxsat beradi.

Agar 12 ta ustundan alohida foydalanishni xohlamasangiz, kattaroq ustunlar yaratish uchun ustunlarni birga guruhlashingiz mumkin:

<figure><img src="../../.gitbook/assets/image (560).png" alt=""><figcaption></figcaption></figure>

Grid tizimi moslashuvchan va ustunlar ekran o'lchamiga qarab avtomatik tarzda moslashadi.

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

Quyida biz boshlan'gich Bootstrap 5 grid maketlarining ba'zi misollarini to'pladik.

### Uchta bir xil ustunlar

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

Quyidagi misol barcha qurilmalarda va ekran kengligida uchta bir xil kenglikdagi ustunlarni qanday yaratish kerakligini ko'rsatadi:

```
<div class="row">
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
</div>
```

### Moslashuvchan ustunlar

<figure><img src="../../.gitbook/assets/image (577).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda planshetlardan boshlab va qo'shimcha katta ish stollariga moslashadigan bir xil kenglikdagi to'rtta ustunni qanday yaratish kerakligi ko'rsatilgan. Kengligi 576px dan kichik boʻlgan mobil telefonlar yoki ekranlarda ustunlar avtomatik tarzda bir-birining ustida joylashadi:

```
<div class="row">
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
</div>
```

### Ikkita turli kenglikdagi moslashuvchan ustunlar

<figure><img src="../../.gitbook/assets/image (606).png" alt=""><figcaption></figcaption></figure>

Quyidagi misol planshetlardan boshlab, katta qo'shimcha ish stollariga moslashadigan ikkita turli kenglikdagi ustunlarni qanday tuzish mumkinligini ko'rsatadi:

```
<div class="row">
  <div class="col-sm-4">.col-sm-4</div>
  <div class="col-sm-8">.col-sm-8</div>
</div>
```

{% hint style="warning" %}
**Maslahat:** Ushbu qo'llanmada keyinroq **grid tizimi** haqida batafsil bilib olasiz.
{% endhint %}
