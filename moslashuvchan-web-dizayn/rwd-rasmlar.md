# RWD Rasmlar

<figure><img src="https://www.w3schools.com/css/img_chania.jpg" alt=""><figcaption><p>Rasmni sahifaga moslashishini ko'rish uchun brauzer oynasining o'lchamini o'zgartiring.</p></figcaption></figure>

### width xususiyatidan foydalanish

Agar `width` xususiyat foizda berilgan bo'lsa va `height` xususiyat "auto" qilingan bo'lsa, rasm moslashuvchan bo'ladi va o'zi kattalashadi va kichiklashadi:

```
img {
  width: 100%;
  height: auto;
}
```

Yuqoridagi misolda rasmni asl o'lchamidan kattaroq qilib kattalashtirish mumkinligiga e'tibor bering. Ko'p hollarda buning o'rniga `max-width` xususiyatidan foydalanish samarali yechim bo'ladi.

### max-width xususiyatidan foydalanish

Agar `max-width` xususiyati 100% qilingan bo'lsa, rasm kerak bo'lganda kichrayadi, lekin  hech qachon asl o'lchamidan kattalashmaydi:

```
img {
  max-width: 100%;
  height: auto;
}
```

### Veb-sahifasiga rasm qo'shing

```
img {
  width: 100%;
  height: auto;
}
```

### Background rasmlar

Background rasmlar o'zining o'lchamini o'zgartirishda va masshtablashtirishda moslashuvchan bo'ladi.

Sizga uch xil usulni ko'rsatamiz:

1\. Agar `background-size` xususiyat "contain" qilingan bo'lsa, bacgroundi rasm masshtablanadi va rasm maydoniga moslashishga harakat qiladi. Lekin, rasm o'zining tomonlar nisbatini saqlab qoladi (Rasmning kengligi va balandligi o'rtasidagi proportsional munosabat):

<figure><img src="../.gitbook/assets/image (436).png" alt=""><figcaption></figcaption></figure>

CSS kodi:

```
div {
  width: 100%;
  height: 400px;
  background-image: url('img_flowers.jpg');
  background-repeat: no-repeat;
  background-size: contain;
  border: 1px solid red;
}
```

2\. Agar `background-size` xususiyat "100% 100%" qilingan bo'lsa, background rasm kontent maydonini to'liq qamrab olish uchun cho'zilib ketadi:

<figure><img src="../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure>

CSS kodi:

```
div {
  width: 100%;
  height: 400px;
  background-image: url('img_flowers.jpg');
  background-size: 100% 100%;
  border: 1px solid red;
}
```

3\. Agar `background-size` xususiyat "cover" qilingan bo'lsa, background rasm kontent maydonining hammasini egallab oladigan darajada o'zgaradi. E'tibor bering, "cover" qiymati rasmning tomonlar nisbatini saqlab qoladi va bunda background rasmning ma'lum bir qismi kesib olinadi:

<figure><img src="../.gitbook/assets/image (388).png" alt=""><figcaption></figcaption></figure>

CSS kodi:

```
div {
  width: 100%;
  height: 400px;
  background-image: url('img_flowers.jpg');
  background-size: cover;
  border: 1px solid red;
}
```

### Turli xil qurilmalar uchun turli xil rasmlar

Katta rasm kattaroq kompyuter ekranlarida to'g'ri ko'rinishi mumkin, lekin kichik qurilmalarda bunday bo'lmaydi. Rasmni kichraytirishga to'g'ri kelsa, nima uchun katta rasmni yuklash kerak? Yuklash vaqtini kamaytirish yoki boshqa sabablarga ko'ra har xil rasmlarni turli qurilmalarga mos tarzda ko'rsatish uchun media queriedan foydalanishingiz mumkin.

Turli qurilmalarda ko'rsatiladigan bitta katta rasm va bitta kichikroq rasm:

![](https://www.w3schools.com/css/img\_flowers.jpg)

&#x20;                                                   ![](../.gitbook/assets/img\_smallflower.jpg)

```
/* For width smaller than 400px: */
body {
  background-image: url('img_smallflower.jpg');
}

/* For width 400px and larger: */
@media only screen and (min-width: 400px) {
  body {
    background-image: url('img_flowers.jpg');
  }
}
```

Brauzer kengligini emas qurilma kengligini tekshiradigan `min-width` o'rniga `min-device-width` media queriesidan foydalanishingiz mumkin. Shunda brauzer oynasining o'lchamini o'zgartirganingizda rasm o'zgarmaydi:

```
/* For devices smaller than 400px: */
body {
  background-image: url('img_smallflower.jpg');
}

/* For devices 400px and larger: */
@media only screen and (min-device-width: 400px) {
  body {
    background-image: url('img_flowers.jpg');
  }
}
```

### HTML \<picture> elementi

HTMLning `<picture>` elementi veb dasturchilarga rasmlarni berishda bir necha moslashuvchanlik imkoniyatini beradi.

Moslashuvchan dizaynlarda ishlatiladigan rasmlar uchun `<picture>` elementidan juda ko'p foydalanishadi. Viewport kengligidan kelib chiqqan holda kattalashtirilgan yoki kichraytirilgan birgina rasm o'rniga, brauzer viewportini yanada chiroyli qilish uchun bir nechta rasmlarni berish mumkin.

`<picture>` elementi `<video>` va `<audio>` elementlariga o'xshab ishlaydi. Turli xil sourcelarni berganingizda va qurilmaga mos keladigan birinchi source foydalaniladi:

```
<picture>
  <source srcset="img_smallflower.jpg" media="(max-width: 400px)">
  <source srcset="img_flowers.jpg">
  <img src="img_flowers.jpg" alt="Flowers">
</picture>
```

`srcset` atributi talab qilinadi va rasm source-ini belgilaydi.

`media` atributi dan foydalanish ixtiyoriy va CSS @media qoidasidagi media querielarni qabul qiladi.

`<picture>` elementini qo'llab-quvvatlamaydigan brauzerlar uchun `<img>` elementidan foydalanishingiz kerak.
