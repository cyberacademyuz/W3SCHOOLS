# BS5 Cardlar

### Cardlar

Bootstrap 5-dagi card - chegarasi mavjud va chegarasida biroz paddingga ega quti hisoblanadi. U sarlavhalar, footerlar, kontent, ranglar va boshqa narsalar uchun har hil variantlarni o'z ichiga oladi.

![](<../../.gitbook/assets/image (108).png>)

### Sodda card

`.card` classi bilan sodda card yaratiladi va uning ichidagi kontentda `.card-body` classi bo'ladi:

<figure><img src="../../.gitbook/assets/image (563).png" alt=""><figcaption></figcaption></figure>

```
<div class="card">
  <div class="card-body">Basic card</div>
</div>
```

### Header va footer

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

`.card-header` classi cardga header qo'shadi, `.card-footer` classi bo'lsa cardga footer qo'shadi:

```
<div class="card">
  <div class="card-header">Header</div>
  <div class="card-body">Content</div>
  <div class="card-footer">Footer</div>
</div>
```

### Tarkibiy cardlar

Cardga orqafon rangini qo'shish uchun tarkibiy classlardan foydalaning (`.bg-primary`, `.bg-success`, `.bg-info`, `.bg-warning`, `.bg-danger`, `.bg-secondary`, `.bg-dark` va `.bg-light`.

<figure><img src="../../.gitbook/assets/image (569).png" alt=""><figcaption></figcaption></figure>

### Sarlavhalar, matn va havolalar

<figure><img src="../../.gitbook/assets/image (596).png" alt=""><figcaption></figcaption></figure>

Har qanday sarlavha elementiga card sarlavhasini qo'shish uchun `.card-title` classidan foydalaning. `.card-text` classi  \<p> elementining pastki marginlarini olib tashlash uchun ishlatiladi, agar o'sha \<p> elementi `.card-body` ichidagi oxirgi (yoki yagona) element bo'lsa.

```
<div class="card">
  <div class="card-body">
    <h4 class="card-title">Card title</h4>
    <p class="card-text">Some example text. Some example text.</p>
    <a href="#" class="card-link">Card link</a>
    <a href="#" class="card-link">Another link</a>
  </div>
</div>
```

### Card rasmlari

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

Rasmni cardning yuqori yoki pastki qismiga joylashtirish uchun `<img>` elementiga `.card-img-top` yoki `.card-img-bottom` c;assini qo'shing . Biz butun widthni qamrab olish uchun rasmni `.card-body` dan tashqarida berganimizga e'tibor qiling:

```
<div class="card" style="width:400px">
  <img class="card-img-top" src="img_avatar1.png" alt="Card image">
  <div class="card-body">
    <h4 class="card-title">John Doe</h4>
    <p class="card-text">Some example text.</p>
    <a href="#" class="btn btn-primary">See Profile</a>
  </div>
</div>
```

### Cardni rasm bilan qoplab olish

![](<../../.gitbook/assets/image (589).png>)

Rasmni cardning orqafoniga aylantiring va rasm ustiga matn yozish uchun `.card-img-overlay` classidan foydalaning:

```
<div class="card" style="width:500px">
  <img class="card-img-top" src="img_avatar1.png" alt="Card image">
  <div class="card-img-overlay">
    <h4 class="card-title">John Doe</h4>
    <p class="card-text">Some example text.</p>
    <a href="#" class="btn btn-primary">See Profile</a>
  </div>
</div>
```
