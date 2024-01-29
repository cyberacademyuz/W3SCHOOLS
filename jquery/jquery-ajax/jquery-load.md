# jQuery Load

## jQuery - load() AJAX metodi <a href="#jquery-load-ajax-metodi" id="jquery-load-ajax-metodi"></a>

### jQuery load() metodi <a href="#jquery-load-metodi" id="jquery-load-metodi"></a>

jQuery ning `load()` metodi oddiy ammo kuchli AJAX metodi hisoblanadi.

`load()` metodi serverdan ma'lumotni yuklaydi va yuklangan ma'lumotni tanlangan elementga qo'yadi.

**Sintaksis:**

```
$(selector).load(URL,data,callback); 
```

**URL** parametri yuklanishi kerak bo'lgan URL ni qabul qiluvchi majburiy qiymatni o'z ichiga oladi.

Ixtiyoriy hisoblangan **data** parametri soʻrov bilan birga yuborish uchun **querystring**/**value** juftligini o'z ichiga oladi.

Ixtiyoriy hisoblangan **callback** parametri `load()` metodi tugallangandan keyin ishga tushadigan funksiyani o'z ichiga oladi.

**Quyida bizning "demo\_test.txt" faylimizning tarkibi:**

```
<h2>jQuery and AJAX is FUN!!!</h2>
<p id="p1">This is some text in a paragraph.</p>
```

Quyidagi misol "demo\_test.txt" faylining kontentini maxsus `<div>` elementiga yuklaydi:

```
$("#div1").load("demo_test.txt"); 
```

URL parametriga jQuery selektorini qo'shib jo'natish ham mumkin.

Quyidagi misol "**demo\_test.txt**" faylidagi **id="p1"** attributiga elementning mazmunini ma'lum bir `<div>` elementiga yuklaydi:

```
$('#div1').load("demo_text.txt #p1");
```

Ixtiyoriy hisoblangan callback parametri `load()` metodi tugallangandan so'ng ishga tushadigan funksiyani o'z ichiga oladi. callback funksiyasida har xil parametrlar bor:

* `responseTxt` - Agarda chaqiruv muvaffaqiyatli amalga oshirilsa, natijaning kontentini o'z ichida saqlaydi.
* `statusTxt` - chaqiruvning statusini o'zida saqlaydi
* `xhr` - XMLHttpRequest obyektini o'zida saqlaydi.

Quyidagi misol `load()` metodi tugagandan keyin alert oynasini ko'rsatadi. Agar `load()` metodi muvaffaqiyatli bajarilsa, u "External content loaded successfully!" deb ko'rsatadi va agar muvaffaqiyatsiz yakunlansa, xato xabarini ko'rsatadi:

```
$("button").click(function(){
  $("#div1").load("demo_test.txt", function(responseTxt, statusTxt, xhr){
    if(statusTxt == "success")
      alert("External content loaded successfully!");
    if(statusTxt == "error")
      alert("Error: " + xhr.status + ": " + xhr.statusText);
  });
}); 
```
