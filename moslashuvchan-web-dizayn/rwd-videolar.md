# RWD Videolar

### width xususiyatidan foydalanish

Agar `width` xususiyat 100% qilingan boʻlsa, video player moslashuvchan va o'zi kattalashadi va kichiklashadi:

```
video {
  width: 100%;
  height: auto;
}
```

Yuqoridagi misolda video playerni asl o'lchamidan kattaroq qilib kattalashtirish mumkin. Ko'p hollarda buning o'rniga `max-width` xususiyatidan foydalanish samaraliroq yechim bo'ladi.

### max-width xususiyatidan foydalanish

Agar `max-width` xususiyati 100% qilingan boʻlsa, video pleyer kerak bo'lgan payt kichiklashadi, lekin hech qachon asl oʻlchamidan kattalashmaydi:

```
video {
  max-width: 100%;
  height: auto;
}
```

### Veb-sahifaga video qo'shing

Veb-sahifamizga video qo'shmoqchimiz. Video har doim barcha bo'sh joyni egallab olishi uchun uning o'lchami o'zgartiriladi:

```
video {
  width: 100%;
  height: auto;
}
```
