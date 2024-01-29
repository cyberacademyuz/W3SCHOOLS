# Hodisalar

jQuery ataylab siz uchun HTML dagi event larga javob beradigan qilib yasalgan.

### Event lar  nima? <a href="#event-lar-ozi-nima" id="event-lar-ozi-nima"></a>

Barcha foydalanuvchilarning web sahifada amalga oshiradigan ishlari bitta so'z bilan hodisa (event) deyiladi.

Hodisa biror narsa sodir bo'lgan aniq vaqtni ifodalaydi.

Masalan:

* Sichqoncha kursori element ustida harkatlanishi
* Radio tugmalarini tanlanishi
* Elementga bosish&#x20;

Quyida ba'zi DOM eventlarini keltirdik:

| Sichqoncha eventlar | Klaviatura eventlari | Forma eventlari | Document/Window eventlari |
| ------------------- | -------------------- | --------------- | ------------------------- |
| click               | keypress             | submit          | load                      |
| dblclick            | keydown              | change          | resize                    |
| mouseenter          | keyup                | focus           | scroll                    |
| mouseleave          |                      | blur            | unload                    |

#### Hodisa metodlari uchun jQuery sintaksisi <a href="#event-metodlar-uchun-jquery-sintaksisi" id="event-metodlar-uchun-jquery-sintaksisi"></a>

jQueryda, ko'plab DOM eventlari jQuery metodlari bilan bir xil.

Sahifadagi barcha paragraflarga click hodisasini berish uchun bunday qilishingiz mumkin:

```
$("p").click(); 
```

Keyingi qadam esa, o'sha holat sodir bo'lganda qanday amallar bajarilishini qo'shish. Ko'pincha funksiya qo'shishingiz kerak bo'ladi:

```
$("p").click(function(){
  // action goes here!!
}); 
```

### jQueryning ko'p ishlatilgan Event metodlar <a href="#jquery-eng-kop-ishlatilgan-event-metodlar" id="jquery-eng-kop-ishlatilgan-event-metodlar"></a>

**$(document).ready()**

`$(document).ready()` metodi  hujjat to'liq yuklangandan so'ng, funksiyalarni ishga tushirishga imkon beradi. Bu event jQuery sintaksisi bo'limida to'liq tushuntirilgan.

**click()**

`click()` metodi hodisa boshqaruvchisini HTML elementiga biriktiradi.

Foydalanuvchi HTML elementini bosganida funktsiya bajariladi.

Masalan, quyidagi misolda:  `<p>` elemtida click eventi ishga tushganda joriy \<p> elementi yarinsin:

```
$("p").click(function(){
  $(this).hide();
});
```

**dblclick()**

`dblclick()` metodi hodisa boshqaruvchi funksiyani HTML elementiga biriktiradi.

HTML elementi ikki marta bosilganida funktsiya ishga tushadi.

```
$("p").dblclick(function(){
  $(this).hide();
});
```

**mouseenter()**

`mouseenter()` metodi hodisa boshqaruvchi funksiyani HTML elementiga biriktiradi.

Sichqoncha kursori HTML elementiga olib borilganda funktsiya ishga tushadi.

```
$("#p1").mouseenter(function(){
  alert("You entered p1!");
});
```

**mouseleave()**

`mouseleave()` metodi hodisa boshqaruvchi funksiyani HTML elementiga biriktiradi.

Sichqoncha kursori HTML elementidan olinganda funksiya ishga tushadi.

```
$("#p1").mouseleave(function(){
  alert("Bye! You now leave p1!");
});
```

**mousedown()**

`mousedown()` metodi hodisa boshqaruvchi funksiyani HTML elementiga biriktiradi.

Sichqoncha HTML elementi ustida bo'lgan paytda uning chap, o'rta yoki o'ng tugmasi bosilganda funksiya ishga tushadi:

```
$("#p1").mousedown(function(){
  alert("Mouse down over p1!");
});
```

**mouseup()**

`mouseup()`  metodi hodisa boshqaruvchi funksiyani HTML elementiga biriktiradi.

Sichqoncha HTML elementi ustida bo'lgan paytda uning chap, o'rta yoki o'ng tugmasi qo'yib yuborilganida funksiya ishga tushadi:

```
$("#p1").mouseup(function(){
  alert("Mouse up over p1!");
});
```

**hover()**

`hover()` metodi ikkita funksiyani oladi va u`mouseenter()` hamda `mouseleave()` funksiyalarining birikmasi hisoblanadi.

Birinchi funksiya sichqoncha HTML elementiga kirganda, ikkinchi funksiya esa sichqoncha HTML elementidan chiqqanda bajariladi:

```
$("#p1").hover(function(){
  alert("You entered p1!");
},
function(){
  alert("Bye! You now leave p1!");
});
```

**focus()**

`focus()` metodi hodisa boshqaruvchi funksiyani HTMLning forma maydoniga biriktiradi.

Forma maydoni focus bo'lganida funksiya ishga tushadi:

```
$("input").focus(function(){
  $(this).css("background-color", "#cccccc");
});
```

**blur()**

`blur()` metodi HTMLning forma maydoniga hodisani boshqaruvchi funksiyani biriktiradi.

Forma maydonidan fokusdan chiqganida funksiya ishga tushadi:

```
 $("input").blur(function(){
  $(this).css("background-color", "#ffffff");
});
```

### on() metodi <a href="#on-metodi" id="on-metodi"></a>

`on()` metodi tanlangan elementlar uchun bir yoki bir nechta hodisa boshqaruvchilarini biriktiradi.

`<p>` elementiga click hodisasini biriktiramiz:

```
$("p").on("click", function(){
  $(this).hide();
}); 
```

bir qancha hodisa boshqaruvchilarini  `<p>` elementiga qo'shamiz:

```
$("p").on({
  mouseenter: function(){
    $(this).css("background-color", "lightgray");
  },
  mouseleave: function(){
    $(this).css("background-color", "lightblue");
  },
  click: function(){
    $(this).css("background-color", "yellow");
  }
}); 
```
