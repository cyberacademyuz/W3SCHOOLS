# jQuery O'lchamlar

jQuery yordamida element o'lchamlari va brauzer oynasi bilan ishlash ancha qulay.

### jQuery O'lcham metodlari <a href="#jquery-olchamlar-metodlari" id="jquery-olchamlar-metodlari"></a>

jQuery da o'lchamlar bilan ishlashda ishlatiladigan bir qancha muhim metodlar mavjud:

* `width()`
* `height()`
* `innerWidth()`
* `innerHeight()`
* `outerWidth()`
* `outerHeight()`

### jQuery o'lchamlari <a href="#jquery-olchamlari" id="jquery-olchamlari"></a>

<figure><img src="../../.gitbook/assets/img_jquerydim.gif" alt=""><figcaption></figcaption></figure>

### jQuery width() va height() metodlari <a href="#jquery-width-va-height-metodlari" id="jquery-width-va-height-metodlari"></a>

`width()` metodi elementning uzunligini o'zgartiradi yoki u haqidagi ma'lumotni qaytaradi (padding, border va marginlarni istisno qilgan holda)

`height()` metodi elementning balandligini o'zgartiradi yoki u haqidagi ma'lumotni qaytaradi (padding, border va marginlarni istisno qilgan holda)

Quyidagi misolda tanlangan `<div>` elementining balandligi hamda uzunligi haqida ma'lumot beriladi:

```
$("button").click(function(){
  var txt = "";
  txt += "Width: " + $("#div1").width() + "</br>";
  txt += "Height: " + $("#div1").height();
  $("#div1").html(txt);
}); 
```

### jQuery innerWidth() va innerHeight() metodlari <a href="#jquery-innerwidth-va-innerheight-metodlari" id="jquery-innerwidth-va-innerheight-metodlari"></a>

`innerWidth()` metodi elementning uzunligi haqidagi ma'lumotni qaytaradi (paddingni o'z ichiga olgan holda)

`innerHeight()` metodi elementning balandligi haqidagi ma'lumotni qaytaradi (paddingni o'z ichiga olgan holda)

Quyidagi misolda tanlangan `<div>` elementining balandligi hamda uzunligi haqida ma'lumot beriladi:

```
$("button").click(function(){
  var txt = "";
  txt += "Inner width: " + $("#div1").innerWidth() + "</br>";
  txt += "Inner height: " + $("#div1").innerHeight();
  $("#div1").html(txt);
}); 
```

### jQuery outerWidth() va outerHeight() metodlari <a href="#jquery-outerwidth-va-outerheight-metodlari" id="jquery-outerwidth-va-outerheight-metodlari"></a>

`outerWidth()` metodi elementning uzunligi haqidagi ma'lumotni qaytaradi (padding va borderni o'z ichiga olgan holda)

`outerHeight()` metodi elementning balandligi haqidagi ma'lumotni qaytaradi (padding va borderni o'z ichiga olgan holda)

Quyidagi misolda tanlangan `<div>` elementining balandligi hamda uzunligi haqida ma'lumot beriladi:

```
$("button").click(function(){
  var txt = "";
  txt += "Outer width: " + $("#div1").outerWidth() + "</br>";
  txt += "Outer height: " + $("#div1").outerHeight();
  $("#div1").html(txt);
}); 
```

`outerWidth(true)` metodi elementning uzunligi haqidagi ma'lumotni qaytaradi (padding, margin va borderni o'z ichiga olgan holda)

`outerHeight()` metodi elementning balandligi haqidagi ma'lumotni qaytaradi (padding, margin va borderni o'z ichiga olgan holda)

```
$("button").click(function(){
  var txt = "";
  txt += "Outer width (+margin): " + $("#div1").outerWidth(true) + "</br>";
  txt += "Outer height (+margin): " + $("#div1").outerHeight(true);
  $("#div1").html(txt);
}); 
```

### jQuery width() va height() metodlari haqida ko'proq <a href="#jquery-width-va-height-metodlari-haqida-koproq" id="jquery-width-va-height-metodlari-haqida-koproq"></a>

Ushbu misoldagi kod HTML hujjatning balandligi, uzunligi va window o'lchamini (brauzer viewport) qaytaradi:

```
$("button").click(function(){
  var txt = "";
  txt += "Document width/height: " + $(document).width();
  txt += "x" + $(document).height() + "\n";
  txt += "Window width/height: " + $(window).width();
  txt += "x" + $(window).height();
  alert(txt);
}); 
```

Ushbu misoldagi kod tanlangan `<div>` elementining balandligini va uzunligini o'zgartiradi:

```
$("button").click(function(){
  $("#div1").width(500).height(500);
}); 
```
