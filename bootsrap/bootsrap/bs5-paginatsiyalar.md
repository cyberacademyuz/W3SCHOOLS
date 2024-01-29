# BS5 Paginatsiyalar

### Sahifalarni raqamlash

Agar veb-saytingiz ko'p sahifali bo'lsa, har bir sahifaga qandaydir raqam qo'shishni xohlashingiz mumkin.

![](<../../.gitbook/assets/image (107).png>)

Sodda paginatsiya yaratish uchun `<ul>` elementiga `.pagination` classini qo'shing. Keyin har bir `<li>` elementiga `.page-item` va `<li>` ichidagi har bir havolaga `.page-link` classini qo'shing:

```
<ul class="pagination">
  <li class="page-item"><a class="page-link" href="#">Previous</a></li>
  <li class="page-item"><a class="page-link" href="#">1</a></li>
  <li class="page-item"><a class="page-link" href="#">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>
```

### Faol holat

`.active` classi sahifani "ajratib ko'rsatish" uchun ishlatiladi:

![](<../../.gitbook/assets/image (629).png>)

```
<ul class="pagination">
  <li class="page-item"><a class="page-link" href="#">Previous</a></li>
  <li class="page-item"><a class="page-link" href="#">1</a></li>
  <li class="page-item active"><a class="page-link" href="#">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>
```

### Nofaol holat

`.disabled` classi bosilmaydigan havolalar uchun ishlatiladi:

![](<../../.gitbook/assets/image (573).png>)

```
<ul class="pagination">
  <li class="page-item disabled"><a class="page-link" href="#">Previous</a></li>
  <li class="page-item"><a class="page-link" href="#">1</a></li>
  <li class="page-item"><a class="page-link" href="#">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>
```

### Paginatsiya o'lchami

Paginatsiya bloklari ham katta yoki kichikroq o'lchamga ega bo'lishi mumkin:

![](<../../.gitbook/assets/image (584).png>)

Blok o'lchamini katta qilish uchun `.pagination-lg` yoki  kichkina qilish uchun `.pagination-sm` classidan foydalaning:

```
<ul class="pagination pagination-lg">
  <li class="page-item"><a class="page-link" href="#">Previous</a></li>
  <li class="page-item"><a class="page-link" href="#">1</a></li>
  <li class="page-item"><a class="page-link" href="#">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>

<ul class="pagination pagination-sm">
  <li class="page-item"><a class="page-link" href="#">Previous</a></li>
  <li class="page-item"><a class="page-link" href="#">1</a></li>
  <li class="page-item"><a class="page-link" href="#">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>
```

### Paginatsiyani surish

Paginatsiya joylashuvini o'zgartirish uchun utilitalardan foydalaning:

<figure><img src="../../.gitbook/assets/image (621).png" alt=""><figcaption></figcaption></figure>

```
<!-- Default (left-aligned) -->
<ul class="pagination" style="margin:20px 0">
  <li class="page-item">...</li>
</ul>

<!-- Center-aligned -->
<ul class="pagination justify-content-center" style="margin:20px 0">
  <li class="page-item">...</li>
</ul>

<!-- Right-aligned -->
<ul class="pagination justify-content-end" style="margin:20px 0">
  <li class="page-item">...</li>
</ul>
```

### Breadcrumbslar

Paginatsiyalar uchun yana bir ko'rinish - bu breadcrumblar hisoblanadi:

![](<../../.gitbook/assets/image (567).png>)

`.breadcrumb` va `.breadcrumb-item` classlari joriy sahifaning navigatsiya ierarxiyasidagi joylashuvini bildiradi:

```
<ul class="breadcrumb">
  <li class="breadcrumb-item"><a href="#">Photos</a></li>
  <li class="breadcrumb-item"><a href="#">Summer 2017</a></li>
  <li class="breadcrumb-item"><a href="#">Italy</a></li>
  <li class="breadcrumb-item active">Rome</li>
</ul>
```
