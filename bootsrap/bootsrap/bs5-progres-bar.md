# BS5 Progres bar

### Sodda progres bar

Progres bari foydalanuvchi jarayonning qayeridaligini ko'rsatish uchun ishlatilishi mumkin.

<figure><img src="../../.gitbook/assets/image (624).png" alt=""><figcaption></figcaption></figure>

Standart pregres barini yaratish uchun konteyner elementiga `.progress` classini qo'shing va uning bola elementiga `.progress-bar` classini qo'shing. Progres barining uzunligini belgilash uchun CSSning `width` xususiyatidan foydalaning:

```
<div class="progress">
  <div class="progress-bar" style="width:70%"></div>
</div>
```

### Progress bar balandligi

<figure><img src="../../.gitbook/assets/image (630).png" alt=""><figcaption></figcaption></figure>

Progres barning balandligi default tarzda `1rem`(odatda `16px`) bo'ladi. Uni o'zgartirish uchun CSSning `height` xususiyatidan foydalaning. Progres konteyneri va progres bar uchun bir xil balandlik berishingiz kerakligini unutmang:

```
<div class="progress" style="height:20px">
  <div class="progress-bar" style="width:40%;height:20px"></div>
</div>
```

### Progres bar labeli

Necha foizligini ko'rsatish uchun progress bariga matn qo'shing:

<figure><img src="../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

```
<div class="progress">
  <div class="progress-bar" style="width:70%">70%</div>
</div>
```

### Rangli taraqqiyot barlari

<figure><img src="../../.gitbook/assets/image (604).png" alt=""><figcaption></figcaption></figure>

Progress barning standart  ranggi ko'k. Uning rangini o'zgartirish uchun orqafon ranggni belgilovchi istalgan tarkibiy classlardan foydalaning:

```
<!-- Blue -->
<div class="progress">
  <div class="progress-bar" style="width:10%"></div>
</div>

<!-- Green -->
<div class="progress">
  <div class="progress-bar bg-success" style="width:20%"></div>
</div>

<!-- Turquoise -->
<div class="progress">
  <div class="progress-bar bg-info" style="width:30%"></div>
</div>

<!-- Orange -->
<div class="progress">
   <div class="progress-bar bg-warning" style="width:40%"></div>
</div>

<!-- Red -->
<div class="progress">
  <div class="progress-bar bg-danger" style="width:50%"></div>
</div>

<!-- White -->
<div class="progress border">
  <div class="progress-bar bg-white" style="width:60%"></div>
</div>

<!-- Grey -->
<div class="progress">
  <div class="progress-bar bg-secondary" style="width:70%"></div>
</div>

<!-- Light Grey -->
<div class="progress border">
  <div class="progress-bar bg-light" style="width:80%"></div>
</div>

<!-- Dark Grey -->
<div class="progress">
  <div class="progress-bar bg-dark" style="width:90%"></div>
</div>
```

### Chiziqli progres barlar

<figure><img src="../../.gitbook/assets/image (594).png" alt=""><figcaption></figcaption></figure>

Progres barga chiziqlar qo'shish uchun `.progress-bar-striped` classidan foydalaning:

```
<div class="progress">
  <div class="progress-bar progress-bar-striped" style="width:40%"></div>
</div>
```

### Animatsiyali progres bar

<figure><img src="../../.gitbook/assets/image (590).png" alt=""><figcaption></figcaption></figure>

Progres barni animatsiyali qilish uchun `.progress-bar-animated` classini qo'shing:

```
<div class="progress-bar progress-bar-striped progress-bar-animated" style="width:40%"></div>
```

### Bir nechtalik progres barlar

Progres barlar ham bir joyga to'planishi mumkin:

<figure><img src="../../.gitbook/assets/image (622).png" alt=""><figcaption></figcaption></figure>

```
<div class="progress">
  <div class="progress-bar bg-success" style="width:40%">
    Free Space
  </div>
  <div class="progress-bar bg-warning" style="width:10%">
    Warning
  </div>
  <div class="progress-bar bg-danger" style="width:20%">
    Danger
  </div>
</div>
```
