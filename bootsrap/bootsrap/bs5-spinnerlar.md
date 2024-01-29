# BS5 Spinnerlar

### Spinnerlar

Spinner/loader yaratish uchun `.spinner-border` classidan foydalaning:

![](<../../.gitbook/assets/image (356).png>)

```
<div class="spinner-border"></div>
```

### Rangli spinnerlar

Spinnerga rang qo'shish uchun har qanday matn rangini belgilovchi utilitlaridan foydalaning:

![](<../../.gitbook/assets/image (105).png>)

```
<div class="spinner-border text-muted"></div>
<div class="spinner-border text-primary"></div>
<div class="spinner-border text-success"></div>
<div class="spinner-border text-info"></div>
<div class="spinner-border text-warning"></div>
<div class="spinner-border text-danger"></div>
<div class="spinner-border text-secondary"></div>
<div class="spinner-border text-dark"></div>
<div class="spinner-border text-light"></div>
```

### Kattalashuvchi spinnerlar

Agar "aylanuvchi spinner" o'rniga kattalashuvchi spinner/loaderdan foydalanishni hohlasangiz, `.spinner-grow` calssidan foydalaning:

![](<../../.gitbook/assets/image (559).png>)

```
<div class="spinner-grow text-muted"></div>
<div class="spinner-grow text-primary"></div>
<div class="spinner-grow text-success"></div>
<div class="spinner-grow text-info"></div>
<div class="spinner-grow text-warning"></div>
<div class="spinner-grow text-danger"></div>
<div class="spinner-grow text-secondary"></div>
<div class="spinner-grow text-dark"></div>
<div class="spinner-grow text-light"></div>
```

### Spinner o'lchami

Kichikroq spinner yaratish uchun `.spinner-border-sm`  yoki `.spinner-grow-sm` classidan foydalaning:

![](<../../.gitbook/assets/image (617).png>)

```
<div class="spinner-border spinner-border-sm"></div>
<div class="spinner-grow spinner-grow-sm"></div>
```

### Tugmadagi spinnerlar

Tugmaga ham matnli yoki matnsiz spinnerlar qo'shishingiz mumkin:

![](<../../.gitbook/assets/image (459).png>)

```
<button class="btn btn-primary">
  <span class="spinner-border spinner-border-sm"></span>
</button>

<button class="btn btn-primary">
  <span class="spinner-border spinner-border-sm"></span>
  Loading..
</button>

<button class="btn btn-primary" disabled>
  <span class="spinner-border spinner-border-sm"></span>
  Loading..
</button>

<button class="btn btn-primary" disabled>
  <span class="spinner-grow spinner-grow-sm"></span>
  Loading..
</button>
```
