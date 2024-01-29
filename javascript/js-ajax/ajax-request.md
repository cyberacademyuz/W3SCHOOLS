# AJAX Request

XMLHttpRequest obyekti serverdan ma'lumotlarni so'rash uchun ishlatiladi.

### Serverga so'rov yuboring

Serverga so'rov yuborish uchun `XMLHttpRequest` obyektining `open()` va `send()` metodlaridan foydalanamiz:

```
xhttp.open("GET", "ajax_info.txt", true);
xhttp.send();
```

| Metod                      | Ta'rif                                                                                                                                                                      |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| open(_method, url, async_) | <p>Request turini belgilaydi<br><br><em>method</em>: the request turi: GET yoki POST<br>url: server (fayl) joylashuvi</p><p>async: true (asinxron) yoki false (sinxron)</p> |
| send()                     | Serverga request yuboradi (GET uchun ishlatiladi)                                                                                                                           |
| send(_string_)             | Serverga request yuboradi (POST uchun ishlatiladi)                                                                                                                          |

### url - Serverdagi fayl

`open()` metodining `url` parametri serverdagi faylning manzilidir:

```
xhttp.open("GET", "ajax_test.asp", true);
```

Fayl .txt va .xml kabi har qanday fayl yoki .asp va .php kabi server skript fayllari (response yuborishdan oldin serverda amallarni bajarishi mumkin) bo'lishi mumkin.

### Async - true yoki false ?

Server so'rovlari asinxron tarzda yuborilishi kerak.

open() metodining `async` parametri true ga o'rnatilishi kerak:

```
xhttp.open("GET", "ajax_test.asp", true);
```

Asinxron yuborish orqali JavaScript server javobini kutishi shart emas, aksincha:

* server javobini kutayotganda boshqa skriptlarni bajarish mumkin
* response tayyor bo'lganidan keyin response bilan shug'ullanadi

{% hint style="danger" %}
`async = true` - async parametri uchun standart qiymat hisoblanadi.

Uchinchi parametrni kodingizdan xavfsiz tarzda olib tashlashingiz mumkin.

Sinxron XMLHttpRequest (ya'ni async = false) tavsiya qilinmaydi, chunki server response-i tayyor bo'lmaguncha JavaScript ishni to'xtatadi. Agar server band yoki sekin ishlasa, dastur osilib qoladi yoki to'xtaydi.
{% endhint %}

### GET yoki POST?

`GET` `POST`ga nisbatan sodda, tez va koʻp hollatlarda foydalanish mumkin.

Biroq, quyidagi holatlarda har doim POST metodidan foydalaning:

* Keshlangan fayl ixtiyoriy bo'lmaganda (serverdagi fayl yoki ma'lumotlar bazasini yangilash).
* Serverga katta hajmdagi ma'lumotlarni yuborganda (POST metodida o'lcham cheklovlari yo'q).
* Foydalanuvchi ma'lumotlarini yuborganda (u noma'lum belgilarni o'z ichiga olishi mumkin), POST GETga qaraganda mustahkam va xavfsizroq.

### GET so'rovlari

Oddiy `GET` so'rovi:

```
xhttp.open("GET", "demo_get.asp");
xhttp.send();
```

Yuqoridagi misolda siz keshlangan natija olishingiz mumkin. Bunga yo'l qo'ymaslik uchun URL manziliga unikal ID qo'shing:

```
xhttp.open("GET", "demo_get.asp?t=" + Math.random());
xhttp.send();
```

Agar `GET` metodi orqali ma'lumot yubormoqchi bo'lsangiz, ma'lumotni URL manziliga qo'shing:

```
xhttp.open("GET", "demo_get2.asp?fname=Henry&lname=Ford");
xhttp.send();
```

Server inputdan qanday foydalanishi va requestga qanday javob berishi keyingi bo'limda o'rgatiladi.

### POST so'rovlari

Oddiy `POST` so'rovi:

```
xhttp.open("POST", "demo_post.asp");
xhttp.send();
```

HTML formasi kabi ma'lumotlarni POST qilish uchun `setRequestHeader()` bilan HTTP headerini qo'shing. `Send()` metodida joʻnatiladigan maʼlumotlarni belgilang:

```
xhttp.open("POST", "ajax_test.asp");
xhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
xhttp.send("fname=Henry&lname=Ford");
```

| Metod                             | Description                                                                                                                               |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| setRequestHeader(_header, value_) | <p>Requestga HTTP headerlarni qo'shish<br><br><em>header</em>:  header nomini o'rnatish<br><em>value</em>: header qiymatini o'rnatish</p> |

### Sinxron so'rov

Sinxron so'rovni amalga oshirish uchun `open()` metodidagi uchinchi parametrni `false`ga o'zgartiring:

```
xhttp.open("GET", "ajax_info.txt", false);
```

Ba'zan test uchun async=false tez tez ishlatiladi. Bundan tashqari, eski JavaScript kodlarda ham sinxron so'rovlarni topishingiz mumkin.

Kod server o'z ishini tugatishini kutganligi sababli, `onreadystatechange` funksiyasiga ehtiyoj qolmaydi:

```
xhttp.open("GET", "ajax_info.txt", false);
xhttp.send();
document.getElementById("demo").innerHTML = xhttp.responseText;
```

{% hint style="danger" %}
Sinxron XMLHttpRequest (ya'ni async = false) tavsiya qilinmaydi, chunki server response-i tayyor bo'lmaguncha JavaScript ishni to'xtatadi. Agar server band yoki sekin ishlasa, dastur osilib qoladi yoki to'xtaydi.

Zamonaviy dasturchi vositalari sinxron so'rovlardan foydalanish haqida ogohlantiradigan qilindi va sinxron so'rovlardan foydalanilganda `InvalidAccessError`ni keltirib chiqarishi mumkin.
{% endhint %}
