# jQuery noConflict()

Agar jQuerydan foydalanayotgan paytda boshqa frameworklarni ham ishlatmoqchi bo'lsangiz nima qilasiz ?

### jQuery va boshqa JavaScript frameworklari <a href="#jquery-va-boshqa-javascript-frameworklari" id="jquery-va-boshqa-javascript-frameworklari"></a>

Bilganingizdek, jQuery `$` belgisini jQuery qisqartmasi sifatida ishlatadi.

JavaScriptda yana shunga o'xshash frameworklar bor: **Angular**, **Backbone**, **Ember**, **Knockout**, va boshqalar.

**Agarda boshqa JavaScript frameworklari ham `$` belgisidan foydalansachi ?**

Agar ikkita turli framework bir xil qisqartmalardan foydalansa ulardan biri ishlamasligi mumkin.

jQuery jamoasi bu haqida allaqachon o'ylab qo'yishgan va `noConflict()` metodini ishlab chiqishgan.

### jQuery noConflict() metodi <a href="#jquery-noconflict-metodi" id="jquery-noconflict-metodi"></a>

`noConflict()` metodi $ ni olib tashlaydi, shundan keyin boshqa frameworklar ham bu belgidan foydalana oladi.

Albatta jQuerydan foydalanishingiz mumkin, faqatgina $ belgisi o'rniga uning to'liq nomini yozasiz:

```xquery
$.noConflict();
jQuery(document).ready(function(){
  jQuery("button").click(function(){
    jQuery("p").text("jQuery is still working!");
  });
});
```

Bundan tashqari, o'zingizning shortuctingizni osongina yaratishingiz mumkin. `noConflict()` metodi jQuery-ga havolani qaytaradi, uni keyinchalik foydalanish uchun o'zgaruvchida saqlashingiz mumkin. Mana bunga bir misol:

```
var jq = $.noConflict();
jq(document).ready(function(){
  jq("button").click(function(){
    jq("p").text("jQuery is still working!");
  });
});
```

Agar jQuery kodida `$` belgisini ishlatishni bloklagan bo'lsangiz, `$` belgisini ready metodiga parametr sifatida kiritishingiz ham mumkin. Bu esa sizga jQuery ga murojaat qilish uchun `$` belgisidan funksiya ichida foydalanishga ruxsat beradi, tashqarisida esa jQueryni yozishingiz kerak:

```
$.noConflict();
jQuery(document).ready(function($){
  $("button").click(function(){
    $("p").text("jQuery is still working!");
  });
});
```
