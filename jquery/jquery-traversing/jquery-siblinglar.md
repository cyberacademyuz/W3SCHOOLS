# jQuery Siblinglar

JQuery yordamida elementning siblinglarini topish uchun DOM shajarasida gorizontal tarzda harakatlanishingiz mumkin.

Siblinglar - bir ota elementda joylashgan bo'ladi

### DOM shajarasi bo'ylab gorizontal harakatlanish <a href="#gorizontal-tarzda-dom-dagi-elementlararo-harakatlanish" id="gorizontal-tarzda-dom-dagi-elementlararo-harakatlanish"></a>

DOM shajarasida yon tomonga o'tish uchun juda ko'p foydali jQuery metodlar mavjud:

* `siblings()`
* `next()`
* `nextAll()`
* `prev()`
* `prevAll()`
* `prevUntil()`

### jQuery siblings() metodi <a href="#jquery-siblings-metodi" id="jquery-siblings-metodi"></a>

`siblings()` metodi tanlangan elementning barcha siblinglarini qaytaradi

Quyidagi misolda `<h2>` elementining barcha siblinglari qaytarilgan:

```
 $(document).ready(function(){
  $("h2").siblings();
}); 
```

Yana qo'shimcha qidirish imkoniyatidan foydalanishingiz ham mumkin.

Quyidagi misol `<h2>` siblinglari bo'lgan barcha `<p>` elementlarini qaytaradi:

```
$(document).ready(function(){
  $("h2").siblings("p");
});
```

### jQuery next() metodi <a href="#jquery-next-metodi" id="jquery-next-metodi"></a>

`next()` metodi tanlangan elementdan keyingi siblingni qaytaradi.

Quyidagi misol `<h2>` elementining keyingi siblingini qaytaradi:

```
$(document).ready(function(){
  $("h2").next();
}); 
```

### jQuery nextAll() metodi <a href="#jquery-nextall-metodi" id="jquery-nextall-metodi"></a>

`nextAll()` metodi tanlangan elementdan keyingi barcha siblinglarni qaytaradi.

Quyidagi misolda `<h2>` elementining barcha keyingi siblinglari qaytarilmoqda:

```
$(document).ready(function(){
  $("h2").nextAll();
}); 
```

### jQuery nextUntil() metodi <a href="#jquery-nextuntil-metodi" id="jquery-nextuntil-metodi"></a>

`nextUntil()` metodi ikkita tanlangan argumentlar orasidagi siblinglarni qaytaradi.

Quyidagi misolda `<h2>` va `<h6>` orasidagi barcha sibling elementlar qaytarilayapti:

```
$(document).ready(function(){
  $("h2").nextUntil("h6");
}); 
```

### jQuery prev(), prevAll() & prevUntil() metodlari <a href="#jquery-prev-prevall-prevuntil-metodlari" id="jquery-prev-prevall-prevuntil-metodlari"></a>

`prev()`, `prevAll()` & `prevUntil()` metodlari yuqorida ko'rsatgan metodlarimiz bilan bir xil ishlaydi, ammo teskari holatda: ular tanlangan elementning oldingi siblinglarini qaytaradi.
