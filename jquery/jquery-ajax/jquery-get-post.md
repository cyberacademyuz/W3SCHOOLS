---
description: jQuery - AJAX get() va post() metodlari
---

# jQuery Get/Post

jQueryning `get()` va `post()` metodlari serverdan HTTP GET yoki POST so'rovlari orqali ma'lumotni so'rash uchun ishlatiladi.

### HTTP Request: GET vs POST <a href="#http-request-get-vs-post" id="http-request-get-vs-post"></a>

Client va serverni bog'lab turuvchi request va response uchun eng ko'p ishlatiladigan metodlar ikkita, bular: GET va POST.

* **GET** - belgilangan resursdan ma'lumotni so'raydi.
* **POST** - belgilangan resursga ma'lumotni yuboradi.

GET asosan biror-bir ma'lumotni serverdan qabul qilish uchun ishatiladi. **Note:** GET metodi ba'zida keshlangan ma'lumotni ham qaytarishi mumkin.

POSTni ham ma'lumot olib kelish uchun ishlatsa bo'ladi, biroq, POST metodi hech qachon ma'lumotlarni keshlamaydi va ko'pincha berilgan qiymat bilan birga so'rov qilib yuboriladi.

GET va POST haqida ko'proq ma'lumot olmoqchi bo'lsangiz bizning HTTP metodlari GET va POST bo'limiimizni o'qing.

### jQuery $.get() metodi <a href="#jquery-get-metodi" id="jquery-get-metodi"></a>

$.get() metodi ma'lumotni HTTP GET request asosida olib keladi.

**Sintaksis:**

```
$.get(URL,callback); 
```

**URL** parametri so'rov yuborishingiz kerak bo'lgan URLni qabul qiluvchi majburiy qiymatni o'z ichiga oladi.

Ixtiyoriy hisoblangan **callback** parametri so'rov muvaffaqiyatli yakunlansagina ishga tushadigan funksiya hisoblanadi.

Quyidagi misolda serverdagi fayldan maʼlumotlarni olish uchun `$.get()` metodi qoʻllaniladi:

```
$("button").click(function(){
  $.get("demo_test.asp", function(data, status){
    alert("Data: " + data + "\nStatus: " + status);
  });
}); 
```

`$.get()` metodining birinchi parametr bu ma'lumotni qayerdan olib kelishimizni belgilaydigan URL ("demo\_test.asp").

Ikkinchi parametr esa **callback** funksiya hisoblanadi. Callback funksiyaining birinchi parametri so'ralgan sahifaning ma'lumotini, ikkinchi parametr esa so'rovning statusini saqlaydi.

**Maslahat:** Quyida ASP fayli qanday ko'rinishga ega ekanligi keltirilgan:

```
<%
response.write("This is some text from an external ASP file.")
%>
```

### jQuery $.post() metodi <a href="#jquery-post-metodi" id="jquery-post-metodi"></a>

`$.post()` metodi serverdan ma'lumotlarni HTTP POST metodi orqali so'raydi.

**Sintaksisi:**

```
$.post(URL,data,callback); 
```

**URL** parametri siz request yuboradigan URL manzilini belgilaydi.

Ixtiyoriy hisoblangan **data** parametri so'rov bilan birga yuboriladigan ba'zi ma'lumotlarni belgilaydi.

Ixtiyoriy hisoblangan **callback** parametri, agar so'rov muvaffaqiyatli bo'lsa, bajariladigan funksiyaning nomini o'z ichiga oladi.

Quyidagi misolda soʻrov bilan birga baʼzi maʼlumotlarni yuborish uchun `$.post()` metodi qoʻllaniladi:

```
$("button").click(function(){
  $.post("demo_test_post.asp",
  {
    name: "Donald Duck",
    city: "Duckburg"
  },
  function(data, status){
    alert("Data: " + data + "\nStatus: " + status);
  });
}); 
```

`$.post()` metodining birinchi parametri, ma'lumotni qayerga yuborishimizni belgilaydigan URL ("demo\_test\_post.asp").

Keyin esa biz so'rov bilan birga yuboriladigan ma'lumotni kiritamiz (nom va shahar).

"demo\_test\_post.asp" ASP skripti parametrlarni o'qiydi, tahlil qiladi va natijani qaytaradi.

Uchinchi parametr esa **callback** funksiyasi. Callback funksiyaning birinchi parametri do'rov yuborilgan sahifaning ma'lumotini, ikkinchi parametr esa so'rovning statusini qaytaradi.

**Maslahat:** Quyida ASP fayli qanday ko'rinishga ega ekanligi keltirilgan:

```
<%
dim fname,city
fname=Request.Form("name")
city=Request.Form("city")
Response.Write("Dear " & fname & ". ")
Response.Write("Hope you live well in " & city & ".")
%>
```
