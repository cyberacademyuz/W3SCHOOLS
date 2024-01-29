# AJAX XMLHttp

{% hint style="success" %}
AJAX ning poydevori `XMLHttpRequest` obyektidir.

1. XMLHttpRequest obyektini yarating
2. Callback funksiyasini tuzing
3. XMLHttpRequest obyektini oching
4. Serverga so'rov yuboring
{% endhint %}

### XMLHttpRequest obyekti

Barcha zamonaviy brauzerlar `XMLHttpRequest` obyektni qo'llab-quvvatlaydi.

`XMLHttpRequest` obyekti orqafondagi veb-server bilan ma'lumotlarni almashish uchun ishlatilishi mumkin. Bu butun sahifani qayta yuklamasdan, veb-sahifaning sahifalarini yangilash mumkinlligini anglatadi.

### XMLHttpRequest obyektini yarating

Barcha zamonaviy brauzerlar (Chrome, Firefox, IE, Edge, Safari, Opera) built-in `XMLHttpRequest` obyektiga ega.

`XMLHttpRequest` obyektini yaratish sintaksisi:

```
variable = new XMLHttpRequest();
```

### Callback funktsiyasini tuzish

Callback funktsiyasi boshqa funksiyaga parametr sifatida uzatiladigan funksiya hisoblanadi.

Bu holatda, callback funksiyasi response tayyor bo'lganida bajarilishi kerak bo'lgan kodni o'z ichiga olishi kerak.

```
xhttp.onload = function() {
  // What to do when the response is ready
}
```

### So'rov yuborish

Serverga so'rov yuborish uchun `XMLHttpRequest` obyektining `open()` va `send()` metodlaridan foydalanishingiz mumkin:

```
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
```

```
// Create an XMLHttpRequest object
const xhttp = new XMLHttpRequest();

// Define a callback function
xhttp.onload = function() {
  // Here you can use the Data
}

// Send a request
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
```

### Domenlar bo'ylab murojaat qilish

Xavfsizlik nuqtai nazaridan zamonaviy brauzerlar domenlar bo'ylab murojaat qilishga ruxsat bermaydi.

Bu veb-sahifa ham, u yuklamoqchi bo'lgan XML fayl ham bitta serverda joylashgan bo'lishi kerakligni anglatadi.

W3Schools-dagi misollardagi barcha ochiq  XML fayllar W3Schools domenida joylashgan.

Agar yuqoridagi misolni o'zingizning veb-sahifalaringizdan birida ishlatmoqchi bo'lsangiz, yuklagan XML fayllaringiz o'z serveringizda joylashgan bo'lishi kerak.

### XMLHttpRequest ob'ekt usullari

| Metod                                 | Ta'rif                                                                                                                                                                                                                     |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| new XMLHttpRequest()                  | Yangi XMLHttpRequest obyektini yaratadi                                                                                                                                                                                    |
| abort()                               | Joriy so'rovni bekor qiladi                                                                                                                                                                                                |
| getAllResponseHeaders()               | Header ma'lumotlarini qaytaradi                                                                                                                                                                                            |
| getResponseHeader()                   | O'ziga xos header ma'lumotlarini qaytaradi                                                                                                                                                                                 |
| open(_method, url, async, user, psw_) | <p>So'rovni belgilaydi</p><p></p><p>method: so'rov turi GET yoki POST</p><p>url: fayl joylashuvi</p><p>async: true (asinxron) yoki false (sinxron)</p><p>user: ixtiyoriy foydalanuvchi nomi</p><p>psw: ixtiyoriy parol</p> |
| send()                                | <p>So'rovni serverga yuboradi.</p><p>GET so'rovlari uchun ishlatiladi</p>                                                                                                                                                  |
| send(_string_)                        | <p>So'rovni serverga yuboradi.</p><p>POST so'rovlari uchun ishlatiladi</p>                                                                                                                                                 |
| setRequestHeader()                    | Yuboriladigan headerga label/qiymat juftligini qo'shadi                                                                                                                                                                    |

### XMLHttpRequest obyektining xususiyatlari

| Xususiyat          | Ta'rif                                                                                                                                                                                                                                 |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| onload             | So'rov qabul qilinganda (yuklanganda) chaqiriladigan funksiyani belgilaydi.                                                                                                                                                            |
| onreadystatechange | ReadyState xususiyati o‘zgarganda chaqiriladigan funksiyani belgilaydi                                                                                                                                                                 |
| readyState         | <p>XMLHttpRequest holatini ushlab turadi. </p><p>0: request ishga tushirilmagan </p><p>1: server ulanishi o'rnatildi </p><p>2: request qabul qilindi </p><p>3: requestni qayta ishlash </p><p>4: request tugadi va response tayyor</p> |
| responseText       | Response ma'lumotlarini string sifatida qaytaradi                                                                                                                                                                                      |
| responseXML        | Returns the response data as XML data                                                                                                                                                                                                  |
| status             | <p>Requestning status-kodini qaytaradi:</p><p>200: "OK" </p><p>403: "Taqiqlangan" </p><p>404 "Sahifa topilmadi"<br>To'liq ro'yxatni ko'rish uchun Http xabarlari havolasiga o'ting</p>                                                 |
|                    |                                                                                                                                                                                                                                        |
| statusText         | Status matnini qaytaradi (masalan, "OK" yoki "Sahifa topilmadi")                                                                                                                                                                       |

### Onload xususiyati

`XMLHttpRequest` obyekti yordamida request response olganida bajarilishi kerak bo'lgan callback funksiyasini belgilashingiz mumkin.

Funktsiya `XMLHttpRequest` obyektining `onload`xususiyatida tuziladi:

```
xhttp.onload = function() {
  document.getElementById("demo").innerHTML = this.responseText;
}
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
```

### Bir nechta callback funksiyalar

Agar veb-saytda bir nechta AJAX vazifalari bo'lsa, `XMLHttpRequest` obyektini bajarish uchun bitta funksiya va har bir AJAX vazifasi uchun bitta callback funksiya yaratishingiz kerak.

Funksiya chaqiruvi, URL va reponse tayyor bo'lganda qaysi funksiyani chaqirish kerakligini o'z ichiga olishi kerak.

```
loadDoc("url-1", myFunction1);

loadDoc("url-2", myFunction2);

function loadDoc(url, cFunction) {
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {cFunction(this);}
  xhttp.open("GET", url);
  xhttp.send();
}

function myFunction1(xhttp) {
  // action goes here
}
function myFunction2(xhttp) {
  // action goes here
}
```

### onreadstatechange xususiyati

`readyState` xususiyati `XMLHttpRequest` holatini saqlaydi.

`onreadystatechange` xususiyati readyState o'zgarganda bajarilishi kerak bo'lgan callback funktsiyani belgilaydi.

`status` va `statusText` xususiyatlari `XMLHttpRequest` obyektining statusini saqlaydi.

| Xususiyat          | Ta'rif                                                                                                                                                                                                                               |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| onreadystatechange | ReadyState xususiyati o‘zgarganda chaqiriladigan funksiyani belgilaydi                                                                                                                                                               |
| readyState         | <p>XMLHttpRequest statusini ushlab turadi. </p><p>0: request ishga tushirilmagan </p><p>1: server ulanishi o'rnatildi</p><p>2: request qabul qilindi</p><p>3: requestni qayta ishlash</p><p>4: request tugadi va response tayyor</p> |
| status             | <p>200: "OK"<br>403: "Taqiqlangan"<br>404: "Sahifa topilmadi"<br>To'liq ro'yxatni ko'rish uchun Http xabarlari havolasiga o'ting</p>                                                                                                 |
| statusText         | Status matnini qaytaradi (masalan, "OK" yoki "Sahifa topilmadi")                                                                                                                                                                     |

Har safar readyState o'zgarganida `onreadystatechange` funksiyasi chaqiriladi.

`readyState` 4 va status 200 bo'lsa, response tayyor bo'ladi:

```
function loadDoc() {
  const xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("demo").innerHTML =
      this.responseText;
    }
  };
  xhttp.open("GET", "ajax_info.txt");
  xhttp.send();
}
```

{% hint style="warning" %}
`Onreadstatechange` hodisasi to'rt marta (1-4) ishga tushiriladi, readyState'dagi har bir o'zgarish uchun bir marta.
{% endhint %}
