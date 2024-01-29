# BS5 Utilitalar

### Utilitalar/yordamchi classlar

Bootstrap 5 hech qanday CSS kodidan foydalanmasdan elementlarga tezda still berish uchun juda ko'p utilita/yordamchi classlarga ega.

### Chegaralar

Elementga chegara qo'shish yoki chegarani olib tashlash uchun `border` classlaridan foydalaning:

<figure><img src="../../.gitbook/assets/image (675).png" alt=""><figcaption></figcaption></figure>

```
<span class="border"></span>
<span class="border border-0"></span>
<span class="border border-top-0"></span>
<span class="border border-end-0"></span>
<span class="border border-bottom-0"></span>
<span class="border border-start-0"></span>
<br>

<span class="border-top"></span>
<span class="border-end"></span>
<span class="border-bottom"></span>
<span class="border-start"></span>
```

### Chegara uzunligi

Chegaraning uzunligini berish uchun `.border-1` dan `.border-5` gacha bo'lgan classlardan foydalaning:

<figure><img src="../../.gitbook/assets/image (722).png" alt=""><figcaption></figcaption></figure>

```
<span class="border border-1"></span>
<span class="border border-2"></span>
<span class="border border-3"></span>
<span class="border border-4"></span>
<span class="border border-5"></span>
```

### Chegara rangi

Chegara ranglari uchun mo'ljallangan istalgan classdan foydalanib chegara uchun rang bering.

<figure><img src="../../.gitbook/assets/image (691).png" alt=""><figcaption></figcaption></figure>

```
<span class="border border-primary"></span>
<span class="border border-secondary"></span>
<span class="border border-success"></span>
<span class="border border-danger"></span>
<span class="border border-warning"></span>
<span class="border border-info"></span>
<span class="border border-light"></span>
<span class="border border-dark"></span>
<span class="border border-white"></span>
```

### Chegara radiusi

`rounded` classlari orqali elementga yumaloq burchaklar qo'shing:

<figure><img src="../../.gitbook/assets/image (710).png" alt=""><figcaption></figcaption></figure>

```
<span class="rounded"></span>
<span class="rounded-top"></span>
<span class="rounded-end"></span>
<span class="rounded-bottom"></span>
<span class="rounded-start"></span>
<span class="rounded-circle"></span>
<span class="rounded-pill" style="width:130px"></span>
<span class="rounded-0"></span>
<span class="rounded-1"></span>
<span class="rounded-2"></span>
<span class="rounded-3"></span>
<span class="rounded-4"></span>
<span class="rounded-5"></span>
```

### Float va Clearfix

Elementni `.float-end` classi bilan o‘ngga yoki `.float-start` bilan chapga suring, `.clearfix` classi bilan esa floatlarni tozalang:

<figure><img src="../../.gitbook/assets/image (664).png" alt=""><figcaption></figcaption></figure>

```
<div class="clearfix">
  <span class="float-start">Float left</span>
  <span class="float-end">Float right</span>
</div>
```

### Moslashuvchan floatlar

Elementni ekran kengligiga qarab chapga yoki o‘ngga moslashadigan float classlari (`.float-*-start|end` - where \* is `sm` (>=576px), `md` (>=768px), `lg` (>=992px), `xl` (>=1200px) or `xxl` (>=1400px)):

<figure><img src="../../.gitbook/assets/image (554).png" alt=""><figcaption></figcaption></figure>

```
<div class="float-sm-end">Float right on small screens or wider</div><br>
<div class="float-md-end">Float right on medium screens or wider</div><br>
<div class="float-lg-end">Float right on large screens or wider</div><br>
<div class="float-xl-end">Float right on extra large screens or wider</div><br>
<div class="float-xxl-end">Float right on XXL screens or wider</div><br>
<div class="float-none">Float none</div>
```

### Markazga joylashtirish

Elementni `.mx-auto` classi orqali markazga joylashtiring (margin-lef va margin-right avtomatik tarzda qo'shiladi):

<figure><img src="../../.gitbook/assets/image (686).png" alt=""><figcaption></figcaption></figure>

```
<div class="mx-auto bg-warning" style="width:150px">Centered</div>
```

### Kengligi (width)

Element uzunligini `W-*`  classlari (`.w-25`, `.w-50`, `.w-75`, `.w-100`, `.mw-auto`, `.mw-100`) bilan belgilang:

<figure><img src="../../.gitbook/assets/image (548).png" alt=""><figcaption></figcaption></figure>

```
<div class="w-25 bg-warning">Width 25%</div>
<div class="w-50 bg-warning">Width 50%</div>
<div class="w-75 bg-warning">Width 75%</div>
<div class="w-100 bg-warning">Width 100%</div>
<div class="w-auto bg-warning">Auto Width</div>
<div class="mw-100 bg-warning">Max Width 100%</div>
```

### Balandligi (height)

Element balandligini `h-*` classlari ( `.h-25`, `.h-50`, `.h-75`, `.h-100`, `.mh-auto`, `.mh-100`) bilan belgilang:

<figure><img src="../../.gitbook/assets/image (688).png" alt=""><figcaption></figcaption></figure>

```
<div style="height:200px;background-color:#ddd">
  <div class="h-25 bg-warning">Height 25%</div>
  <div class="h-50 bg-warning">Height 50%</div>
  <div class="h-75 bg-warning">Height 75%</div>
  <div class="h-100 bg-warning">Height 100%</div>
  <div class="h-auto bg-warning">Auto Height</div>
  <div class="mh-100 bg-warning" style="height:500px">Max Height 100%</div>
</div>
```

### Bo'sh joy

Bootstrap 5 keng doiradagi moslashuvchan maargin va padding utilitalariga ega. Ular barcha breakpointlar uchun ishlaydi: `xs` (<=576px), `sm` (>=576px), `md` (>=768px), `lg` (>=992px), `xl` (>=1200px) or `xxl` (>=1400px)):

Classlar quyidagi formatda ishlatiladi: `xs` uchun `{property}{sides}-{size}` va `sm`, `md`, `lg`, `xl` va `xxl` uchun `{property}{sides}-{breakpoint}-{size}`

Bu yerdagi xususiyat quyidagilardan biri hisoblanadi:

* `m`- `margin` beradi
* `p`- `padding` beradi

Qaysi tomonini belgilash:

* `t`- `margin-top`yoki`padding-top` beradi
* `b`- `margin-bottom`yoki`padding-bottom` beradi
* `s`- `margin-left` yoki `padding-left` beradi
* `e`- `margin-right` yoki `padding-right` beradi
* `x` - `padding-left` va `padding-right`yoki `margin-left`va `margin-right` ikkalasini ham o'rnatadi
* `y` - `padding-top` va `padding-bottom` yoki `margin-top`va `margin-bottom` ikkalasini ham beradi
* blank - elementning barcha 4 tomoniga `margin` yoki `padding` beradi

Bu yerdagi o'lcham quyidagilardan biri hisoblanadi:

* `0`- `margin`yoki `padding` ni 0 qiladi
* `1`- `margin`yoki `padding`ni `.25rem` qiladi
* `2`- `margin`yoki `padding`ni`.5rem` qiladi
* `3`- `margin`yoki `padding`ni `1rem` qiladi
* `4`- `margin`yoki `padding`ni`1.5rem` qiladi
* `5`- `margin`yoki `padding`ni `3rem` qiladi
* `auto`- `margin`avtomatik tarzda o'rnatiladi

<figure><img src="../../.gitbook/assets/image (708).png" alt=""><figcaption></figcaption></figure>

```
</div>
<div class="p-5 bg-success">I have a padding on all sides (3rem)</div>
<div class="m-5 pb-5 bg-info">I have a margin on all sides (3rem) and a bottom padding (3rem)</div>
```

#### Yuqoridagiga aloqador ko'proq misollar

| `.m-# / m-*-#`   | har tomondan margin           |
| ---------------- | ----------------------------- |
| `.mt-# / mt-*-#` | margin top                    |
| `.mb-# / mb-*-#` | margin bottom                 |
| `.ms-# / ms-*-#` | margin left                   |
| `.me-# / me-*-#` | margin right                  |
| `.mx-# / mx-*-#` | margin left va margin right   |
| `.my-# / my-*-#` | margin top va margin bottom   |
| `.p-# / p-*-#`   | har tomondan padding          |
| `.pt-# / pt-*-#` | padding top                   |
| `.pb-# / pb-*-#` | padding bottom                |
| `.ps-# / ps-*-#` | padding left                  |
| `.pe-# / pe-*-#` | padding right                 |
| `.py-# / py-*-#` | padding top va padding bottom |
| `.px-# / px-*-#` | padding left va padding right |

{% hint style="warning" %}
Turli `rem` o'lcham birliklari haqida ko'proq ma'lumotni **CSS birliklari** ma'lumotnomamizda o'qishingiz mumkin.
{% endhint %}

### Soyalar

Elementga soya qo'shish uchun `shadow-` classlaridan foydalaning:

<figure><img src="../../.gitbook/assets/image (545).png" alt=""><figcaption></figcaption></figure>

```
<div class="shadow-none p-4 mb-4 bg-light">No shadow</div>
<div class="shadow-sm p-4 mb-4 bg-white">Small shadow</div>
<div class="shadow p-4 mb-4 bg-white">Default shadow</div>
<div class="shadow-lg p-4 mb-4 bg-white">Large shadow</div>
```

### Vertikal joylashuv

Elementlarning joylashishini o'zgartirish uchun `align-` classlaridan foydalaning (faqat inline, inline-block, inline-table va jadvalning katak elementlarida ishlaydi):

<figure><img src="../../.gitbook/assets/image (549).png" alt=""><figcaption></figcaption></figure>

```
<span class="align-baseline">baseline</span>
<span class="align-top">top</span>
<span class="align-middle">middle</span>
<span class="align-bottom">bottom</span>
<span class="align-text-top">text-top</span>
<span class="align-text-bottom">text-bottom</span>
```

### Aspect Ratio

Ota-ona elementning kengligi asosida moslashuvchan video yoki slayd-shoular yaratish.

`.ratio` classini o'zingiz tanlagan .ratio-\* nisbati bilan birga ota ona elementiga bering va uning ichiga embed qo'shing.

```
<!-- Aspect ratio 1:1 -->
<div class="ratio ratio-1x1">
  <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY"></iframe>
</div>

<!-- Aspect ratio 4:3 -->
<div class="ratio ratio-4x3">
  <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY"></iframe>
</div>

<!-- Aspect ratio 16:9 -->
<div class="ratio ratio-16x9">
  <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY"></iframe>
</div>

<!-- Aspect ratio 21:9 -->
<div class="ratio ratio-21x9">
  <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY"></iframe>
</div>
```

### Ko'rinish

Elementlarning ko'rinishini boshqarish uchun `.visible` yoki `invisible` classlaridan foydalaning. **Eslatma:** Bu classlar CSSning display qiymatini o'zgartirmaydi. Ular faqat `visibility:visible` yoki `visibility:hidden` ni qo'shadi.&#x20;

<figure><img src="../../.gitbook/assets/image (700).png" alt=""><figcaption></figcaption></figure>

```
<div class="visible">I am visible</div>
<div class="invisible">I am invisible</div>
```

### Yopish ikonkasi

Yopish ikonkasini yaratish uchun `.btn-close` classidan foydalaning. Bu ko'pincha alert va modallar uchun ishlatiladi.

<figure><img src="../../.gitbook/assets/image (660).png" alt=""><figcaption></figcaption></figure>

```
<button type="button" class="btn-close"></button>
```

### Screenreaderslar

Elementni barcha qurilmalarda yashirish uchun `.visually-hidden` classidan foydalaning, ekranni oʻqish vositalaridan tashqari:

```
<span class="visually-hidden">I will be hidden on all screens except for screen readers.</span>
```

### Ranglar

**Ranglar** bo'limida tavsiflanganidek, bu yerda barcha matn va orqafon rang  classlarining ro'yxati keltirilgan:

Matn ranglarining classlari quyidagilardir: `.text-muted`, `.text-primary`, `.text-success`, `.text-info`, `.text-warning`, `.text-danger`, `.text-secondary`, `.text-white`, `.text-dark`, `.text-body` va `.text-light`:

<figure><img src="../../.gitbook/assets/image (666).png" alt=""><figcaption></figcaption></figure>

Tarkibiy matn classlari havolalarda ham ishlatilishi mumkin:

<figure><img src="../../.gitbook/assets/image (721).png" alt=""><figcaption></figcaption></figure>

Shuningdek, `.text-black-50` yoki `.text-white-50` classlari bilan qora yoki oq matn uchun 50% shaffoflik ham qo'shishingiz mumkin:

<figure><img src="../../.gitbook/assets/image (714).png" alt=""><figcaption></figcaption></figure>

### Fon ranglari

Fon ranglari uchun classlar: `.bg-primary`, `.bg-success`, `.bg-info`, `.bg-warning`, `.bg-danger`, `.bg-secondary`, `.bg-dark` va `.bg-light`.

<figure><img src="../../.gitbook/assets/image (676).png" alt=""><figcaption></figcaption></figure>

Yuqoridagi `.bg-color` classlari matn bilan yaxshi ishlamaydi yoki hech bo'lmaganda har bir orqafon uchun to'g'ri matn rangini olishda tegishli `.text-color` classini belgilashingiz kerak.

Biroq, siz `.text-bg-color` classlaridan foydalanishingiz mumkin va Bootstrap har bir orqfon rangi uchun mos matn rangini avtomatik tarzda boshqaradi:

<figure><img src="../../.gitbook/assets/image (709).png" alt=""><figcaption></figcaption></figure>
