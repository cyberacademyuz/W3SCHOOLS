# jQuery Fade

jQuery yordamida elementlarga fade effektini bera olasiz.

<figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

#### Misollar <a href="#misollar" id="misollar"></a>

[<mark style="color:green;">jQuery\_fadeIn()</mark>](https://www.w3schools.com/jquery/tryit.asp?filename=tryjquery\_fadein)\
jQueryning fadeIn() metodini ko'rsatib berish.

[<mark style="color:green;">jQuery\_fadeOut()</mark>](https://www.w3schools.com/jquery/tryit.asp?filename=tryjquery\_fadeout)\
jQueryning fadeOut() metodini ko'rsatib berish.

[<mark style="color:green;">jQuery.fadeToggle()</mark>](https://www.w3schools.com/jquery/tryit.asp?filename=tryjquery\_fadetoggle)\
jQuery fadeToggle() metodini ko'rsatib berish.

[<mark style="color:green;">jQuery.fadeTo()</mark>](https://www.w3schools.com/jquery/tryit.asp?filename=tryjquery\_fadeto)\
jQueryning fadeTo() metodini ko'rsatib berish.

### jQuery Fade metodlari <a href="#jquery-fade-metodlari" id="jquery-fade-metodlari"></a>

jQuery orqali elementni fade effekti yordamida ko'rinishi berkitilishini qo'sha olasiz.

jQuery da quyidagi fade metodlari mavjud:

* fadeIn()
* fadeOut()
* fadeToggle()
* fadeTo()

### jQuery fadeIn metodi <a href="#jquery-fadein-metodi" id="jquery-fadein-metodi"></a>

jQueryning `fadeIn()` metodi berkitilgan elementni fade effekti bilan ko'rsatish uchun ishlatiladi.

**Sintaksis**

```
$(selector).fadeIn(speed,callback);
```

Ixtiyoriy speed parametri effektning davomiyligini belgilaydi. U quyidagi qiymatlarni qabul qiladi: "slow", "fast", millisekundlar.

Ixtiyoriy callback parametri fade effekti bajarilgandan keyin ishga tushadigan funksiya hisoblanadi.

Quyidagi misolda `fadeIn()` metodining har xil tarzda amalga oshirilishini ko'ramiz:

```
$("button").click(function(){
  $("#div1").fadeIn();
  $("#div2").fadeIn("slow");
  $("#div3").fadeIn(3000);
}); 
```

### jQuery fadeOut metodi <a href="#jquery-fadeout-metodi" id="jquery-fadeout-metodi"></a>

jQueryning `fadeOut()` metodi ko'rsatilgan elementni fade effekti bilan berkirish uchun ishlatiladi.

**Sintaksis**

```
$(selector).fadeOut(speed,callback);
```

Ixtiyoriy speed parametri effektning davomiyligini belgilaydi. U quyidagi qiymatlarni qabul qiladi: "slow", "fast", millisekundlar.

Ixtiyoriy callback parametri fade effekti bajarilgandan keyin ishga tushadigan funksiya hisoblanadi.

Quyidagi misolda `fadeOut()` metodining har xil tarzda amalga oshirilishini ko'ramiz:

```
$("button").click(function(){
  $("#div1").fadeOut();
  $("#div2").fadeOut("slow");
  $("#div3").fadeOut(3000);
}); 
```

### jQuery fadeToggle metodi <a href="#jquery-fadetoggle-metodi" id="jquery-fadetoggle-metodi"></a>

jQueryning fadeToggle() metodi `fadeIn()` va `fadeOut()` metodlarini birlashtiriadi

**Sintaksis**

```
$(selector).fadeToggle(speed,callback);
```

Ixtiyoriy speed parametri effektning davomiyligini belgilaydi. U quyidagi qiymatlarni qabul qiladi: "slow", "fast", millisekundlar.

Ixtiyoriy callback parametri fade effekti bajarilgandan keyin ishga tushadigan funksiya hisoblanadi.

Quyidagi misolda `fadeToggle()` metodining har xil tarzda amalga oshirilishini ko'ramiz:

```
$("button").click(function(){
  $("#div1").fadeToggle();
  $("#div2").fadeToggle("slow");
  $("#div3").fadeToggle(3000);
}); 
```

### jQuery fadeTo metodi <a href="#jquery-fadeto-metodi" id="jquery-fadeto-metodi"></a>

jQuery fadeTo() metodi ma'lum bir shaffoflikka (0 dan 1 gacha qiymat orasida) o'tishga imkon beradi.

**Sintaksis**

```
$(selector).fadeTo(speed,callback);
```

Talab qilinadigan speed parametri effektning davomiyligini belgilaydi. U quyidagi qiymatlarni qabul qiladi: "slow", "fast", millisekundlar..

FadeTo() metodida talab qilinadigan `opacity` parametri berilgan shaffoflikka (0 dan 1 gacha bo'lgan qiymat) o'tishni belgilaydi.

Ixtiyoriy callback parametri funksiya tugagandan so'ng bajarilishi kerak bo'lgan funksiyadir.

Quyidagi misolda `fadeToggle()` metodining har xil tarzda amalga oshirilishini ko'ramiz:

```
$("button").click(function(){
  $("#div1").fadeTo("slow", 0.15);
  $("#div2").fadeTo("slow", 0.4);
  $("#div3").fadeTo("slow", 0.7);
}); 
```
