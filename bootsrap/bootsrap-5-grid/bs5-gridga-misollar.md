# BS5 Gridga misollar

Quyida Bootstrap 5 grid maketlarining ba'zi misollarini to'pladik.

### Uchta bir xil ustun

Belgilangan miqdordagi elementlarda `.col` classidan foydalaning va Bootstrapning o'zi qancha element borligini aniqlaydi (va bir xil kenglikdagi ustunlar yaratadi). Quyidagi misolda biz har birining kengligi 33,33% bo'lgan uchta ustun elementidan foydalanamiz.

<figure><img src="../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

```
<div class="row">
  <div class="col">col</div>
  <div class="col">col</div>
  <div class="col">col</div>
</div>
```

### Raqamlardan foydalangan holda uchta bir xil ustun

Ustun kengligini boshqarish uchun raqamlardan ham foydalanishingiz mumkin. Shunchaki sahifadagi ustunlarning umumiy soni 12 ta ekanligiga yoki undan kamligiga ishonch hosil qiling. (barcha 12 ta ustundan foydalanish shart emas).

<figure><img src="../../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure>

```
<div class="row">
  <div class="col-4">col-4</div>
  <div class="col-4">col-4</div>
  <div class="col-4">col-4</div>
</div>
```

### Uch bir xil bo'lmagan ustunlar

Kengligi bir xil bo'lmagan ustunlar yaratish uchun raqamlardan foydalanishingiz kerak. Quyidagi misol 25%/50%/25% ko'rinishidagi bo'linish hosil qiladi:

<figure><img src="../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

```
<div class="row">
  <div class="col-3">col-3</div>
  <div class="col-6">col-6</div>
  <div class="col-3">col-3</div>
</div>
```

### Bitta ustun kengligini belgilash

Biroq yoqridagi kabi teng bo'lmagan ustunlar yaratish uchun faqat bitta ustun kengligini belgilash va uning atrofidagi ustunlarnining o'lchamlarini avtomatik tarzda hisoblanadigan qilih qo'yish kifoya. Quyidagi misol yuqoridagi misol kabi 25%/50%/25% ko'rinishidagi bo'linish hosil qiladi:

<figure><img src="../../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>

```
<div class="row">
  <div class="col">col</div>
  <div class="col-6">col-6</div>
  <div class="col">col</div>
</div>
```

### Bir xil uzunlikdagi ko'p ustunlar

<figure><img src="../../.gitbook/assets/image (535).png" alt=""><figcaption></figcaption></figure>

```
<!-- Two equal columns -->
<div class="row">
  <div class="col">1 of 2</div>
  <div class="col">2 of 2</div>
</div>

<!-- Four equal columns -->
<div class="row">
  <div class="col">1 of 4</div>
  <div class="col">2 of 4</div>
  <div class="col">3 of 4</div>
  <div class="col">4 of 4</div>
</div>

<!-- Six equal columns -->
<div class="row">
  <div class="col">1 of 6</div>
  <div class="col">2 of 6</div>
  <div class="col">3 of 6</div>
  <div class="col">4 of 6</div>  
  <div class="col">5 of 6</div>
  <div class="col">6 of 6</div>
</div>
```

### Qatorlar

Bundan tashqari, `.row-cols-*` classlari orali bir-birining yonida nechta ustun bo'lishi kerakligini ham (qancha ustun bo'lishidan qat'iy nazar) boshqarishingiz mumkin:

<figure><img src="../../.gitbook/assets/image (232).png" alt=""><figcaption></figcaption></figure>

```
<div class="row row-cols-1">
  <div class="col">1 of 2</div>
  <div class="col">2 of 2</div>
</div>

<div class="row row-cols-2">
  <div class="col">1 of 4</div>
  <div class="col">2 of 4</div>
  <div class="col">3 of 4</div>
  <div class="col">4 of 4</div>
</div>

<div class="row row-cols-3">
  <div class="col">1 of 6</div>
  <div class="col">2 of 6</div>
  <div class="col">3 of 6</div>
  <div class="col">4 of 6</div>  
  <div class="col">5 of 6</div>
  <div class="col">6 of 6</div>
</div>
```

### Bir xil uzunlikda bo'lmagan ko'p ustunlar

<figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

```
<!-- Two Unequal Columns -->
<div class="row">
  <div class="col-8">1 of 2</div>
  <div class="col-4">2 of 2</div>
</div>

<!-- Four Unequal Columns -->
<div class="row">
  <div class="col-2">1 of 4</div>
  <div class="col-2">2 of 4</div>
  <div class="col-2">3 of 4</div>
  <div class="col-6">4 of 4</div>
</div>

<!-- Setting two column widths -->
<div class="row">
  <div class="col-4">1 of 4</div>
  <div class="col-6">2 of 4</div>
  <div class="col">3 of 4</div>
  <div class="col">4 of 4</div>
</div>
```

### Bir xil balandlik

Agar ustunlardan biri boshqasidan balandroq bo'lsa (matn yoki CSS balandligi tufayli), qolganlari quyidagicha bo'ladi:

<figure><img src="../../.gitbook/assets/image (164).png" alt=""><figcaption></figcaption></figure>

```
<div class="row">
  <div class="col">Lorem ipsum...</div>
  <div class="col">col</div>
  <div class="col">col</div>
</div>
```

### Ichki ustunlar

<figure><img src="../../.gitbook/assets/image (446).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda ikkita ustun layoutini qanday yaratish kerakligi ko'rsatilgan, bunda ustunlardan birida yana ikkita ustun mavjud:

```
<div class="row">
  <div class="col-8">
    .col-8
    <div class="row">
      <div class="col-6">.col-6</div>
      <div class="col-6">.col-6</div>
    </div>
  </div>
  <div class="col-4">.col-4</div>
</div>
```

### Javobgar sinflar

Bootstrap 5 grid tizimida oltita class bor:

* `.col-` (qo'shimcha kichik qurilmalar - ekran kengligi 576px dan kichikina)
* `.col-sm-` (kichkina qurilmalar - ekran kengligi 576 pikselga teng yoki undan katta)
* `.col-md-` (o'rtacha qurilmalar - ekran kengligi 768 pikselga teng yoki undan katta)
* `.col-lg-` (katta qurilmalar - ekran kengligi 992 pikselga teng yoki undan katta)
* `.col-xl-` (xlarge qurilmalar - ekran kengligi 1200px ga teng yoki undan katta)
* `.col-xxl-` (xxlarge qurilmalari - ekran kengligi 1400px ga teng yoki undan katta)

Yuqoridagi classlar yanada dinamik va moslashuvchan tartiblarni yaratishi uchun birlashtirilishi mumkin.

**Maslahat:** Har bir class kattalashadi, shuning uchun `sm` va `md` uchun bir xil width bermoqchi bo'lsangiz, faqat `sm`ni belgilashingiz kerak.

## Ustma ustdan gorizontalga

<figure><img src="../../.gitbook/assets/image (440).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda kattaroq ekranli qurilmalarda (`sm`, `md`, `lg` va `xl`) gorizontal holatga o'tmasdan oldin juda kichik ekranli qurilmalarda ustma ust shaklda ustun layoutini qanday yaratish ko'rsatilgan:

```
<div class="row">
  <div class="col-sm-9">col-sm-9</div>
  <div class="col-sm-3">col-sm-3</div>
</div>
<div class="row">
  <div class="col-sm">col-sm</div>
  <div class="col-sm">col-sm</div>
  <div class="col-sm">col-sm</div>
</div>
```

### Aralashtirish va moslash

<figure><img src="../../.gitbook/assets/image (526).png" alt=""><figcaption></figcaption></figure>

```
<!-- 50%/50% split on extra small devices and 75%/25% split on larger devices -->
<div class="row">
  <div class="col-6 col-sm-9">col-6 col-sm-9</div>
  <div class="col-6 col-sm-3">col-6 col-sm-3</div>
</div>

<!-- 58%/42% split on extra small, small and medium devices and 66.3%/33.3% split on large and xlarge devices -->
<div class="row">
  <div class="col-7 col-lg-8">col-7 col-lg-8</div>
  <div class="col-5 col-lg-4">col-5 col-lg-4</div>
</div>

<!-- 25%/75% split on small devices, a 50%/50% split on medium devices, and a 33%/66% split on large and xlarge devices. On extra small devices, it will automatically stack (100%) -->
<div class="row">
  <div class="col-sm-3 col-md-6 col-lg-4">col-sm-3 col-md-6 col-lg-4</div>
  <div class="col-sm-9 col-md-6 col-lg-8">col-sm-9 col-md-6 col-lg-8</div>
</div>
```

### Gutterslarni olib tashlash

Ustunlar orasidagi bo'sh joylarni o'zgartirish uchun har qanday `.g-1|2|3|4|5` classidan foydalaning (`.g-4` standart bo'ladi).

Gutterslarni butunlay olib tashlash uchun `.g-0` dan foydalaning:

<figure><img src="../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

```
<div class="row g-0">
```
