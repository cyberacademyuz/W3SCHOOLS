# CSS Paginatsiyalar

CSS yordamida moslashuvchan paginatsiyalarni yaratishni o'rganing.

### Oddiy paginatsiya

Agar veb-saytingiz ko'p sahifali bo'lsa, har bir sahifaga qandaydir paginatsiya turini qo'shishni xohlashingiz mumkin:

<figure><img src="../../.gitbook/assets/image (383).png" alt=""><figcaption></figcaption></figure>

```
.pagination {
  display: inline-block;
}

.pagination a {
  color: black;
  float: left;
  padding: 8px 16px;
  text-decoration: none;
}
```

### Aktiv va hoverli paginatsiyalar

![](<../../.gitbook/assets/image (420).png>)

Joriy sahifani `.active` classi bilan ajratib ko'rsating va sichqonchani ularning ustiga olib borilganida har bir sahifa havolasining rangini o'zgartirish uchun `:hover` selektoridan foydalaning:

```
.pagination a.active {
  background-color: #4CAF50;
  color: white;
}

.pagination a:hover:not(.active) {background-color: #ddd;}
```

#### Aktiv va hoverli yumaloqsimon tugmalar

![](<../../.gitbook/assets/image (429).png>)

Agar tugmani aktiv va hover holatida yumaloqsimon bo'lishini hohlasangiz, unga `border-radius` xususiyatni qo‘shing:

```
.pagination a {
  border-radius: 5px;
}

.pagination a.active {
  border-radius: 5px;
}
```

#### Hoverali transition effekti

![](<../../.gitbook/assets/image (407).png>)

Hover bolganda transition effektini yaratish uchun `transition` xususiyatini sahifa havolalariga qoʻshing:

```
.pagination a {
  transition: background-color .3s;
}
```

### Chegarali paginatsiya

![](<../../.gitbook/assets/image (340).png>)

Paginatsiyaga chegaralar qo'shish uchun `border` xususiyatidan foydalaning:

```
.pagination a {
  border: 1px solid #ddd; /* Gray */
}
```

#### Dumaloqsimon chegaralar

**Maslahat:** Paginatsiyadagi birinchi va oxirgi havolaga yumaloqsimon chegara qo'shing:

![](<../../.gitbook/assets/image (369).png>)

```
.pagination a:first-child {
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
}

.pagination a:last-child {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
}
```

#### Havolalar orasidagi bo'sh joy

**Maslahat:** Agar sahifa havolalarini guruhlamasangiz, `margin` xususiyatni qo'shing:

![](<../../.gitbook/assets/image (756).png>)

```
.pagination a {
  margin: 0 4px; /* 0 is for top and bottom. Feel free to change it */
}
```

### Paginatsiya o'lchami

![](<../../.gitbook/assets/image (415).png>)

`font-size` xususiyati orqali paginatsiya o'lchamini o'zgartiring:

```
.pagination a {
  font-size: 22px;
}
```

### O'rtaga joylashtirilgan paginatsiya

<figure><img src="../../.gitbook/assets/image (509).png" alt=""><figcaption></figcaption></figure>

Paginatsiyani o'rtaga olib kelish uchun uning konteyner elementini (masalan, \<div>) `text-align:center;` bilan o'rab oling.

```
.center {
  text-align: center;
}
```

### Ko'proq misollar

<figure><img src="../../.gitbook/assets/image (748).png" alt=""><figcaption></figcaption></figure>

### Breadcrumbs

<figure><img src="../../.gitbook/assets/image (370).png" alt=""><figcaption></figcaption></figure>

Paginatsiyaning yana bir varyanti "breadcrumbs" deb ataladi:

```
ul.breadcrumb {
  padding: 8px 16px;
  list-style: none;
  background-color: #eee;
}

ul.breadcrumb li {display: inline;}

ul.breadcrumb li+li:before {
  padding: 8px;
  color: black;
  content: "/\00a0";
}
```
