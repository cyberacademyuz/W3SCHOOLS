# jQuery Slayd

jQuery slide metodlari elementlarni tepaga va pastga harakatlantiradi.

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

#### Misollar <a href="#misollar" id="misollar"></a>

<mark style="color:green;">jQuery\_slideDown()</mark>\
jQueryning slideDown() metodini ko'rsatib berish.

<mark style="color:green;">jQuery\_slideUp()</mark>\
jQueryning slideUp() metodini ko'rsatib berish

<mark style="color:green;">jQuery.slideToggle()</mark>\
jQueryning slideToggle() metodini ko'rsatib berish

### jQuery Slide metodlari <a href="#jquery-slide-metodlari" id="jquery-slide-metodlari"></a>

jQueryning slide effekti bilan elementlarni harakatlantira olasiz.

jQueryda quyidagi slide metodlari mavjud:

* `slideDown()`
* `slideUp()`
* `slideToggle()`

### jQuery slideDown() metodi <a href="#jquery-slidedown-metodi" id="jquery-slidedown-metodi"></a>

jQueryning `slideDown()` metodi elementni pastga tushirish uchun ishlatiladi.

**Sintaksis**

```
$(selector).slideDown(speed,callback);
```

Ixtiyoriy speed parametri effektning davomiyligini belgilaydi. U quyidagi qiymatlarni qabul qiladi: "slow", "fast", millisekundlar.

Ixtiyoriy callback parametri slide effekti bajarilgandan keyin ishga tushadigan funksiya hisoblanadi.

Quyidagi misolda `slideDown()` metodi ko'rsatib berilgan:

```
$("#flip").click(function(){
  $("#panel").slideDown();
}); 
```

### jQuery slideUp() metodi <a href="#jquery-slideup-metodi" id="jquery-slideup-metodi"></a>

jQuery `slideUp()` metodi elementni tepaga slide qilish uchun ishlatiladi.

**Sintaksis**

```
$(selector).slideUp(speed,callback);
```

Ixtiyoriy speed parametri effektning davomiyligini belgilaydi. U quyidagi qiymatlarni qabul qiladi: "slow", "fast", millisekundlar.

Ixtiyoriy callback parametri slide effekti bajarilgandan keyin ishga tushadigan funksiya hisoblanadi.

Quyidagi misolda `slideUp()` metodi ko'rsatib berilgan:

```
$("#flip").click(function(){
  $("#panel").slideUp();
}); 
```

### jQuery slideToggle() metodi <a href="#jquery-slidetoggle-metodi" id="jquery-slidetoggle-metodi"></a>

jQuery `slideToggle()` metodi `slideUp()` va `slideDown()` metodlarini birlashtiradi

Agar elementlar pastga tushirlgan bo'lsa slideToggle() ularni yuqoriag ko'taradi

Aksincha bo'lsa unda pastga tushiradi

**Sintaksis**

```
$(selector).slideToggle(speed,callback);
```

Ixtiyoriy speed parametri effektning davomiyligini belgilaydi. U quyidagi qiymatlarni qabul qiladi: "slow", "fast", millisekundlar.

Ixtiyoriy callback parametri slide effekti bajarilgandan keyin ishga tushadigan funksiya hisoblanadi.

Quyidagi misolda `slideToggle()` metodi ko'rsatib berilgan:

```
$("#flip").click(function(){
  $("#panel").slideToggle();
}); 
```
