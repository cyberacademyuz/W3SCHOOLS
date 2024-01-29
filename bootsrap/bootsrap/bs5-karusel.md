# BS5 Karusel

### Karusel / slayd-shou

Karusel - bu elementlar bo'ylab harakatlanish uchun slayd-shou.

<figure><img src="https://www.w3schools.com/bootstrap5/chicago.jpg" alt=""><figcaption></figcaption></figure>

### Karuselni qanday yaratish kerak

Quyidagi misol indikatorlar va boshqaruv elementlar orqali sodda karuselni qanday yaratish kerakligini ko'rsatadi:

```
<!-- Carousel -->
<div id="demo" class="carousel slide" data-bs-ride="carousel">

  <!-- Indicators/dots -->
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#demo" data-bs-slide-to="0" class="active"></button>
    <button type="button" data-bs-target="#demo" data-bs-slide-to="1"></button>
    <button type="button" data-bs-target="#demo" data-bs-slide-to="2"></button>
  </div>

  <!-- The slideshow/carousel -->
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="la.jpg" alt="Los Angeles" class="d-block w-100">
    </div>
    <div class="carousel-item">
      <img src="chicago.jpg" alt="Chicago" class="d-block w-100">
    </div>
    <div class="carousel-item">
      <img src="ny.jpg" alt="New York" class="d-block w-100">
    </div>
  </div>

  <!-- Left and right controls/icons -->
  <button class="carousel-control-prev" type="button" data-bs-target="#demo" data-bs-slide="prev">
    <span class="carousel-control-prev-icon"></span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#demo" data-bs-slide="next">
    <span class="carousel-control-next-icon"></span>
  </button>
</div>

```

#### Misolni tushuntirish

Yuqoridagi misoldagi har bir class nima qilishining tavsifi:

| Class                         | Ta'rif                                                                                                                                                                                                 |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `.carousel`                   | Karusel yaratadi                                                                                                                                                                                       |
| `.carousel-indicators`        | Karusel uchun indikatorlar qo'shadi. Ular har bir slaydning pastki qismidagi kichik nuqtalardir (bu karuselda nechta slayd borligini va foydalanuvchi hozirda qaysi slaydni ko'rayotganini ko'rsatadi) |
| `.carousel-inner`             | Karuselga slayd qo'shadi                                                                                                                                                                               |
| `.carousel-item`              | Har bir slaydning tarkibini belgilaydi                                                                                                                                                                 |
| `.carousel-control-prev`      | Karuselga chap (oldingi) tugmani qo'shadi, bu foydalanuvchiga slaydlar orasida orqaga qaytish imkonini beradi.                                                                                         |
| `.carousel-control-next`      | Karuselga o'ng (keyingi) tugmani qo'shadi, bu foydalanuvchiga slaydlar orasida oldinga o'tish imkonini beradi.                                                                                         |
| `.carousel-control-prev-icon` | "Orqaga qaytish" tugmachasini yaratish uchun .carousel-control-prev bilan birga ishlatiladi                                                                                                            |
| `.carousel-control-next-icon` | "Keyingi" tugmachasini yaratish uchun .carousel-control-next bilan birga ishlatiladi                                                                                                                   |
| `.slide`                      | Bir elementdan ikkinchisiga o'tishda CSS transition va animatsiya effektini qo'shadi. Agar bunday effektni kerak bo'lmas, classni olib tashlang                                                        |

### Slaydlarga taglavhalar qo'shing

<figure><img src="https://www.w3schools.com/bootstrap5/chicago.jpg" alt=""><figcaption></figcaption></figure>

Har bir slaydga caption yaratish uchun `<div class="carousel-caption">`  ichidagi elementlarni har bir `<div class="carousel-item">` ichiga qo'shing:

```
<div class="carousel-item">
  <img src="la.jpg" alt="Los Angeles">
  <div class="carousel-caption">
    <h3>Los Angeles</h3>
    <p>We had such a great time in LA!</p>
  </div>
</div>
```
