# jQuery Descendantlar

jQuery yordamida elementlarning descendantlarini topish uchun DOM bo'ylab harakatlanishingiz mumkin.

Descendant bu bola, nevara, avara va  joriy elementdan pastda turgan boshqa elementlar hisoblanadi.

### DOM shajarasi bo'ylab pastga harakatlanish <a href="#dom-da-pastga-harakat-qilish" id="dom-da-pastga-harakat-qilish"></a>

DOM da DOM shajarasi bo'ylab pastga harakatlanish uchun 2 ta foydali metodlar mavjud:

* `children()`
* `find()`

### jQuery children() metodi <a href="#jquery-children-metodi" id="jquery-children-metodi"></a>

`children()` metodi tanlangan elementning barcha bola elementlarini to'g'ridan to'g'ri qaytaradi.

Bu metod faqat bitta pastdagi element haqida ma'lumot beradi

Quyidagi misoldagi kod har bir `<div>` elementlarining bola elementlarini bevosita qaytaradi:

```
$(document).ready(function(){
  $("div").children();
}); 
```

Yana qo'shimcha qidirish imkoniyatidan foydalanishingiz ham mumkin.

Quyidagi misol "**first**" class nomiga ega barcha `<p>` elementlarini qaytaradi, ular `<div>` ning bevosita bola elementlari hisoblanadi:

```
 $(document).ready(function(){
  $("div").children("p.first");
}); 
```

### jQuery find() metodi <a href="#jquery-find-metodi" id="jquery-find-metodi"></a>

`find()` metodi tanlangan elementning oxirgi descendantigacha qaytaradi.

Quyidagi misolda `<div>` elementi descendentlari ichidagi barcha `<span>` elementlari qaytariladi:

```
$(document).ready(function(){
  $("div").find("span");
}); 
```

Quyidagi misol esa barcha descendantlarni qaytaradi:

```
$(document).ready(function(){
  $("div").find("*");
}); 
```
