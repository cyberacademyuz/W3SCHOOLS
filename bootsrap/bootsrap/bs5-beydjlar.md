# BS5 Beydjlar

### Beyjlar

Beyjlar har qanday tarkibga qo'shimcha ma'lumot kiritish uchun ishlatiladi:

![](<../../.gitbook/assets/image (190).png>)

Toʻgʻri burchakli beyjlar yaratish uchun `.badge` classidan \<span> elementlari ichida tarkibiy class (masalan `.bg-secondary`) bilan birga foydalaning. E'tibor bering, beyjlar ota elementning o'lchamiga mos kelishi uchun o'lchami o'zgaradi:

```
<h1>Example heading <span class="badge bg-secondary">New</span></h1>
<h2>Example heading <span class="badge bg-secondary">New</span></h2>
<h3>Example heading <span class="badge bg-secondary">New</span></h3>
<h4>Example heading <span class="badge bg-secondary">New</span></h4>
<h5>Example heading <span class="badge bg-secondary">New</span></h5>
<h6>Example heading <span class="badge bg-secondary">New</span></h6>
```

### Tarkibiy beyjlar

<figure><img src="../../.gitbook/assets/image (592).png" alt=""><figcaption></figcaption></figure>

Beyj rangini o'zgartirish uchun har qanday tarkibiy classlardan (`.bg-*`) foydalaning:

```
<span class="badge bg-primary">Primary</span>
<span class="badge bg-secondary">Secondary</span>
<span class="badge bg-success">Success</span>
<span class="badge bg-danger">Danger</span>
<span class="badge bg-warning">Warning</span>
<span class="badge bg-info">Info</span>
<span class="badge bg-light">Light</span>
<span class="badge bg-dark">Dark</span>
```

### Yumoloq sifat beyjlar

![](<../../.gitbook/assets/image (43).png>)

Beyjlarni yumaloqroq qilish uchun `.rounded-pill` classidan foydalaning:

```
<span class="badge rounded-pill bg-primary">Primary</span>
<span class="badge rounded-pill bg-secondary">Secondary</span>
<span class="badge rounded-pill bg-success">Success</span>
<span class="badge rounded-pill bg-danger">Danger</span>
<span class="badge rounded-pill bg-warning">Warning</span>
<span class="badge rounded-pill bg-info">Info</span>
<span class="badge rounded-pill bg-light">Light</span>
<span class="badge rounded-pill bg-dark">Dark</span>
```

### Element ichidagi beyj

Tugma ichida beyjdan foydalanishga misol:

![](<../../.gitbook/assets/image (627).png>)

```
<button type="button" class="btn btn-primary">
  Messages <span class="badge bg-danger">4</span>
</button>
```
