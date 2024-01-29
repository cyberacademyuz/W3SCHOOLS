# jQuery Get

jQuery HTML elementlarini va attributlarini manipulatsiya va o'zgartirish uchun kuchli metodlarni o'z ichiga olgan.

### jQuery DOM manipulatsiyasi <a href="#jquery-dom-ni-manipulatsiya-qilish" id="jquery-dom-ni-manipulatsiya-qilish"></a>

jQueryning eng muhim jihatlaridan biri bu DOM ni manipulatsiya qila olish imkoni borligi.

jQuery DOM elementlarini va attributlarini manipulatsiya qilish uchun mo'ljallangan bir qancha metodlar bilan birga keladi.

{% hint style="warning" %}
**DOM = Document Object Model**

DOM HTML va XML hujjatlariga murojaat qilish standartini belgilaydi:

"W3C Document Object Model (DOM) - bu dasturlar va skriptlarga hujjat tarkibi, tuzilishi va stiliga dinamik tarzda murojaat qilish va yangilash imkonini beruvchi platforma va  neytral-til interfeysi."
{% endhint %}

### Get Kontent - text(), html() va val() <a href="#kontentni-olib-kelish-text-html-va-val" id="kontentni-olib-kelish-text-html-va-val"></a>

DOM manipulyatsiyasi uchun uchta oddiy, ammo foydali jQuery metodlar:

* `text()` - tanlangan elementning matn kontentini qaytaradi yoki o'rnatadi
* `html()` - tanlangan elementning HTML kontentini qaytaradi yoki o'rnatadi (HTML markuplarini bilan)
* `val()` - forma maydonlaridagi qiymatlarni qaytaradi yoki o'rnatadi.

Quyidagi misolda qanday qilib kontentni jQuery ning `text()` va `html()` metodlari orqali kontentni olib kelish ko'rsatilgan:

```
$("#btn1").click(function(){
  alert("Text: " + $("#test").text());
});
$("#btn2").click(function(){
  alert("HTML: " + $("#test").html());
});
```

Quyidagi misolda esa forma maydonlaridan qiymatlarni jQuery ning `val()` metodidan foydalangan holda olib kelish ko'rsatilgan:

```
$("#btn1").click(function(){
  alert("Value: " + $("#test").val());
});
```

### Attributlarni olish - attr() <a href="#attributlarni-olib-kelish-attr" id="attributlarni-olib-kelish-attr"></a>

jQueryning `attr()` metodi attributlarning qiymatlarini olish uchun ishlatiladi.

Quyidagi misolda `href` attributidagi link qiymatini qanday qilib olib kelish ko'rsatiladi:

```
$("button").click(function(){
  alert($("#w3s").attr("href"));
});
```

Keyingi bo'limda qanday qilib qiymatlarni joylashtirish (o'zgartirish) ni ko'rib chiqamiz.
