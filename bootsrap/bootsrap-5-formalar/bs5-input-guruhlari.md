# BS5 Input guruhlari

### Input guruhlari

`.input-group` classi input maydonining oldiga yoki orqasiga "yordamchi matn" sifatida ikonka, matn yoki tugma qo'shish orqali inputni tushunarli qilishga mo'ljallangan konteynerdir.

Kerakli yordamchi matnni berish uchun `.input-group-text` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

```
<form>
  <div class="input-group">
    <span class="input-group-text">@</span>
    <input type="text" class="form-control" placeholder="Username">
  </div>

  <div class="input-group">
    <input type="text" class="form-control" placeholder="Your Email">
    <span class="input-group-text">@example.com</span>
  </div>
</form>
```

### Guruh o'lchamini kiriting

Kichik input guruhlari uchun `.input-group-sm` classidan va katta input guruhlari uchun `.input-group-lg` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

```
<div class="input-group mb-3 input-group-sm">
   <span class="input-group-text">Small</span>
  <input type="text" class="form-control">
</div>

<div class="input-group mb-3">
  <span class="input-group-text">Default</span>
  <input type="text" class="form-control">
</div>

<div class="input-group mb-3 input-group-lg">
  <span class="input-group-text">Large</span>
  <input type="text" class="form-control">
</div>
```

### Bir nechtalik inputlar va qo'shimcha komponentlar

Bir nechtalik input yoki qo'shimcha komponent qo'shish:

<figure><img src="../../.gitbook/assets/image (301).png" alt=""><figcaption></figcaption></figure>

```
<!-- Multiple inputs -->
<div class="input-group mb-3">
  <span class="input-group-text">Person</span>
  <input type="text" class="form-control" placeholder="First Name">
  <input type="text" class="form-control" placeholder="Last Name">
</div>

<!-- Multiple addons / help text -->
<div class="input-group mb-3">
  <span class="input-group-text">One</span>
  <span class="input-group-text">Two</span>
  <span class="input-group-text">Three</span>
  <input type="text" class="form-control">
</div>
```

### Input guruhida checkboxlar va Radiolar &#x20;

Matn o'rniga checkbox yoki radio tugmalaridan ham foydalanishingiz mumkin:

<figure><img src="../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

```
<div class="input-group mb-3">
  <div class="input-group-text">
    <input type="checkbox">
  </div>
  <input type="text" class="form-control" placeholder="Some text">
</div>

<div class="input-group mb-3">
  <div class="input-group-text">
    <input type="radio">
  </div>
  <input type="text" class="form-control" placeholder="Some text">
</div>
```

### Input guruh tugmalari

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

```
<div class="input-group mb-3">
  <button class="btn btn-outline-primary" type="button">Basic Button</button>
  <input type="text" class="form-control" placeholder="Some text">
</div>

<div class="input-group mb-3">
  <input type="text" class="form-control" placeholder="Search">
  <button class="btn btn-success" type="submit">Go</button>
</div>

<div class="input-group mb-3">
  <input type="text" class="form-control" placeholder="Something clever..">
  <button class="btn btn-primary" type="button">OK</button>
  <button class="btn btn-danger" type="button">Cancel</button>
</div>
```

### Dropdown tugmasi bilan input guruh

Input guruhiga dropdown tugma qo'shing. Sizga odatdagi `.dropdown` o'rab turuvchisi kerak emasligini unutmang.

<figure><img src="../../.gitbook/assets/image (285).png" alt=""><figcaption></figcaption></figure>

```
<div class="input-group mt-3 mb-3">
  <button type="button" class="btn btn-primary dropdown-toggle" data-bs-toggle="dropdown">
    Dropdown button
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">Link 1</a></li>
    <li><a class="dropdown-item" href="#">Link 2</a></li>
    <li><a class="dropdown-item" href="#">Link 3</a></li>
  </ul>
  <input type="text" class="form-control" placeholder="Username">
</div>
```
