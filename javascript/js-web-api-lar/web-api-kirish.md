# WEB API Kirish

{% hint style="success" %}
Web API - bu dasturchining orzusi.

* U brauzerning funksionalligini kengaytirishi mumkin
* U murakkab funksiyalarni sezilarli darajada soddalashtirishi mumkin
* U murakkab kodni sodda sintaksis orqali yozishni ta'minlaydi
{% endhint %}

### Web API nima ?

API qisqartma so'z hisoblanib **A**pplication **P**rogramming **I**nterface degan ma'noni anglatadi.

Web API - bu Internet uchun dasturlash interfeysi.

Brauzer API veb-brauzer funksiyalarini kengaytirishi mumkin.

Server API esa veb-serverning funksiyalarini kengaytirishi mumkin.

### Brauzer API'lari

Barcha brauzerlarda murakkab operatsiyalarni qo'llab-quvvatlash va ma'lumotlarga murojaat qilishga yordam berish uchun o'rnatilgan veb-APIlar to'plami mavjud.

Masalan, **Geolocation API** brauzer joylashgan joyning koordinatalarini qaytarishi mumkin.

{% code title="Foydalanuvchi joylashuvining kenglik va uzunligini oling:" %}
```
const myElement = document.getElementById("demo");

function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else {
    myElement.innerHTML = "Geolocation is not supported by this browser.";
  }
}

function showPosition(position) {
  myElement.innerHTML = "Latitude: " + position.coords.latitude +
  "<br>Longitude: " + position.coords.longitude;
}
```
{% endcode %}

### Uchinchi tomon API'lari

Uchinchi tomon API'lari brauzeringizda o'rnatilmagan.

Ushbu API-lardan foydalanish uchun siz kodni Internetdan yuklab olishingiz kerak bo'ladi.

Misollar:

* YouTube API - veb-saytda videolar ko'rsatish imkonini beradi.
* Twitter API - Tvitlarni veb-saytda ko'rsatish imkonini beradi.
* Facebook API - veb-saytda Facebook ma'lumotlarini ko'rsatish imkonini beradi.
