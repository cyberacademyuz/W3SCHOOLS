---
description: >-
  Responsive veb-dizayn barcha qurilmalarda to'g'ri ko'rinadigan veb-sahifalar
  yaratishdir! Responsive veb-dizayn avtomatik tarzda turli ekran o'lchamlari va
  viewportlarga moslashadi
---

# Responsive

## Moslashuvchan veb dizayn nima ?

Responsive veb-dizayn veb sahifani barcha qurilmalar (PC, planshetlar va telefonlar)da  to'g'ri ko'rinishi uchun veb-sayt o'lchami avtomatik ravishda o'zgartirish, yashirish, kichraytirish yoki kattalashtirish uchun HTML va CSS-dan foydalanishdir.

## Viewportni sozlash

Moslashuvchan veb-sayt yaratish uchun barcha veb-sahifalaringizga quyidagi \<meta> tegni qo'shing:

```
<meta name="viewport" content="width=device-width, initial-scale=1.0"> 
```

Bu sizning sahifangizning viewportini o'rnatadi, u brauzerga sahifa o'lchamlari va masshtabini to'g'rlash bo'yicha ko'rsatmalar beradi.

_Bu bir sahifaning viewport berilgan va berilmagan holatdagi ko'rinishiga misol:_

&#x20;                              [![](<../../.gitbook/assets/image (210).png>)](https://www.w3schools.com/html/example\_withoutviewport.htm)               [![](<../../.gitbook/assets/image (37).png>)](https://www.w3schools.com/html/example\_withviewport.htm)

&#x20;                                   Viewport meta tegisiz                     Viewport meta tegi bilan

{% hint style="warning" %}
**Maslahat**: Agar siz ushbu sahifani telefon yoki planshet orqali koʻrayotgan boʻlsangiz, farqni koʻrish uchun quyidagi rasmlar ustiga bosing.
{% endhint %}

## Moslashuvchan rasmlar

Moslashuvchan ramslar har qanday brauzer o'lchamiga mos keladigan o'lchamdagi rasmlardir.

### Width xususiyatidan foydalanish

Agar CSSning `width` xususiyati 100%  deb berilgan bo'lsa, rasm moslashuvchan bo'ladi va o'lchamini yuqoriga va pastga cho'zadi:

<figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

```
<img src="img_girl.jpg" style="width:100%;"> 
```

E'tibor bering, yuqoridagi misolda rasmni o'zining asl o'lchamidan kattaroq qilib kattalashtirish mumkin. Ko'p hollarda buning o'rniga CSSning max-width xususiyatidan foydalanish yaxshiroq yechim bo'ladi.

### Max-width xususiyatidan foydalanish

Agar max-width xususiyatining qiymati 100% qilib berilsa rasm kerak paytda kichrayadi, lekin asl o'lchamidan kattalashib ketmaydi.

![](<../../.gitbook/assets/image (38).png>)

```
<img src="img_girl.jpg" style="max-width:100%;height:auto;"> 
```

## Browser kengligiga qarab turli rasmlarni ko'rsatish

HTMLning elementi turli browser oynasining o'lchamiga mos bir nechta rasmlarni joylashtirish imkonini beradi.

Quyidagi rasm oyna o'lchamiga qarab qanday o'zgarishini ko'rish uchun brauzer oynasining o'lchamini o'zgartiring:

![](<../../.gitbook/assets/image (4).png>)

```
<picture>
  <source srcset="img_smallflower.jpg" media="(max-width: 600px)">
  <source srcset="img_flowers.jpg" media="(max-width: 1500px)">
  <source srcset="flowers.jpg">
  <img src="img_smallflower.jpg" alt="Flowers">
</picture> 
```

## Moslashuvchan matn o'lchami

Matn o'lchami "vw" bilan berilishi mumkin, bu "viewport width" degan ma'noni anglatadi.

Shu yo'l bilan matn o'lchami brauzer oynasining o'lchamiga moslashadi:

<figure><img src="../../.gitbook/assets/image (518).png" alt=""><figcaption></figcaption></figure>

```
<h1 style="font-size:10vw">Hello World</h1> 
```

{% hint style="warning" %}
Viewport - bu brauzer oynasining o'lchamidir. 1vw = viewport kengligining 1%-i bo'ladi. Agar viewport 50 sm kenglikda bo'lsa, 1vw 0,5 sm-ga teng bo'ladi.
{% endhint %}

## Media querylar

Matn va rasmlar o'lchamini o'zgartirishdan tashqari, responsive veb-sahifalarda media querylardan foydalanish ham keng tarqalgan.

Media querylar bilan siz turli xil brauzer o'lchamlari uchun butunlay boshqa stillar berishingiz mumkin.

Misol: brauzer oynasining oʻlchamini oʻzgartiring va quyidagi uchta div elementi katta ekranlarda gorizontal va kichik ekranlarda vertikal holda joylashishini guvohi bo'ling:

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

```
<style>
.left, .right {
  float: left;
  width: 20%; /* The width is 20%, by default */
}

.main {
  float: left;
  width: 60%; /* The width is 60%, by default */
}

/* Use a media query to add a breakpoint at 800px: */
@media screen and (max-width: 800px) {
  .left, .main, .right {
    width: 100%; /* The width is 100%, when the viewport is 800px or smaller */
  }
}
</style>
```

## Moslashuvchan web sahifa - to'liq misol

Moslashuvchan veb-sahifa katta ekranli kompyuterlarda va kichik ekranli telefonlarda to'g'ri ko'rinishi kerak.

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

## Moslashuvchan web dizayn - Freymworklar

Barcha mashhur CSS Frameworklar o'zlarining moslashuvchan dizaynlarini taklif qiladi.

Ular ulardan foydalanish oson va bepul.

## W3.CSS

W3.CSS standart PC, planshet va mobil qurilmalar uchun moslashuvchan dizaynni qo'llab-quvvatlaydigan zamonaviy CSS freymworki hisoblanadi.

W3.CSS boshqa shu kabi CSS freymworklariga qaraganda kichikroq va tezroq.

W3.CSS jQuery yoki boshqa JavaScript kutubxonasidan mustaqil bo'lishi uchun yaratilgan.

<figure><img src="../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

```
<!DOCTYPE html>
<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<body>

<div class="w3-container w3-green">
  <h1>W3Schools Demo</h1>
  <p>Resize this responsive page!</p>
</div>

<div class="w3-row-padding">
  <div class="w3-third">
    <h2>London</h2>
    <p>London is the capital city of England.</p>
    <p>It is the most populous city in the United Kingdom,
    with a metropolitan area of over 13 million inhabitants.</p>
  </div>

  <div class="w3-third">
    <h2>Paris</h2>
    <p>Paris is the capital of France.</p>
    <p>The Paris area is one of the largest population centers in Europe,
    with more than 12 million inhabitants.</p>
  </div>

  <div class="w3-third">
    <h2>Tokyo</h2>
    <p>Tokyo is the capital of Japan.</p>
    <p>It is the center of the Greater Tokyo Area,
    and the most populous metropolitan area in the world.</p>
  </div>
</div>

</body>
</html> 
```

W3.CSS haqida ko'proq o'rganish uchun [W3.CSS qo'llanmamizni](https://www-w3schools-com.translate.goog/w3css/default.asp?\_x\_tr\_sl=en&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) o'qing.

## Bootsrap

Yana bir mashhur CSS freymworki bu Bootstrap hisoblanadi. Bootstrap moslashuvchan veb-sahifalarni yaratish uchun HTML, CSS va jQuery-dan foydalanadi.

```
<!DOCTYPE html>
<html lang="en">
<head>
<title>Bootstrap Example</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
</head>
<body>

<div class="container">
  <div class="jumbotron">
    <h1>My First Bootstrap Page</h1>
  </div>
  <div class="row">
    <div class="col-sm-4">
      ...
    </div>
    <div class="col-sm-4">
      ...
    </div>
    <div class="col-sm-4">
    ...
    </div>
  </div>
</div>

</body>
</html> 
```
