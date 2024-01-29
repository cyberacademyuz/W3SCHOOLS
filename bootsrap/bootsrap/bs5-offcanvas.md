# BS5 Offcanvas

### Tuvaldan tashqari

Offcanvas modallarga o'xshaydi (standart holda ko'rimaydi va ishga tushirilganda ko'rsatiladi), bundan tashqari ko'pincha yon tomonda ko'rsatiladigan navbar sifatida ishlatiladi.

![](<../../.gitbook/assets/image (724).png>)

### Offcanvas qanday yaratish mumkin

Quyidagi misolda offcanvas sidebarini qanday yaratish kerakligi ko'rsatilgan:

```
<!-- Offcanvas Sidebar -->
<div class="offcanvas offcanvas-start" id="demo">
  <div class="offcanvas-header">
    <h1 class="offcanvas-title">Heading</h1>
    <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas"></button>
  </div>
  <div class="offcanvas-body">
    <p>Some text lorem ipsum.</p>
    <p>Some text lorem ipsum.</p>
    <button class="btn btn-secondary" type="button">A Button</button>
  </div>
</div>

<!-- Button to open the offcanvas sidebar -->
<button class="btn btn-primary" type="button" data-bs-toggle="offcanvas" data-bs-target="#demo">
  Open Offcanvas Sidebar
</button
```

#### Misolni tushuntirish

`.offcanvas` classi offcanvas sidebarini yaratadi.

`.offcanvas-start` classi kanvasni joylashtiradi va uning uzunligini 400px qiladi. Qo'shimcha  joylashuv classlari uchun quyidagi misollarga qarang.

`.offcanvas-title` classi mos keladigan margin va line-height bilan ta'minlaydi.

Keyin kontentlarni `.offcanvas-body` classi ichida joylashtiring.

Offcanvas sidebarini ochish uchun `.offcanvas` konteynerining id-si murojaat qiluvchi `<button>` yoki \<a> elementidan foydalanishingiz kerak (bizning misolda `#demo`).

Offcanvas sidebarini `<a>` elementi bilan ochish uchun `#demodata-bs-target` atributi o‘rniga `href` atributiga murojaat qilishingiz qilishingiz mumkin.

### Offcanvas joylashuvi

Offcanvasni chapga, o'ngga, yuqoriga yoki pastga joylashtirish uchun quyidagi classlardan foydalaning: `.offcanvas-start|end|top|bottom`

{% code title="To'g'ri misol" %}
```
<div class="offcanvas offcanvas-end" id="demo">
```
{% endcode %}

![](<../../.gitbook/assets/image (673).png>)

{% code title="Yuqori misol" %}
```
<div class="offcanvas offcanvas-top" id="demo">
```
{% endcode %}

![](<../../.gitbook/assets/image (678).png>)

{% code title="pastki misol" %}
```
<div class="offcanvas offcanvas-bottom" id="demo">
```
{% endcode %}

![](<../../.gitbook/assets/image (661).png>)

### Moslashuvchan Offcanvas menyusi

Bundan tashqari, `.offcanvas-sm|md|lg|xl|xxl` classlari yordamida turli ekranlar mos keladigam offcanvas menyusini berkirish yoki ko'rsatishni ham boshqarishingiz mumkin:

```
<div class="offcanvas offcanvas-start offcanvas-lg" id="demo">
```

### To'q rangli Offcanvas menyusi

To'q rangli offcanvas menyu yaratish uchun `.text-bg-dark` classidan foydalaning.

**Maslahat:** Toʻq fonda chiroyli koʻrinadigan oq rangli yopish tugmachasini yaratish uchun `btn-close`-ga `.btn-close-white` classini ham qoʻshdik:

```
<div class="offcanvas offcanvas-end" id="demo">
<button type="button" class="btn-close btn-close-white" data-bs-dismiss="offcanvas"></button>
```
