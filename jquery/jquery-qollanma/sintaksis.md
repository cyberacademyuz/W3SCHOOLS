# Sintaksis

jQuery orqali HTML elementlarini tanlaysiz va ularda amallar bajara olasiz.

### jQuery sintaksisi <a href="#jquery-sintaksisi-2" id="jquery-sintaksisi-2"></a>

jQuery sintaksisi HTML dagi element(lar)ni tanlash va ular ustida amallar bajarish uchun maxsus buyurtma qilingandek qilib ishlangan.

Asosiy sintaksis: **$(selector).action()** hisoblanadi.

* $ belgisi jQuery ni anglatadi
* _(selector)_ esa HTML elementlarini qidirishni bildiradi
* _action()_ esa elementlarda qilinadigan amallarni bildiradi.

Misollar:

`$(this).hide()` - Joriy elementni yashiradi.

`$("p").hide()` - Barcha `<p>` elementlarini yashiradi.

`$(".test").hide()` - Barcha class="test"ga ega elementlarni yashiradi.

`$("#test").hide()` - Barcha id="test" attributiga ega elementlarni yashiradi.

{% hint style="warning" %}
#### CSS selectorlari bilan tanishmisiz? <a href="#siz-css-selectorlari-bilan-tanishmisiz" id="siz-css-selectorlari-bilan-tanishmisiz"></a>

jQuery elementlarni tanlash uchun CSS sintaksisidagi selectorlardan foydalanadi. Selectorlar haqida keyingi bo'limlarda ko'proq ma'lumotga ega bo'lasiz.

**Maslahat:** Mabodo, CSSni bilmasangiz, bizninb CSS darsligimizni o'qishingiz mumkin.
{% endhint %}

### Document Ready Event <a href="#document-ready-event" id="document-ready-event"></a>

Bizning misollarimizdagi barcha jQuery metodlar document ready event ichida yozilganligini payqagan bo'lishingiz mumkin:

```
$(document).ready(function(){

  // jQuery methods go here...

}); 
```

Hujjat bilan ishlashdan avval uning to'liq yuklanishi va tayyor bo'lishini kutish good practice hisoblanadi. Bu sizga JavaScript kodingizni hujjatingizning bosh qismida, asosiy qismidan oldin joylashtirish imkonini beradi.

Quyida, agarda metodlar hujjat yuklanishidan oldin ishga tushsa nimalar bo'lishi haqida aytib o'tamiz:

* Hali yaratilmagan elementni yashirishga urinadi
* Hali yuklanmagan rasmning o'lchamini olishga urinadi

Maslahat: jQuery jamoasi document ready event metodi uchun yanada qisqaroq metod yaratdi:

```
$(function(){

  // jQuery methods go here...

}); 
```

O'zingiz yoqtirgan sintaksisdan foydalaning. Bizning fikrimizcha document ready event ishlatilgan kodni tushunish osonroq.
