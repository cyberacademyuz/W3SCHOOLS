# jQuery Set

### Set Kontent - text(), html() va val() <a href="#kontentni-joylashtirish-text-html-va-val" id="kontentni-joylashtirish-text-html-va-val"></a>

Avvalgi bo'limda o'rgangan metodlarimizni kontentni o'rnatish uchun ham ishlatamiz:

* `text()` - tanlangan elementning matn kontentini qaytaradi yoki o'rnatadi
* `html()` - tanlangan elementning HTML kontentini qaytaradi yoki o'rnatadi (HTML markuplarini bilan)
* `val()` - forma maydonlaridagi qiymatlarni qaytaradi yoki o'rnatadi.

Quyidagi misolda jQuery ning `text()`, `html()` va `val()` metodlari orqali kontentni joylashtirish ko'rsatilgan:

```
$("#btn1").click(function(){
  $("#test1").text("Hello world!");
});
$("#btn2").click(function(){
  $("#test2").html("<b>Hello world!</b>");
});
$("#btn3").click(function(){
  $("#test3").val("Dolly Duck");
});
```

### text(), html() va val() uchun callback funksiya <a href="#text-html-va-val-uchun-callback-funksiya" id="text-html-va-val-uchun-callback-funksiya"></a>

Yuqorida sanab o'tgan metodlarimiz: `text()`, `html()` va `val()` funksiyalarini barchasida callback funksiyani amalga oshirish mumkin. Callback funksiyada 2 ta parametr bo'ladi: tanlangan elementlar ro'yxatidagi joriy elementning indeksi va asl (eski) qiymati. Keyin funksiyadan yangi qiymat sifatida foydalanmoqchi bo'lgan stringni  qaytarasiz.

Quyidagi misolda `html()` va `text()` metodlari callback funksiya bilan birgalikda qo'llash ko'rsatilgan.

```
$("#btn1").click(function(){
  $("#test1").text(function(i, origText){
    return "Old text: " + origText + " New text: Hello world!
    (index: " + i + ")";
  });
});

$("#btn2").click(function(){
  $("#test2").html(function(i, origText){
    return "Old html: " + origText + " New html: Hello <b>world!</b>
    (index: " + i + ")";
  });
});
```

### Attributlarni joylashtirish - attr() <a href="#attributlarni-joylashtirish-attr" id="attributlarni-joylashtirish-attr"></a>

jQuery ning `attr()` metodi attributlarning qiymatlarini joylashtirish/o'zgartirish uchun ishlatiladi.

Quyidagi misolda `href` attributidagi link qiymatini qanday qilib o'zgartirish ko'rsatiladi:

```
$("button").click(function(){
  $("#w3s").attr("href", "https://www.w3schools.com/jquery/");
});
```

Bundan tashqari `attr()` metodi bir nechta attributlarning qiymatini bir vaqtni o'zida yangilash imkonini beradi.

Quyidagi misolda href atributiga ham va title attributiga ham qiymat berish ko'rsatiladi:

```
$("button").click(function(){
  $("#w3s").attr({
    "href" : "https://www.w3schools.com/jquery/",
    "title" : "W3Schools jQuery Tutorial"
  });
});
```

### attr() uchun callback funksiya <a href="#attr-uchun-callback-funksiya" id="attr-uchun-callback-funksiya"></a>

jQuery `attr()` metodida callback funksiyani amalga oshirish mumkin. Callback funksiyada 2 ta parametri bo'ladi: tanlangan elementlar ro'yxatidagi joriy elementning indeksi va asl (eski) qiymati. Keyin funksiyadan yangi atribut qiymati sifatida foydalanmoqchi bo'lgan stringni qaytarasiz.

Quyidagi misolda attr() metodida callback funksiyani amalga oshirish ko'rsatiladi:

```
$("button").click(function(){
  $("#w3s").attr("href", function(i, origValue){
    return origValue + "/jquery/";
  });
});
```
