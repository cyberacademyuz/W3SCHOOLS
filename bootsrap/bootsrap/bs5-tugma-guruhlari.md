# BS5 Tugma guruhlari

### Tugma guruhlari

Bootstrap 5 tugma guruhida bir qator tugmalarni (bitta satrda) guruhlash imkonini beradi:

![](<../../.gitbook/assets/image (582).png>)

Tugmalar guruhini yaratish uchun `.btn-group` classi bilan `<div>` elementidan foydalaning:

```
<div class="btn-group">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <button type="button" class="btn btn-primary">Sony</button>
</div>
```

**Maslahat:** Guruhdagi har bir tugma uchun tugma oʻlchamlarini berish oʻrniga katta tugmalar guruhi uchun `.btn-group-lg` yoki kichik tugmalar guruhi uchun `.btn-group-sm` classidan foydalaning:

**Katta tugmalar:**

![](<../../.gitbook/assets/image (583).png>)

**Standart tugmalar:**

![](<../../.gitbook/assets/image (628).png>)

**Kichik tugmalar:**

![](<../../.gitbook/assets/image (616).png>)

```
<div class="btn-group btn-group-lg">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <button type="button" class="btn btn-primary">Sony</button>
</div>
```

### Vertikal tugmalar guruhi

Bootstrap 5 vertikal tugmalar guruhini ham qo'llab-quvvatlaydi:

![](<../../.gitbook/assets/image (102).png>)

Vertikal tugmalar guruhini yaratish uchun `.btn-group-vertical` classidan foydalaning:

```
<div class="btn-group-vertical">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <button type="button" class="btn btn-primary">Sony</button>
</div>
```

### Tugma guruhlari yonma-yon

Tugma guruhlari default tarzda "inline" hisoblanadi, bu bir nechta guruhlar mavjud bo'lganida ularni yonma-yon ko'rinishga olib keladi:

![](<../../.gitbook/assets/image (116).png>)

```
<div class="btn-group">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <button type="button" class="btn btn-primary">Sony</button>
</div>

<div class="btn-group">
  <button type="button" class="btn btn-primary">BMW</button>
  <button type="button" class="btn btn-primary">Mercedes</button>
  <button type="button" class="btn btn-primary">Volvo</button>
</div>
```

### Tugma guruhlarini joylashtirish va dropdown menyular

![](<../../.gitbook/assets/image (114).png>)

Dropdown menyular yaratish uchun tugma guruhlarini joylashtirish (keyingi bo'limda dropdown menyular haqida ko'proq bilib olasiz):

```
<div class="btn-group">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <div class="btn-group">
    <button type="button" class="btn btn-primary dropdown-toggle" data-bs-toggle="dropdown">Sony</button>
    <div class="dropdown-menu">
      <a class="dropdown-item" href="#">Tablet</a>
      <a class="dropdown-item" href="#">Smartphone</a>
    </div>
  </div>
</div>
```
