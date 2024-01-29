# jQuery CSS classlar

jQuery yordamida elementlarning stillarini boshqarish qilish oson.

### jQuery CSS manipulatsiyasi <a href="#jquery-css-manipulatsiyasi" id="jquery-css-manipulatsiyasi"></a>

jQuery da CSSni boshqarish uchun har xil metodlari mavjud. Biz quyidagi metodlarni ko'rib chiqamiz:

* `addClass()` - Tanlangan elementga bitta yoki undan ko'p class qo'shadi
* `removeClass()` - Tanlangan elementdan bitta yoki undan ko'p classlarni olib tashlaydi
* `toggleClass()` - Tanlangan elementlarnining classlarini qo'shish yoki olib tashlashni bajaradi.
* `css()` - style attributini beradi yoki qaytaradi

### Misol Stylesheet <a href="#misol-uchun-stylesheet" id="misol-uchun-stylesheet"></a>

Ushbu sahifadagi barcha misollar uchun quyidagi stylesheet ishlatiladi:

```
.important {
  font-weight: bold;
  font-size: xx-large;
}

.blue {
  color: blue;
}
```

### jQuery addClass() metodi <a href="#jquery-addclass-metodi" id="jquery-addclass-metodi"></a>

Quyidagi misolda turli elementlarga class atributlarini qanday qo'shish kerakligi ko'rsatilgan Albatta, classlarni qo'shganda bir nechta elementlarni tanlashingiz mumkin:

```
$("button").click(function(){
  $("h1, h2, p").addClass("blue");
  $("div").addClass("important");
});
```

AddClass() metodida bir nechta classlarni ham berishingiz mumkin:

```
$("button").click(function(){
  $("#div1").addClass("important blue");
});
```

### jQuery removeClass() metodi <a href="#jquery-removeclass-metodi" id="jquery-removeclass-metodi"></a>

Quyidagi misolda turli elementlardan ma'lum bir class atributini olib tashlash ko'rsatilgan:

```
$("button").click(function(){
  $("h1, h2, p").removeClass("blue");
});
```

### jQuery toggleClass() metodi <a href="#jquery-toggleclass-metodi" id="jquery-toggleclass-metodi"></a>

Quyidagi misolda `toggleClass()` metodidan qanday foydalanish kerakligi ko'rsatilgan. Ushbu metod tanlangan elementlarnining classlarini qo'shish yoki olib tashlashni bajaradi.

```
$("button").click(function(){
  $("h1, h2, p").toggleClass("blue");
});
```

### jQuery css() metodi <a href="#jquery-css-metodi" id="jquery-css-metodi"></a>

jQuery `css()` metodini keyingi bo'limlarda ko'rib chiqamiz
