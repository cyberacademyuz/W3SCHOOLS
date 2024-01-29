# BS5 Dropdownlar

### Sodda dropdown menyu

Dropdown menyu - o'zgaruvchan menyu bo'lib, u foydalanuvchiga oldinroq yaratilgan ro'yxat ichidan bitta qiymat tanlash imkonini beradi:

![](<../../.gitbook/assets/image (605).png>)

```
<div class="dropdown">
  <button type="button" class="btn btn-primary dropdown-toggle" data-bs-toggle="dropdown">
    Dropdown button
  </butto>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">Link 1</a></li>
    <li><a class="dropdown-item" href="#">Link 2</a></li>
    <li><a class="dropdown-item" href="#">Link 3</a></li>
  </ul>
</div>
```

#### Misolni tushuntirish

`.dropdown` classi dropdown menyu yaratadi.

Dropdown menyuni ochish uchun `.dropdown-toggle` va `data-bs-toggle="dropdown"` atributiga ega tugma yoki havoladan foydalaning.&#x20;

Dropdown menyu yaratish uchun `<div>` elementiga `.dropdown-menu` classini qo'shing. Keyin dropdown menyu ichidagi har bir elementga (havolalar yoki tugmalar) `.dropdown-item` classini qo'shing.

### Ajralib turuvchi elementli dropdown

![](<../../.gitbook/assets/image (73).png>)

Dropdown menyu ichidagi havolalarni ingichka gorizontal chegara bilan ajratish uchun `.dropdown-divider` classi ishlatiladi:

```
<li><hr class="dropdown-divider"></hr></li>
```

### Sarlavhali dropdown

![](<../../.gitbook/assets/image (73).png>)

`.dropdown-header` classi dropdwon menyuga sarlavha qo'shish uchun ishlatiladi:

```
<li><h5 class="dropdown-header">Dropdown header 1</h5></li>
```

### O'chirib qo'yilgan va aktiv elementlar

![](<../../.gitbook/assets/image (557).png>)

`.active` classi bilan dropdownning ma'lum bir elementni ajratib ko'rsatish (ko'k fon rangi qo'shiladi) mumkin.

Dropdown menyudagi elementni o'chirib qo'yish uchun `.disabled` classidan foydalaning (och kulrangli matn va oddiy kursor" belgisini o'z ichiga oladi):

```
<li><a class="dropdown-item" href="#">Normal</a></li>
<li><a class="dropdown-item active" href="#">Active</a></li>
<li><a class="dropdown-item disabled" href="#">Disabled</a></li>
```

### Dropdownning ochilish joyi

![](<../../.gitbook/assets/image (637).png>)

Shuningdek, ochiladigan elementga `.dropend` yoki `.dropstart` classini qo'shish orqali "dropend" yoki "dropstart" menyusini yaratishingiz mumkin. O'ng yoki chapga qaragn strellka avtomatik ravishda qo'shilishini unutmang:

{% code title="Dropright" %}
```
<div classg="dropdown dropend">
```
{% endcode %}

{% code title="Dropleft" %}
```
<div class="dropdown dropstart">
```
{% endcode %}

### O'ngga ochiladigan dropdown menyu&#x20;

![](<../../.gitbook/assets/image (702).png>)

Ochiladigan menyuni o'ng tomonga surish uchun elementga `.dropdown-menu-end` classini .dropdown-menu classi bilan birga qo'shing:

```
<div class="dropdown-menu dropdown-menu-end">
```

### Dropup

![](<../../.gitbook/assets/image (711).png>)

Agar dropdown menyu pastga emas, tepaga qarab ochilishini istasangiz, \<div> elementidagi class="dropdown"ni `"dropup"` classi bilan o'zgartiring:

```
<div class="dropup">
```

### Dropdownda matn

![](<../../.gitbook/assets/image (550).png>)

`.dropdown-item-text` classi dropdown menyu elementiga oddiy matn qo'shish uchun ishlatiladi yoki standart havola stilidagi havolalar qo'shish uchun ishlatiladi.

```
<ul class="dropdown-menu">
  <li><a class="dropdown-item" href="#">Link 1</a></li>
  <li><a class="dropdown-item" href="#">Link 2</a></li>
  <li><a class="dropdown-item" href="#">Link 3</a></li>
  <li><a class="dropdown-item-text" href="#">Text Link</a></li>
  <li><span class="dropdown-item-text">Just Text</span></li>
</ul>
```

### Dropdown menyu bilan guruhlangan tugmalar

![](<../../.gitbook/assets/image (712).png>)

```
<div class="btn-group">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <div class="btn-group">
    <button type="button" class="btn btn-primary dropdown-toggle" data-bs-toggle="dropdown">Sony</button>
    <ul class="dropdown-menu">
      <li><a class="dropdown-item" href="#">Tablet</a></li>
      <li><a class="dropdown-item" href="#">Smartphone</a></li>
    </ul>
  </div>
</div>
```

### Dropdown menyu bilan vertikal tugmalar guruhi

![](<../../.gitbook/assets/image (657).png>)

```
<div class="btn-group-vertical">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <div class="btn-group">
    <button type="button" class="btn btn-primary dropdown-toggle" data-bs-toggle="dropdown">Sony</button>
    <ul class="dropdown-menu">
      <li><a class="dropdown-item" href="#">Tablet</a></li>
      <li><a class="dropdown-item" href="#">Smartphone</a></li>
    </ul>
  </div>
</div>
```
