# BS5 Modal

### Modallar

Modal komponenti - bu joriy sahifaning yuqori qismida ko'rsatiladigan dialog oynasi hisoblanadi:

![](<../../.gitbook/assets/image (680).png>)

### Modalni qanday yaratish kerak

Quyidagi misolda oddiy modal qanday yaratilishi ko'rsatilgan:

```
<!-- Button to Open the Modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#myModal">
  Open modal
</button>

<!-- The Modal -->
<div class="modal" id="myModal">
  <div class="modal-dialog">
    <div class="modal-content">

      <!-- Modal Header -->
      <div class="modal-header">
        <h4 class="modal-title">Modal Heading</h4>
        <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
      </div>

      <!-- Modal body -->
      <div class="modal-body">
        Modal body..
      </div>

      <!-- Modal footer -->
      <div class="modal-footer">
        <button type="button" class="btn btn-danger" data-bs-dismiss="modal">Close</button>
      </div>

    </div>
  </div>
</div>
```

### Animatsiya qo'shish

Modalni ochish va yopishda sekin yopilish effektini qo'shish uchun `.fade` classidan foydalaning:

```
<!-- Fading modal -->
<div class="modal fade"></div>

<!-- Modal without animation -->
<div class="modal"></div>
```

### Modal o'lchami

Kichkina modallar uchun `.modal-sm` classini (maksimal kenglik 300px), katta modallar uchun `.modal-lg` classini (maksimal uzunlik 800px) yoki qoʻshimcha katta modallar uchun `.modal-xl` classini (maksimal uzunlik 1140px) qoʻshish orqali modal o'lchamini oʻzgartiring. Standart maksimal uzunlik 500px.

`.modal-dialog` classi bilan `<div>` elementiga o'lcham classini qo'shing:

{% code title="kichik modal" %}
```
<div class="modal-dialog modal-sm">
```
{% endcode %}

{% code title="Katta modal" %}
```
<div class="modal-dialog modal-lg">
```
{% endcode %}

{% code title="Extra Large Modal" %}
```
<div class="modal-dialog modal-xl">
```
{% endcode %}

{% hint style="warning" %}
Odatiy bo'lib, modallarning o'lchami "o'rta" (maksimal kengligi 500px).
{% endhint %}

### To'liq ekranli modalar

Agar modal sahifaning butun uzunligini va balandligini qamrab olishini istasangiz, `.modal-fullscreen` classidan foydalaning:

```
<div class="modal-dialog modal-fullscreen">
```

### Toʻliq ekranli moslashuvchan modalar

Modal o'lchamo qachon toʻliq ekranga moslashishini `.modal-fullscreen-*-*` classlari bilan ham boshqarishingiz mumkin:

| Class                        | Ta'rif                         |
| ---------------------------- | ------------------------------ |
| `.modal-fullscreen-sm-down`  | Toʻliq ekran 576px-dan kichik  |
| `.modal-fullscreen-md-down`  | Toʻliq ekran 768px-dan kichik  |
| `.modal-fullscreen-lg-down`  | Toʻliq ekran 992px-dan kichik  |
| `.modal-fullscreen-xl-down`  | Toʻliq ekran 1200px-dan kichik |
| `.modal-fullscreen-xxl-down` | Toʻliq ekran 1400px-dan kichik |

### Markazda joylashgan modal

Modalni sahifaning qoq o'rtasiga joylashtirish uchun `.modal-dialog-centered` classidan foydalaning:

```
<div class="modal-dialog modal-dialog-centered">
```

### Scroll bo'luvchi modali

Modal ichida juda ko'p kontent bo'lsa, sahifaga scroll paneli qo'shiladi. Buni tushunish uchun quyidagi misollarga qarang:

```
<div class="modal-dialog">
```

Biroq, `.modal-dialog`ga `.modal-dialog-scrollable` ni qo'shish orqali sahifani o'rniga faqat modal ichida scroll qilish mumkin:

```
<div class="modal-dialog modal-dialog-scrollable">
```
