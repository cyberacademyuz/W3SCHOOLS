# jQuery Ancestorlar

jQuery yordamida elementlarning ancestorlarini topish uchun DOM shajarasi bo'ylab tepaga harakatlanishingiz kerak.

Ancestor - bu ota, bobo, katta bobo va joriy elementdan tepada turgan boshqa elementlar hisoblanadi.

### DOM shajarasi bo'ylab yuqoriga harakatlanish <a href="#dom-da-tepaga-harakatlanish" id="dom-da-tepaga-harakatlanish"></a>

jQuery da DOM shajarasi bo'ylab yuqoriga harakatlanish uchun 3 ta foydali metodlar bor:

* `parent()`
* `parents()`
* `parentsUntil()`

### jQuery parent() metodi <a href="#jquery-parent-metodi" id="jquery-parent-metodi"></a>

`parent()` metodi tanlangan elementning ota elementini to'g'tidan to'g'ri qaytaradi.

Bu metod faqat bitta tepadagi element haqida ma'lumot beradi.

Quyidagi misoldagi kod har bir `<span>` elementlarining ota elementini qaytaradi:

```
$(document).ready(function(){
  $("span").parent();
}); 
```

### jQuery parents() metodi <a href="#jquery-parents-metodi" id="jquery-parents-metodi"></a>

`parents()` metodi tanlangan elementning barcha ota elementlarini qaytaradi, toki hujjatning root elementi `<html>` gacha.

Quyidagi misoldagi kod bizga har bir `<span>` elementlarining barcha ota elementlarini qaytaradi:

```
$(document).ready(function(){
  $("span").parents();
}); 
```

Yana qo'shimcha qidirish imkoniyatidan foydalanishingiz ham mumkin.

Quyidagi misol `<ul>` elementi bo'lgan barcha `<span>` elementlarning ancestorlarini qaytaradi:

```
$(document).ready(function(){
  $("span").parents("ul");
}); 
```

### jQuery parentsUntil() metodi <a href="#jquery-parentsuntil-metodi" id="jquery-parentsuntil-metodi"></a>

`parentsUntil()` metodi berilgan ikkita element orasidagi elementlarni qaytaradi.

Quyidagi misoldagi kod bizga `<span>` va `<div>` elementlari orasidagi elementlarni qaytaradi:

```
$(document).ready(function(){
  $("span").parentsUntil("div");
}); 
```
