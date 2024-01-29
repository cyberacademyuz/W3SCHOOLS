# jQuery Add

jQuery bilan yangi elementlar/kontentlar qo'shish oson.

### Yangi HTML kontentini qo'shish <a href="#yangi-html-kontent-qoshish" id="yangi-html-kontent-qoshish"></a>

Yangi kontent qo'shish uchun ishlatiladigan 4 ta metodni ko'rib chiqamiz:

* `append()` - tanlangan elementlarning oxiriga kontent qo'shadi
* `prepend()` - tanlangan elementlarni boshiga kontent qo'shadi
* `after()` - tanlangan elementlardan keyin kontent qo'shadi
* `before()` - tanlangan elementlardan oldin kontent qo'shadi

### jQuery append() metodi <a href="#jquery-append-metodi" id="jquery-append-metodi"></a>

jQuery append() metodi kontentni tanlangan HTML elementning oxiriga qo'yadi.

```
$("p").append("Some appended text.");
```

### jQuery prepend() metodi <a href="#jquery-prepend-metodi" id="jquery-prepend-metodi"></a>

jQuery append() metodi kontentni tanlangan HTML elementning boshiga qo'yadi.

```
$("p").prepend("Some prepended text.");
```

### append() va prepend() orqali bir nechta elementlar qo'shish <a href="#bir-nechta-elementlarni-append-va-prepend-orqali-qoshish" id="bir-nechta-elementlarni-append-va-prepend-orqali-qoshish"></a>

Yuqoridagi ikkala misolda ham tanlangan HTML elementlarining boshiga/oxiriga faqatgia bir qancha matn/HTML kiritdik.

Biroq, `append()` va `prepend()` metodlari cheklanmagan miqdorda yangi elementlarni parametr sifatida qabul qilishi mumkin. Yangi elementlar (yuqoridagi misollarda qilganimiz kabi) matn/HTML. jQuery yoki JavaScript kodi va DOM elementlari yordamida yaratilishi mumkin.

Quyidagi misolda bir nechta yangi elementlar yaratamiz. Elementlar matn/HTML, jQuery va JavaScript/DOM orqali yaratilgan. Keyin yangi elementlarni `append()` metodi bilan matnga qo'shamiz (bu `prepend()` bilan ham ishlaydi):

```
function appendText() {
  var txt1 = "<p>Text.</p>";               // Create element with HTML 
  var txt2 = $("<p></p>").text("Text.");   // Create with jQuery
  var txt3 = document.createElement("p");  // Create with DOM
  txt3.innerHTML = "Text.";
  $("body").append(txt1, txt2, txt3);      // Append the new elements
} 
```

### jQuery after() va before() metodlari <a href="#jquery-after-va-before-metodlari" id="jquery-after-va-before-metodlari"></a>

jQueryning `after()` metodi kontentni tanlangan HTML elementlaridan keyin qo'shadi.

jQueryning `before()` metodi konentni tanlangan HTML elementlaridan oldin qo'shadi.

```
$("img").after("Some text after");

$("img").before("Some text before");
```

### after() va before() orqali bir nechta elementlar qo'shish <a href="#bir-nechta-elementlarni-after-va-before-bilan-qoshish" id="bir-nechta-elementlarni-after-va-before-bilan-qoshish"></a>

Yuqoridagi ikkala misolda ham tanlangan HTML elementlarining boshiga/oxiriga faqatgia bir qancha matn/HTML kiritdik.

Biroq, `after()` va `before()` metodlari cheklanmagan miqdorda yangi elementlarni parametr sifatida qabul qilishi mumkin. Yangi elementlar (yuqoridagi misollarda qilganimiz kabi) matn/HTML. jQuery yoki JavaScript kodi va DOM elementlari yordamida yaratilishi mumkin.

Quyidagi misolda bir nechta yangi elementlar yaratamiz. Elementlar matn/HTML, jQuery va JavaScript/DOM orqali yaratilgan. Keyin yangi elementlarni `after()` metodi bilan matnga qo'shamiz (bu `before()` bilan ham ishlaydi):

```
function afterText() {
  var txt1 = "<b>I </b>";                    // Create element with HTML 
  var txt2 = $("<i></i>").text("love ");     // Create with jQuery
  var txt3 = document.createElement("b");    // Create with DOM
  txt3.innerHTML = "jQuery!";
  $("img").after(txt1, txt2, txt3);          // Insert new elements after <img>
} 
```
