# jQuery Hide/Show

Berkitish, ko'rsatish, toggle, slide, fade va Animatsiya qilish. WOW!

#### Misollar <a href="#misollar" id="misollar"></a>

[<mark style="color:green;">jQuery.hide()</mark>](https://www.w3schools.com/jquery/tryit.asp?filename=tryjquery\_hide)\
Oddiy jQuery hide() metodini ko'rsatib beradi

<mark style="color:green;">jQuery.hide()</mark>\
Yana bir hide() ni ko'rsatib berish. Matn qismlarini qanday yashirish kerak.

### jQuery hide() va show() <a href="#jquery-hide-va-show" id="jquery-hide-va-show"></a>

jQuery bilan HTML elementlarini `hide()` va `show()` metodlari orqali berkitishingiz va ko'rsatishingiz mumkin:

**Masalan:**

```
$("#hide").click(function(){
  $("p").hide();
});

$("#show").click(function(){
  $("p").show();
}); 
```

**Sintaksis:**

```
$(selector).hide(speed,callback);

$(selector).show(speed,callback); 
```

Ixtiyoriy speed parametri berkitish/ko'rsatish qancha vaqt ichida sodir bo'lishini belgilaydi va "slow", "fast", millisekundlar qiymatlarini qabul qiladi.

Ixtiyoriy callback parametri `hide()` va `show()` metodlari tugatilgandan keyin ishga tushadigan funksiya hisoblanadi (callback funksiyalari haqida keyingi bo'limlarda batafsil bilib olasiz).

Quyidagi misolda speed parametrini hide() yordamida ko'rsatib berilgan:

```
$("button").click(function(){
  $("p").hide(1000);
}); 
```

### jQuery toggle() <a href="#jquery-toggle" id="jquery-toggle"></a>

Bundan tashqari berkitish va ko'rsatish holatlarini almashtirishingiz ham mumkin, buning uchun toggle() metodidan foydalaning.

Ko'rsatilgan elementlar berkitiladi, berkitilgan elementlar ko'rsatiladi:

```
$("button").click(function(){
  $("p").toggle();
}); 
```

**Sintaksis:**

```
$(selector).toggle(speed,callback); 
```

Ixtiyoriy speed parametri berkitish/ko'rsatish qancha vaqt ichida sodir bo'lishini belgilaydi va "slow", "fast", millisekundlar qiymatlarini qabul qiladi.

Ixtiyoriy callback parametri toggle() metodi bajarilgandan keyin ishga tushadigan funksiya hisoblanadi.
