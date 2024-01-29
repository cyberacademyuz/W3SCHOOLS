# jQuery Remove

jQuery orqali HTML elementlarini olib tashlash oson.

### Elementlarni/Kontentni olib tashlash <a href="#elementlarnikontentni-olib-tashlash" id="elementlarnikontentni-olib-tashlash"></a>

Elementlarni va kontentni olib tashlash uchun, jQuery da asosan 2 ta metod mavjud:

* `remove()` - Tanlangan elementni (va uning bola elementini ham) olib tashlaydi
* `empty()` - Tanlangan elementining ichidagi elementlarni olib tashlaydi

### jQuery remove() metodi <a href="#jquery-remove-metodi" id="jquery-remove-metodi"></a>

jQueryning `remove()` metodi tanlangan elementni (va uning bola elementini ham) olib tashlaydi

```
 $("#div1").remove();
```

### jQuery empty() metodi <a href="#jquery-empty-metodi" id="jquery-empty-metodi"></a>

jQueryning empty() metodi tanlangan elementining ichidagi elementlarni olib tashlaydi

```
$("#div1").empty();
```

### Olib tashlanadigan elementlarni filterlash <a href="#olib-tashlanadigan-elementlarni-filterlash" id="olib-tashlanadigan-elementlarni-filterlash"></a>

jQueryning `remove()` metodi olib tashlanadigan elementlarni filterlash imkonini beruvchi bitta parametr qabul qiladi.

Parametr jQueryning selector sintaksislaridan istalgan biri bo'lishi mumkin

Ushbu misoldagi kod barcha `class="test"` ga ega `<p>` elementlarini olib tashlaydi:

```
$("p").remove(".test"); 
```

Ushbu misoldagi kod esa barcha `class="test"` va `class="demo"` ga ega `<p>` elementlarini olib tashlaydi:

```
$("p").remove(".test, .demo"); 
```
