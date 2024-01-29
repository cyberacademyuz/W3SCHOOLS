# Geolocation

HTMLning Geolokatsiya API-sidan foydalanuvchi joylashuvini aniqlash uchun foydalaniladi.

## Foydalanuvchi joylashuvini aniqlash

HTMLning API-si foydalanuvchining geografik joylashuvini aniqlash uchun ishlatiadi.

Bu maxfiylik qoidalarini buzishi mumkinligi sababli, agar foydalanuvchi rozi bo'lmasa, joylashuvni aniqlab bo'lmaydi.

{% hint style="warning" %}
**Eslatma:** Geolokatsiya smartfon kabi GPSga ega qurilmalarda juda aniqlik bilan aniqlanadi.
{% endhint %}

## Brauzerning qo'llab quvvatlashi

Jadvaldagi raqamlar geolokatsiyani to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| API          | Chrome                         | Edge | Firefox | Safari | Opera |
| ------------ | ------------------------------ | ---- | ------- | ------ | ----- |
| Geolokatsiya | 5.0 - 49.0 (http) 50.0 (https) | 9.0  | 3.5     | 5.0    | 16.0  |

{% hint style="warning" %}
**Eslatma:** Chrome 50 dan boshlab Geolocation API faqat HTTPS kabi xavfsiz kontekstlarda ishlaydi. Agar sizning saytingiz xavfsiz bo'lmagan manbada (masalan, HTTP) joylashtirilgan bo'lsa, foydalanuvchilarning joylashuvini aniqlash so'rovlari ishlamaydi.
{% endhint %}

### HTML Geolocation-dan foydalanish

`getCurrentPosition()` metodi foydalanuvchining joylashuvini qaytarish uchun ishlatiladi.

Quyidagi misol foydalanuvchi joylashuvining kenglik va uzunligini qaytaradi:

```javascript
<script>
var x = document.getElementById("demo");
function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else {
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}

function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude +
  "<br>Longitude: " + position.coords.longitude;
}
</script>O'zingiz sinab ko'ring »a
```

Misoni tushuntirish:

* Geolocation qo'llab-quvvatlanishini tekshiring
* Agar qo'llab-quvvatlansa, `getCurrentPosition()` metodoni ishga tushiring. Agar qo'llab quvvatlanmasa, foydalanuvchiga bu haqidagi xabarni ko'rsating.
* Agar `getCurrentPosition()` metodi muvaffaqiyatli bajarilsa, u koordinatalar obyektini parametrda (showPosition) ko'rsatilgan funktsiyaga qaytaradi.
* `showPosition()` funksiyasi kenglik va uzunlikni ko'rsatadi.

Yuqoridagi misol juda sodda Geolocation uchun kod bo'lib, unda hech qanday xatolik yo'q.

### Xatolarni va rad qilishlarni boshqarish

`getCurrentPosition()` metodining ikkinchi parametri xatolarni boshqarish uchun ishlatiladi. U foydalanuvchining joylashuvini ololmasa, ishga tushirish funksiyasini ifodalaydi:

```javascript
function showError(error) {
  switch(error.code) {
    case error.PERMISSION_DENIED:
      x.innerHTML = "User denied the request for Geolocation."
      break;
    case error.POSITION_UNAVAILABLE:
      x.innerHTML = "Location information is unavailable."
      break;
    case error.TIMEOUT:
      x.innerHTML = "The request to get user location timed out."
      break;
    case error.UNKNOWN_ERROR:
      x.innerHTML = "An unknown error occurred."
      break;
  }
}
```

### Joylashuvga oid ma'lumotlar

Ushbu sahifada foydalanuvchining xaritadagi joylashuvini qanday qilib ko'rsatish o'rgatilgan.

Bundan tashqari Geolocation, joylashuvga oid ma'lumotlar uchun ham juda foydali, masalan:

* Yangilangan mahalliy ma'lumotlar
* Foydalanuvchi yaqinidagi qiziqarli joylarni ko'rsatish
* Qadamma qadam navigatsiya (GPS)

### getCurrentPosition() metodi - ma'lumotlarni qaytarish

`getCurrentPosition()` metodi obyektni muvaffaqiyatli tarzda qaytaradi. Kenglik, uzunlik va aniqlik xususiyatlari har doim qaytariladi. Agar imkoni bo'lsa, boshqa xususiyatlar ham qaytariladi:

| Xususiyat               | Qaytariladigan natija                                                                    |
| ----------------------- | ---------------------------------------------------------------------------------------- |
| coords.latitude         | O'nlik son tizimida kenglik qiymati (har doim qaytariladi)                               |
| coords.longitude        | O'nlik son tizimida uzunlik qiymati (har doim qaytariladi)                               |
| coords.accuracy         | Joylashuvning aniqligi (har doim qaytariladi)                                            |
| coords.altitude         | Dengiz sathidan oʻrtacha metr balandlikda (mavjud boʻlsa qaytariladi)                    |
| coords.altitudeAccuracy | Joylashuvning balandlik aniqligi (mavjud bo'lsa qaytariladi)                             |
| coords.heading          | Yonalish, shimoldan soat yo'nalishi bo'yicha daraja sifatida (mavjud bo'lsa qaytariladi) |
| coords.speed            | Tezlik sekundiga metrda (mavjud bo'lsa qaytariladi)                                      |
| timestamp               | Qaytarilgan natija sanasi/vaqti (mavjud bo'lsa qaytariladi)                              |

### Geolocation obyekti - Boshqa qiziqarli metodlar

Geolocation obyektida boshqa qiziqarli metodlar ham mavjud:

* `watchPosition()`- Foydalanuvchining joriy holatini qaytaradi va foydalanuvchi harakatlanayotganda yangilangan pozitsiyasini qaytarishda davom etadi (masalan, avtomobildagi GPS).
* `clearWatch()`- `watchPosition()`metodini to'xtatadi.

Quyidagi misol `watchPosition()`metodini ko'rsatadi. Buni tekshirish uchun sizga GPS qurilmasi kerak (masalan, smartfon):

```javascript
<script>
var x = document.getElementById("demo");
function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.watchPosition(showPosition);
  } else {
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}
function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude +
  "<br>Longitude: " + position.coords.longitude;
}
</script>
```
