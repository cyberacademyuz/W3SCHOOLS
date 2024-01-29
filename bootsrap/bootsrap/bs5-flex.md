# BS5 Flex

### Flexbox

Bootstrap 3, 4 va Bootstrap 5 o'rtasidagi eng katta farq shundaki, Bootstrap 5 endi joylashuv tartibi (layout)ni boshqarish uchun floatlar o'rniga flexbox-dan foydalanadi.

**Flexible Box Layout** moduli float yoki positioningdan foydalanmasdan moslashuvchan responsive layout strukturasini loyihalashni osonlashtiradi. Agar flex-ni yaxshi tushunmasangiz, bu haqda bizning <mark style="color:green;">**CSS Flexbox**</mark> qo'llanmamizda o'qishingiz mumkin.

{% hint style="warning" %}
**Eslatma:** Flexbox **IE9** va undan kichik versiyalarda qo'llab-quvvatlanmaydi.

Agar sizga **IE8-9** qo'llab-quvvatlashi kerak bo'lsa, **Bootstrap 3**-dan foydalaning. Bu Bootstrap-ning eng barqaror versiyasidir va u hali ham jiddiy xatolarni tuzatish va hujjatlardagi o'zgarishlar uchun jamoa tomonidan qo'llab-quvvatlanadi. Biroq, unga hech qanday yangi xususiyatlar qo'shilmaydi.
{% endhint %}

Flexbox konteynerini yaratish va to'g'ridan to'g'ri bolal elementlarni moslashuvchan elementlarga aylantirish uchun `d-flex` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (684).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex p-3 bg-secondary text-white">
  <div class="p-2 bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 bg-primary">Flex item 3</div>
</div>
```

Inline flexbox konteynerini yaratish uchun `d-inline-flex` classidan foydalaning:

![](<../../.gitbook/assets/image (529).png>)

```
<div class="d-inline-flex p-3 bg-secondary text-white">
  <div class="p-2 bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 bg-primary">Flex item 3</div>
</div>
```

### Gorizontal joylashuv

Moslashuvchan elementlarni gorizontal tarzda (yonma-yon) ko'rsatish uchun `.flex-row` dan foydalaning.&#x20;

**Maslahat:** Gorizontal joylashuvni o'ngga surish uchun `.flex-row-reverse`dan foydalaning :

<figure><img src="../../.gitbook/assets/image (679).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex flex-row bg-secondary">
  <div class="p-2 bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 bg-primary">Flex item 3</div>
</div>

<div class="d-flex flex-row-reverse bg-secondary">
  <div class="p-2 bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 bg-primary">Flex item 3</div>
</div>
```

### Vertikal joylashuv

Moslashuvchan elementlarni vertikal (ustam-ust) ko'rsatish uchun `.flex-column` classidan yoki vertikal joylashtirishni teskarimachasiga ko'rsatish uchun `.flex-column-reverse` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (547).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex flex-column">
  <div class="p-2 bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 bg-primary">Flex item 3</div>
</div>

<div class="d-flex flex-column-reverse">
  <div class="p-2 bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 bg-primary">Flex item 3</div>
</div>
```

### Justify Content

Moslashuvchan elementlarning joylashuvini o'zgartirish uchun `.justify-content-*` classlaridan foydalaning. Ular  `start` (standart), `end`, `center`, `between`yoki `around` hisoblanadi.

<figure><img src="../../.gitbook/assets/image (698).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex justify-content-start">...</div>
<div class="d-flex justify-content-end">...</div>
<div class="d-flex justify-content-center">...</div>
<div class="d-flex justify-content-between">...</div>
<div class="d-flex justify-content-around">...</div>
```

### To'ldirish / bir xil uzunlik

Moslashuvchuan elementlarda ularni bir xil uzunlikda bo'lishiga majburlash uchun `.flex-fill` dan foydalaning:

<figure><img src="../../.gitbook/assets/image (683).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex">
  <div class="p-2 bg-info flex-fill">Flex item 1</div>
  <div class="p-2 bg-warning flex-fill">Flex item 2</div>
  <div class="p-2 bg-primary flex-fill">Flex item 3</div>
</div>
```

### Grow

Qolgan joyni egallash uchun moslashuvchan elementda `.flex-grow-1`dan foydalaning. Quyidagi misolda birinchi ikkita moslashuvchan element o'ziga kerakli joyni egallaydi, oxirgi element esa ortiqcha bo'sh joyning qolgan qismini egallaydi:

<figure><img src="../../.gitbook/assets/image (706).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex">
  <div class="p-2 bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 bg-primary flex-grow-1">Flex item 3</div>
</div>
```

**Maslahat:** Agar uni qisqartirish kerak bo'lib qolsa bu uchun moslashuvchan elementda `.flex-shrink-1`dan foydalaning.

### Tartib

Muayyan moslashuvchan element(lar)ning vizual tartibini `.order` classlari bilan o'zgartiring. Ular  0 dan 5 gacha bo'ladi, bunda eng kichik raqam eng katta ustunlikka ega (order-1 order-2-dan oldin ko'rsatiladi):

![](<../../.gitbook/assets/image (716).png>)

```
<div class="d-flex bg-secondary">
  <div class="p-2 bg-info order-3">Flex item 1</div>
  <div class="p-2 bg-warning order-2">Flex item 2</div>
  <div class="p-2 bg-primary order-1">Flex item 3</div>
</div>
```

### Avtomatik marginlar

&#x20;`.ms-auto` yoki `.me-auto` yordamida elementlarni moslashuvchan qilish uchun avtomatik beriladigan marginlarni osongina qo'shing.

<figure><img src="../../.gitbook/assets/image (703).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex bg-secondary">
  <div class="p-2 ms-auto bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 bg-primary">Flex item 3</div>
</div>

<div class="d-flex bg-secondary">
  <div class="p-2 bg-info">Flex item 1</div>
  <div class="p-2 bg-warning">Flex item 2</div>
  <div class="p-2 me-auto bg-primary">Flex item 3</div>
</div>
```

### Wrap

`.flex-nowrap`, `.flex-wrap` yoki `.flex-wrap-reverse` orqali moslashuvchan elementlarni moslashuvchan konteyneriga o'rab olishni boshqaring.

Misoldagi moslashuvchan elementlarning wrap-ini o'zgartirib, uchxil class o'rtasidagi farqni ko'rish uchun quyidagi tugmalarni bosing:

![](<../../.gitbook/assets/image (543).png>)

<figure><img src="../../.gitbook/assets/image (667).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex flex-wrap">..</div>

<div class="d-flex flex-wrap-reverse">..</div>

<div class="d-flex flex-nowrap">..</div>
```

### Align Content

`.align-content-*` classlari bilan to'plangan moslashuvchan elementlarning vertikal joylashuvini boshqaring. Mos classlar: `.align-content-start` (default), `.align-content-end`, `.align-content-center`, `.align-content-between`, `.align-content-around` va `.align-content-stretch`.

**Eslatma:** Bu classlar moslashuvchan elementlarning bir qatorlilariga ta'sir qilmaydi.

Beshta class o'rtasidagi farqni ko'rish uchun quyidagi tugmachalarni bosing, misoldagi moslashuvchan elementlarning vertikal joylashuvini o'zgartiring:

<figure><img src="../../.gitbook/assets/image (704).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (728).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex flex-wrap align-content-start">..</div>

<div class="d-flex flex-wrap align-content-end">..</div>

<div class="d-flex flex-wrap align-content-center">..</div>

<div class="d-flex flex-wrap align-content-around">..</div>

<div class="d-flex flex-wrap align-content-stretch">..</div>
```

### Align Items

`.align-items-*` classlari orqali bir qatorli moslashuvchan elementlarning vertikal joylashuvini boshqaring. Mos classlar: `.align-items-start`, `.align-items-end`, `.align-items-center`, `.align-items-baseline`, and `.align-items-stretch` (default).

Beshta class o'rtasidagi farqni ko'rish uchun quyidagi tugmalarni bosing:

<figure><img src="../../.gitbook/assets/image (723).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (692).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex align-items-start">..</div>

<div class="d-flex align-items-end">..</div>

<div class="d-flex align-items-center">..</div>

<div class="d-flex align-items-baseline">..</div>

<div class="d-flex align-items-stretch">..</div>
```

### Align Self

Ma'lum bir moslashuvchan elementning vertikal tekislanishini `.align-self-*` classlari orqali boshqaring. Mos classlar: `.align-self-start`, `.align-self-end`, `.align-self-center`, `.align-self-baseline`, va `.align-self-stretch` (default).

Beshta class o'rtasidagi farqni ko'rish uchun quyidagi tugmalarni bosing:

<figure><img src="../../.gitbook/assets/image (351).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-flex bg-light" style="height:150px">
  <div class="p-2 border">Flex item 1</div>
  <div class="p-2 border align-self-start">Flex item 2</div>
  <div class="p-2 border">Flex item 3</div>
</div>
```

### Responsive Flex classlar

Barcha moslashuvchan classlar qo'shimcha responsive classalr bilan birga keladi, bu esa ma'lum bir ekran o'lchamida ma'lum bir moslashuvchan class berishni osonlashtiradi.

`*` belgisini `sm`, `md`, `lg`, `xl` yoki `xxl` bilan almashtirish mumkin, bu kichik, o'rta, katta, xlarge va xxlarge ekranlarni ifodalaydi.

| Class                        | Ta'rif                                                                                      |
| ---------------------------- | ------------------------------------------------------------------------------------------- |
| Flex Container               |                                                                                             |
| `.d-*-flex`                  | Turli ekranlar uchun flexbox konteynerini yaratadi                                          |
| `.d-*-inline-flex`           | Turli ekranlar uchun inline flexbox konteynerini yaratadi                                   |
| Direction                    |                                                                                             |
| `.flex-*-row`                | Moslashuvchan elementlarni turli ekranlarda gorizontal shaklda ko'rsatish                   |
| `.flex-*-row-reverse`        | Moslashuvchan elementlarni turli ekranlarda gorizontal va o'ngga surilgan holda ko'rsatish  |
| `.flex-*-column`             | Moslashuvchan elementlarni turli ekranlarda  vertikal tarzda ko'rsatish                     |
| `.flex-*-column-reverse`     | Moslashuvchan elementlarni turli ekranlarda  vertikal tarzda va teskari tartibda ko'rsatish |
| Justified Content            |                                                                                             |
| `.justify-content-*-start`   | Moslashuvchan elementlarni turli ekranlarda qator boshida (chapga surilgan) ko'rsatish      |
| `.justify-content-*-end`     | Moslashuvchan elementlarni turli ekranlarda ohirida (o'ngga surilgan) ko'rsatish            |
| `.justify-content-*-center`  | Moslashuvchan elementlarni turli ekranlarda o'rtada ko'rsatish                              |
| `.justify-content-*-between` | Moslashuvchan elementlarni turli ekranlarda oraliqda ko'rsatish                             |
| `.justify-content-*-around`  | Moslashuvchan elementlarni turli ekranlarda atrofda ko'rsatish                              |
| Fill / Equal Width           |                                                                                             |
| `.flex-*-fill`               | Moslashuvchan elementlarni turli ekranlarda bir xil uzunlikga majburlash                    |
| Grow                         |                                                                                             |
| `.flex-*-grow-0`             | Elementlarni turli ekranlardagi bo'sh joyni egallamaydigan qilish                           |
| `.flex-*-grow-1`             | Elementlarni turli ekranlarda bo'sh joyni egallaydigan qilish                               |
| Shrink                       |                                                                                             |
| `.flex-*-shrink-0`           | Elementlarni turli ekranlarda kichraytirmaslik                                              |
| `.flex-*-shrink-1`           | Elementlarni turli ekranlarda kichraytirish                                                 |
| Order                        |                                                                                             |
| `.order-*-`_`0-12`_          | Kichik ekranlarda tartibni 0 dan 5 gacha o'zgartirish                                       |
| Wrap                         |                                                                                             |
| `.flex-*-nowrap`             | Elementlarni turli ekranlarga wrap qilmaslik                                                |
| `.flex-*-wrap`               | Elementlarni turli ekranlarga wrap qilish                                                   |
| `.flex-*-wrap-reverse`       | Turli ekranlarda elementlarning teskari wrapp qilinishi                                     |
| Align Content                |                                                                                             |
| `.align-content-*-start`     | Yig'ilgan narsalarni turli ekranlarda qator boshiga joylash                                 |
| `.align-content-*-end`       | Yig'ilgan narsalarni turli ekranlarda qator ohiriga joylash                                 |
| `.align-content-*-center`    | Yig'ilgan narsalarni turli ekranlarda qator o'rtasiga joylash                               |
| `.align-content-*-around`    | Yig'ilgan narsalarni turli ekranlarda qator atrofiga joylash                                |
| `.align-content-*-stretch`   | Yig'ilgan narsalarni turli ekranlarda cho'zish.                                             |
| Align Items                  |                                                                                             |
| `.align-items-*-start`       | Elementlarning bir qatorlilarini turli ekranlarda qator boshiga joylash                     |
| `.align-items-*-end`         | Elementlarning bir qatorlilarini turli ekranlarda qator ohiriga joylash                     |
| `.align-items-*-center`      | Elementlarning bir qatorlilarini turli ekranlarda o'rtaga joylash                           |
| `.align-items-*-baseline`    | Elementlarning bir qatorlilarini turli ekranlarda bir chiziqga joylash                      |
| `.align-items-*-stretch`     | Elementlarning bir qatorlilarini turli ekranlarda cho'zish                                  |
| Align Self                   |                                                                                             |
| `.align-self-*-start`        | Moslashuvchan elementni turli ekranlarda qator boshiga joylash                              |
| `.align-self-*-end`          | Moslashuvchan elementni turli ekranlarda qator ohiriga joylash                              |
| `.align-self-*-center`       | Moslashuvchan elementni turli ekranlarda qator o'rtasiga joylash                            |
| `.align-self-*-baseline`     | Moslashuvchan elementni turli ekranlarda asosiy chiziqqa joylash                            |
| `.align-self-*-stretch`      | Moslashuvchan elementni turli ekranlarda asosiy cho'zish                                    |
