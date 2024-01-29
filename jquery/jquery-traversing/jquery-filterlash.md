# jQuery Filterlash

### first(), last(), eq(), filter() va not() metodlari <a href="#first-last-eq-filter-va-not-metodlari" id="first-last-eq-filter-va-not-metodlari"></a>

Asosiy filterlash metodlari `first()`, `last()`, `eq()`, `filter()` hamda `not()` bo'lib, ular ma’lum bir elementni elementlar guruhidagi joylashuviga qarab tanlash imkonini beradi.

`filtr()` va `not()` kabi boshqa filtrlash metodlari ma'lum bir mezonga mos keladigan yoki mos kelmaydigan elementlarni tanlash imkonini beradi.

### jQuery first() metodi <a href="#jquery-first-metodi" id="jquery-first-metodi"></a>

`first()` metodi tanlangan elementlarning birinchisini qaytaradi.

Quyidagi misoldagi kod birinchi `<div>` elementini tanlaydi:

```
$(document).ready(function(){
  $("div").first();
}); 
```

### jQuery last() metodi <a href="#jquery-last-metodi" id="jquery-last-metodi"></a>

`last()` metodi tanlangan elementlarning oxirgisini qaytaradi.

Quyidagi misoldagi kod oxirgi `<div>` elementini tanlaydi:

```
$(document).ready(function(){
  $("div").last();
}); 
```

### jQuery eq() metodi <a href="#jquery-eq-metodi" id="jquery-eq-metodi"></a>

`eq()` metodi tanlangan elementlarning berilgan indeks raqamiga qarab qaytaradi.

Indeks 0 raqami bilan boshlanadi, shunday ekan birinchi elementning indeksi 1 emas balki 0 bo'ladi. Quyidagi misoldagi kod ikkinchi `<p>` elementini tanlaydi (indeks raqami 1):

```
$(document).ready(function(){
  $("p").eq(1);
}); 
```

### jQuery filter() metodi <a href="#jquery-filter-metodi" id="jquery-filter-metodi"></a>

`filter()` metodi mezonni belgilash imkoniyatini taqdim etadi. Mezonlarga mos kelmaydigan elementlar tanlovdan olib tashlanadi va mos keladiganlari esa qaytariladi.

Quyidagi misoldagi kod "intro" klassiga ega barcha `<p>` elementlarini qaytaradi:

```
$(document).ready(function(){
  $("p").filter(".intro");
}); 
```

### jQuery not() metodi <a href="#jquery-not-metodi" id="jquery-not-metodi"></a>

`not()` metodi esa mezonga mos bo'lmagan barcha elementlarni qaytaradi.

**Maslahat:** `not()` metodi `filter()` metodining teskarisi hisoblanadi.

Quyidagi misoldagi kod "intro" klassiga ega bo'lmagan barcha `<p>` elementlarini qaytaradi:

```
$(document).ready(function(){
  $("p").not(".intro");
}); 
```
