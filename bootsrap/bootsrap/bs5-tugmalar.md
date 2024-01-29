# BS5 Tugmalar

## Tugma stillari

Bootstrap 5 turli xil stilga ega tugmalar taqdim qiladi:

<figure><img src="../../.gitbook/assets/image (608).png" alt=""><figcaption></figcaption></figure>

```
<button type="button" class="btn">Basic</button>
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-dark">Dark</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-link">Link</button>
```

Tugma classlari  `<a>`, `<button>`, yoki `<input>`elementlarda ishlatilishi mumkin:

```
<a href="#" class="btn btn-success">Link Button</a>
<button type="button" class="btn btn-success">Button</button>
<input type="button" class="btn btn-success" value="Input Button">
<input type="submit" class="btn btn-success" value="Submit Button">
<input type="reset" class="btn btn-success" value="Reset Button">
```

{% hint style="warning" %}
**Nima uchun havolaning href atributiga # qo'yamiz ?**\
\
Bizda tugmani bosganda yo'naltiriladigan sahifa yo'qligi va "404" xabarini olmasligimiz uchun havola sifatida **#** qo'yamiz. Real hayotda bu albatta, "Qidiruv" sahifasining URL manzili bo'lishi kerak.
{% endhint %}

### Button outline-i

Bootstrap 5, sakkizta outline/chegarali tugmalar taqdim qiladi.

Qo'shimcha "hover" effektini ko'rish uchun sichqonchani ularning ustiga olib boring:

<figure><img src="../../.gitbook/assets/image (625).png" alt=""><figcaption></figcaption></figure>

```
<button type="button" class="btn btn-outline-primary">Primary</button>
<button type="button" class="btn btn-outline-secondary">Secondary</button>
<button type="button" class="btn btn-outline-success">Success</button>
<button type="button" class="btn btn-outline-info">Info</button>
<button type="button" class="btn btn-outline-warning">Warning</button>
<button type="button" class="btn btn-outline-danger">Danger</button>
<button type="button" class="btn btn-outline-dark">Dark</button>
<button type="button" class="btn btn-outline-light text-dark">Light</button>
```

### Tugma o'lchamlari

Katta tugmalar yaratish uchun `.btn-lg` classidan yoki kichik tugmalar yaratish uchun `.btn-sm` classidan foydalaning:

![](<../../.gitbook/assets/image (568).png>)

```
<button type="button" class="btn btn-primary btn-lg">Large</button>
<button type="button" class="btn btn-primary">Default</button>
<button type="button" class="btn btn-primary btn-sm">Small</button>
```

### Block darajali tugmalar

Ota elementning butun kengligini qamrab oladigan block darajasidagi tugma yaratish uchun ota elementida `.d-grid` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (619).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-grid">
  <button type="button" class="btn btn-primary btn-block">Full-Width Button</button>
</div>
```

Agar block-darajali tugmalaringiz ko'p bo'lsa, ular orasidagi bo'sh joyni `.gap-*` classi bilan boshqarishingiz mumkin:

<figure><img src="../../.gitbook/assets/image (580).png" alt=""><figcaption></figcaption></figure>

```
<div class="d-grid gap-3">
  <button type="button" class="btn btn-primary btn-block">Full-Width Button</button>
  <button type="button" class="btn btn-primary btn-block">Full-Width Button</button>
  <button type="button" class="btn btn-primary btn-block">Full-Width Button</button>
</div>
```

### Active/Disabled tugmalar

Tugmani aktiv (bosish mumkin) yoki o'chirilgan (bosilmaydigan) qilib qo'ysh mumkin:

![](<../../.gitbook/assets/image (833).png>)

`.active` classi tugmani bosiluvchan qiladi va `disabled` atributi esa tugmani bosib bo'lmaydigan qiladi. E'tibor bering, \<a> elementlari disabled atributini qo'llab-quvvatlamaydi va shuning uchun uni vizual ravishda o'chirib qo'yish uchun `.disabled` classidan foydalanish kerak.

```
<button type="button" class="btn btn-primary active">Active Primary</button>
<button type="button" class="btn btn-primary" disabled>Disabled Primary</button>
<a href="#" class="btn btn-primary disabled">Disabled Link</a>
```

### Spinner tugmalar

Bundan tashqari, tugmachaga "spinnerlar" qo'shishingiz mumkin, bu haqda [**BS5 Spinner qo'llanmasida**](bs5-spinnerlar.md) ko'proq bilib olasiz:

![](<../../.gitbook/assets/image (460).png>)

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
