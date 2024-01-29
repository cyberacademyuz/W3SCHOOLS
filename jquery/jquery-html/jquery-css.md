# jQuery css()

#### jQuery css() metodi <a href="#jquery-css-metodi" id="jquery-css-metodi"></a>

`css()` metodi tanlangan elementlarga bir yoki bir nechta stil qiymatlarini beradi yoki qaytaradi.

### CSS qiymatini qaytarish <a href="#css-qiymatini-qaytarish" id="css-qiymatini-qaytarish"></a>

CSS qiymatini qaytarish uchun quyidagi sintaksisdan foydalaning:

```
css("propertyname");
```

Quyidagi misolda esa background-color qiymatiga ega birinchi element qaytariladi.

```
$("p").css("background-color");
```

### CSS qiymatini qo'shish <a href="#css-qiymatini-qoshish" id="css-qiymatini-qoshish"></a>

CSS qiymatini qo'shish uchun sintaksis:

```
css("propertyname","value");
```

Quyidagi misol barcha `<p>` elementlarining background-color qiymatini <mark style="color:yellow;">yellow</mark> qiladi.

```
 $("p").css("background-color", "yellow");
```

### Turli CSS qiymatlarini joylashtirish <a href="#har-xil-css-qiymatlarini-joylashtirish" id="har-xil-css-qiymatlarini-joylashtirish"></a>

CSSning turli qiymatlarini berish uchun quyidagi sintaksisdan foydalaning:

```
css({"propertyname":"value","propertyname":"value",...});
```

Quyidagi misolda barcha \<p> elementlariga `background-color` va `font-size` qiymatlarini beradi:

```
$("p").css({"background-color": "yellow", "font-size": "200%"});
```
