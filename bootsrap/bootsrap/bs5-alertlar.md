# BS5 Alertlar

### Alertlar

Bootstrap 5 ogohlantirish xabarlarini yaratishning osonroq usulini taqdim qiladi:

<figure><img src="../../.gitbook/assets/image (457).png" alt=""><figcaption></figcaption></figure>

Ogohlantirishlar `.alert` klassi, undan keyin `.alert-success`, `.alert-info`, `.alert-warning`, `.alert-danger`, `.alert-primary`, `.alert-secondary`, `.alert-light` yoki `.alert-dark` kabi kontekstli classlardan biri orqali yaratiladi.

```
<div class="alert alert-success">
  <strong>Success!</strong> Indicates a successful or positive action.
</div>
```

### Ogohlantirish havolalari

`.alert-link` classini "mos rangli havolalar" yaratish uchun ogohlantirish oynasi ichidagi har qanday havolalarga qo'shing:

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

```
<div class="alert alert-success">
  <strong>Success!</strong> You should <a href="#" class="alert-link">read this message</a>.
</div>
```

### Alertlarni yopish

<figure><img src="../../.gitbook/assets/image (586).png" alt=""><figcaption></figcaption></figure>

Ogohlantirish xabarini yopish uchun alert konteyneriga `.alert-dismissible` classini qo'shing. Keyin \<a> yoki \<button> elementiga `class="btn-close"` va `data-bs-dismiss="alert"` classini qo'shing (uni bosganingizda ogohlantirish oynasi yo'qoladi).

```
<div class="alert alert-success alert-dismissible">
  <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
  <strong>Success!</strong> This alert box could indicate a successful or positive action.
</div>
```

### Animatsiyali alertlar

Ogohlantirish xabarini yopayotganda `.fade` va `.show` classlari sekin yo'q bolish effektini qo'shadi:

```
<div class="alert alert-danger alert-dismissible fade show">
```
