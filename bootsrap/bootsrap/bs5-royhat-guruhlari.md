# BS5 Ro'yhat guruhlari

### Boshlang'ich ro'yxat guruhlari

Eng oddiy ro'yxat guruhi - bu ro'yxat elementlaridan tashkil topgan tartibsiz ro'yxat hisoblanadi:

<figure><img src="../../.gitbook/assets/image (599).png" alt=""><figcaption></figcaption></figure>

Sodda ro'yxat guruhini yaratish uchun `<ul>` elementini  `.list-group` classi bilan va `<li>` elementini `.list-group-item` classi bilan ishlating:

```
<ul class="list-group">
  <li class="list-group-item">First item</li>
  <li class="list-group-item">Second item</li>
  <li class="list-group-item">Third item</li>
</ul>
```

### Faol holat

<figure><img src="../../.gitbook/assets/image (585).png" alt=""><figcaption></figcaption></figure>

Joriy elementni ajratib ko'rsatish uchun `.active` classidan foydalaning:

```
<ul class="list-group">
  <li class="list-group-item active">Active item</li>
  <li class="list-group-item">Second item</li>
  <li class="list-group-item">Third item</li>
</ul>
```

### Havolali elementlar bilan guruh ro'yxatini yaratish

<figure><img src="../../.gitbook/assets/image (566).png" alt=""><figcaption></figcaption></figure>

Havolali elementlar bilan ro'yxat guruhini yaratish uchun `<div>` elementi o'rniga `<ul>`va `<li>`o'rniga \<a> elementidan foydalaning. Kursorni havola ustiga olib borganda orqafonning rangini kulrang qilishni xohlasangiz, `.list-group-item-action`  classini qo'shing:

```
<div class="list-group">
  <a href="#" class="list-group-item list-group-item-action">First item</a>
  <a href="#" class="list-group-item list-group-item-action">Second item</a>
  <a href="#" class="list-group-item list-group-item-action">Third item</a>
</div>
```

### O'chirib qo'yilgan element

`.disabled` classi o'chirib qo'yilgan elementga ochiqroq matn rangini qo'shadi. Va havolani va undagi hover effektini olib tashlaydi:

<figure><img src="../../.gitbook/assets/image (587).png" alt=""><figcaption></figcaption></figure>

```
<div class="list-group">
  <a href="#" class="list-group-item disabled">Disabled item</a>
  <a href="#" class="list-group-item disabled">Disabled item</a>
  <a href="#" class="list-group-item">Third item</a>
</div>
```

### Chegaralarni olib tashlash

Ba'zi chegaralar va yumaloq burchaklarni olib tashlash uchun `.list-group-flush` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (830).png" alt=""><figcaption></figcaption></figure>

```
<ul class="list-group list-group-flush">
  <li class="list-group-item">First item</li>
  <li class="list-group-item">Second item</li>
  <li class="list-group-item">Third item</li>
  <li class="list-group-item">Fourth item</li>
</ul>
```

### Raqamli ro'yxat guruhlari

Raqamli ro'yxat elementlarini yaratish uchun `.list-group-numbered` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure>

```
<ol class="list-group list-group-numbered">
  <li class="list-group-item">First item</li>
  <li class="list-group-item">Second item</li>
  <li class="list-group-item">Third item</li>
</ol>
```

### Gorizontal ro'yxat guruhlari

Agar roʻyxat elementlarini yonma yon  koʻrsatilishini istasangiz `.list-group` classiga `.list-group-horizontal` classini qo'shing:

![](<../../.gitbook/assets/image (597).png>)

```
<ul class="list-group list-group-horizontal">
  <li class="list-group-item">First item</li>
  <li class="list-group-item">Second item</li>
  <li class="list-group-item">Third item</li>
  <li class="list-group-item">Fourth item</li>
</ul>
```

### Tarkibiy classlar

Tarkibiy classlar ro'yxat elementlariga rang qo'shish uchun ishlatilishi mumkin:

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

Ro'yxat elementlarini bo'yovchi classlar quyidagilardir: `.list-group-item-success`, `list-group-item-secondary`, `list-group-item-info`, `list-group-item-warning`, `.list-group-item-danger`, `.list-group-item-primary`, `list-group-item-dark` va `list-group-item-light`,:

```
<ul class="list-group">
  <li class="list-group-item list-group-item-success">Success item</li>
  <li class="list-group-item list-group-item-secondary">Secondary item</li>
  <li class="list-group-item list-group-item-info">Info item</li>
  <li class="list-group-item list-group-item-warning">Warning item</li>
  <li class="list-group-item list-group-item-danger">Danger item</li>
  <li class="list-group-item list-group-item-primary">Primary item</li>
  <li class="list-group-item list-group-item-dark">Dark item</li>
  <li class="list-group-item list-group-item-light">Light item</li>
</ul>
```

### Havolali elementlar bilan tarkibiy classlar

<figure><img src="../../.gitbook/assets/image (539).png" alt=""><figcaption></figcaption></figure>

```
<div class="list-group">
  <a href="#" class="list-group-item list-group-item-action">Action item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-success">Success item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-secondary">Secondary item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-info">Info item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-warning">Warning item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-danger">Danger item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-primary">Primary item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-dark">Dark item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-light">Light item</a>
</div>
```

### Beyjlar bilan ro'yhat guruhi

Roʻyxat guruhiga beyj qoʻshish uchun `.badge` classi bilan yordamchi utilitalar qo'shing:

<figure><img src="../../.gitbook/assets/image (561).png" alt=""><figcaption></figcaption></figure>

```
<ul class="list-group">
  <li class="list-group-item d-flex justify-content-between align-items-center">
    Inbox
    <span class="badge bg-primary rounded-pill">12</span>
  </li>
  <li class="list-group-item d-flex justify-content-between align-items-center">
    Ads
    <span class="badge bg-primary rounded-pill">50</span>
  </li>
  <li class="list-group-item d-flex justify-content-between align-items-center">
    Junk
    <span class="badge bg-primary rounded-pill">99</span>
  </li>
</ul>
```
