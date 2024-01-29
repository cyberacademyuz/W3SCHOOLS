# HTML SSE

Server tomonidan yuborilgan hodisalar (Server-Sent Events - SSE) veb-sahifaga yangilanishlarni serverdan olish imkonini beradi.

### Server tomonidan yuborilgan hodisalar - bir tomonlama xabarlar

SSE bu veb-sahifaning yangilanishlarni avtomatik tarzda serverdan olishidir.

Bu avval ham bor edi, lekin veb-sahifada yangilanishlar bor yoki yo'qligini so'rash kerak edi. SSE orqali esa yangilanishlar avtomatik tarzda keladi.

**Masalan**: Facebook/Twitter yangilanishlari, aksiyalardagi narx yangilanishlari, yangiliklar tasmasi, sport natijalari va boshqalar.

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar web-workerni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini bildiradi.

| API | Chrome | Edge | Firefox | Safari | Opera |
| --- | ------ | ---- | ------- | ------ | ----- |
| SSE | 6.0    | 79.0 | 6.0     | 5.0    | 11.5  |

### SSE bildirishnomalarini olish

EventSource obyekti server tomonidan yuborilgan hodisa bildirishnomalarini olish uchun ishlatiladi:

```
var source = new EventSource("demo_sse.php");
source.onmessage = function(event) {
  document.getElementById("result").innerHTML += event.data + "<br>";
};
```

Misol tushuntirildi:

* Yangi EventSource obyektini yarating va yangilanishlarni yuboradigan sahifaning URL manzilini belgilang (bu misolda "demo\_sse.php")
* Har safar yangilanish qabul qilinganda, onmessage hodisasi sodir bo'ladi
* Onmessage hodisasi sodir bo'lganda, olingan ma'lumotlarni id="result" bilan elementga qo'ying.

### SSEni qo'llab-quvvatlanishini tekshiring

Yuqoridagi misolda brauzer SSE ni qo'llab-quvvatlashini tekshirish uchun qo'shimcha kodlar mavjud:

```
if(typeof(EventSource) !== "undefined") {
  // Ha! SSE qo'llab-quvvatlanadi
  // Biror kod.....
} else {
  // Kechirasiz! SSE qo'llab-quvvatlanmaydi..
}
```

### Server-Side kodiga misol

Yuqoridagi kod ishlashi uchun sizga ma'lumotlar yangilanishlarini yubora oladigan server kerak (masalan, PHP yoki ASP).

Server tomondagi hodisalar stream sintaksisi oddiy. "**Content-Type**" headerini "text/event stream" qilib o'rnating. Endi hodisalar streamini yuborishni boshlashingiz mumkin.

PHP kodi (demo\_sse.php):

```php
<?php
header('Content-Type: text/event-stream');
header('Cache-Control: no-cache');

$time = date('r');
echo "data: The server time is: {$time}\n\n";
flush();
?>
```

ASP (VB) kodi (demo\_sse.asp):

```aspnet
<%
Response.ContentType = "text/event-stream"
Response.Expires = -1
Response.Write("data: The server time is: " & now())
Response.Flush()
%>
```

Kodni tushuntirish:

* "**Content-Type**" headerini "text/event stream" qilib o'rnating
* Sahifa keshlanmasligi kerakligini belgilang
* Yuboriladigan ma'lumotlarni chiqaring ( **Har doim** "data:" bilan boshlang)
* Ko'rsatiladigan ma'lumotlarni yana veb-sahifaga yuboring

### EventSource obyekti

Yuqoridagi misollarda biz xabarlarni olish uchun onmessage hodisasidan foydalanganmiz. Ammo boshqa hodisalar ham mavjud:

| Hodisalar | Ta'rif                                    |
| --------- | ----------------------------------------- |
| onopen    | When a connection to the server is opened |
| onmessage | When a message is received                |
| onerror   | When an error occurs                      |
