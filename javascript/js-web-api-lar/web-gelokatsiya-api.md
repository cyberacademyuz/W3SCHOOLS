# WEB Gelokatsiya API

### Foydalanuvchining joylashuvini toping

HTML Geolocation API foydalanuvchining geografik joylashuvini olish uchun ishlatiladi.

Bu maxfiylikni buzishi mumkinligi sababli, agar foydalanuvchi ma'qullamasa, joylashuv aniqlanmaydi.

{% hint style="warning" %}
### Eslatma

Geolokatsiya smartfonlar kabi GPSga ega qurilmalarda yaxshi ishlaydi.
{% endhint %}

### Brauzerning qo'llab-quvvatlashi

Geolocation API barcha brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari | Opera |
| ------ | ---- | ------- | ------ | ----- |
| Ha     | Ha   | Ha      | Ha     | Ha    |

{% hint style="warning" %}
### Eslatma

Geolocation API faqat HTTPS kabi xavfsiz kontekstlarda ishlaydi.

Agar saytingiz xavfsiz bo'lmagan manbaga joylashtirilgan bo'lsa, foydalanuvchilarning joylashuvini aniqlash so'rovlari ishlamaydi.
{% endhint %}

### Geolocation API dan foydalanish

`getCurrentPosition()` metodi foydalanuvchining joylashuvini qaytarish uchun ishlatiladi.

Quyidagi misol foydalanuvchi joylashuvining kordinatalarini qaytaradi:

```
<script>
const x = document.getElementById("demo");
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
</script>
```

Misolni tushuntirish:

* Geolocation qo'llab-quvvatlanishini tekshiring
* Agar qo'llab-quvvatlansa, `getCurrentPosition()` metodini ishga tushiring. Agar qo'llab quvvatlanmasa, foydalanuvchiga bu haqida habar ko'rsating,
* Agar `getCurrentPosition()` metodi muvaffaqiyatli ishlasa, u koordinata obyektini parametrda (showPosition) ko'rsatilgan funksiyaga qaytaradi.
* `showPosition()` funksiyasi kordinatani ko'rsatadi

Yuqoridagi misol juda oddiy Geolocation skripti bo'lib, unda hech qanday xato yo'q.

### Xatoliklarni va bekor qilinishni boshqarish

`getCurrentPosition()` metodining ikkinchi parametri xatoliklarni qayta ishlash uchun ishlatiladi. U foydalanuvchining joylashuvini ololmasa, ishga tushirish funksiyasini belgilaydi:

```
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

### Natijani xaritada ko'rsatish

Natijani xaritada ko'rsatish uchun Google Xaritasi kabi xarita servislaridajnfoydalanishingiz kerak.

Quyidagi misolda qaytarilgan kordinatalar Google Xaritadagi joylashuvni ko'rsatish uchun ishlatiladi (statik rasm yordamida):

```
function showPosition(position) {
  let latlon = position.coords.latitude + "," + position.coords.longitude;

  let img_url = "https://maps.googleapis.com/maps/api/staticmap?center=
  "+latlon+"&zoom=14&size=400x300&sensor=false&key=YOUR_KEY";

  document.getElementById("mapholder").innerHTML = "<img src='"+img_url+"'>";
}
```

### Joylashuvga oid ma'lumotlar

Ushbu sahifada foydalanuvchining xaritadagi joylashuvini qanday ko'rsatish mumkinligi ko'rsatilgan.

Geolokatsiya, joylashuvga oid ma'lumotlar uchun foydali, masalan:

* Yangilangan lokal ma'lumotlar
* Foydalanuvchi yaqinidagi qiziqarli joylarni ko'rsatish
* Navbatma-navbat navigatsiya (GPS)

### getCurrentPosition() metodi - ma'lumotlarni qaytarish

`getCurrentPosition()` metodi obyektni muvaffaqiyatli tarda qaytaradi. Latitude, longitude va accuracy xususiyatlari har doim qaytariladi. Agar boshqa xususiyatlar mavjud bo'lsa ular qaytariladi:

| Xususiyat               | Qaytariladi                                                                      |
| ----------------------- | -------------------------------------------------------------------------------- |
| coords.latitude         | Kenglikni o'nlik son sifatida qaytarish (har doim qaytariladi)                   |
| coords.longitude        | Uzunlikni o'nlik son sifatida qaytarish (har doim qaytariladi)                   |
| coords.accuracy         | Joylashuv aniqligi qaytarish (har doim qaytariladi)                              |
| coords.altitude         | Dengiz sathidan oʻrtacha metr balandligini qaytarish (mavjud boʻlsa qaytariladi) |
| coords.altitudeAccuracy | Joylashuvning balandlik aniqligini qaytarish (mavjud bo'lsa qaytariladi)         |
| coords.heading          | Sarlavha shimoldan soat yo'nalishi bo'yicha daraja (mavjud bo'lsa qaytariladi)   |
| coords.speed            | Tezlik sekundiga necha metr ekanligini qaytarish(mavjud bo'lsa qaytariladi)      |
| timestamp               | Javob sanasi/vaqti (mavjud bo'lsa qaytariladi)                                   |

### Geolokatsiya obyekti - Boshqa qiziqarli metodlar

Geolocation obyektida boshqa qiziqarli usullar ham mavjud:

* `watchPosition()`- Foydalanuvchining joriy holatini qaytaradi va foydalanuvchi harakatlanayotganda yangilangan pozitsiyasini qaytarishda davom etadi (masalan, avtomobildagi GPS).
* `clearWatch()`- `watchPosition()` metodini to'xtatadi.

Quyidagi misol `watchPosition()` metodini ko'rsatadi. Buni tekshirish uchun sizga GPS qurilmasi kerak (masalan, smartfon):

```
<script>
const x = document.getElementById("demo");
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
