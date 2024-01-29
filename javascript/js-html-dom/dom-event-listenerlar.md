# DOM Event listenerlar

### addEventListener() metodi

{% code title="Foydalanuvchi tugmani bosganida ishga tushadigan event listener qo'shish :" %}
```
document.getElementById("myBtn").addEventListener("click", displayDate);
```
{% endcode %}

`addEventListener()` metodi berilgan elementga hodisa boshqaruvchisini biriktiradi.

`addEventListener()` metodi hodisa boshqaruvchisini elementga mavjud hodisa boshqaruvchilarini o'zgartirmasdan turib biriktiradi.

Bitta elementga bir nechta hodisa boshqaruvchilarini qo'shishingiz mumkin.

Bitta elementga bir xil turdagi ko'plab hodisa boshqaruvchilarini qo'shishingiz mumkin

Hodisa tinglovchilarini nafaqat HTML elementlariga balki har qanday DOM obyektiga qo'shishingiz mumkin. Masalan window obyektiga.

`addEventListener()` metodi hodisaning yuqoriga ko'tarilishiga qanday munosabatda bo'lishini nazorat qilishni osonlashtiradi.

`addEventListener()` metodidan foydalanganda, JavaScript kodini o'qish osonlashishi uchun HTML belgilaridan ajratiladi va HTML belgilashni nazorat qilmaganingizda ham hodisa tinglovchilarini qo'shish imkonini beradi.

`removeEventListener()` metodi yordamida hodisa tinglovchisini osongina olib tashlashingiz mumkin.

### Sintaksis

```
element.addEventListener(event, function, useCapture);
```

Birinchi parametr hodisaning turi (masalan, " `click`" yoki " `mousedown`" yoki boshqa [HTML DOM hodisasi](https://www-w3schools-com.translate.goog/jsref/dom\_obj\_event.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp).)

Ikkinchi parametr - hodisa sodir bo'lganda chaqirilayotgan funksiya.

Uchinchi parametr esa `boolean` qiymat boʻlib, hodisa ko'tarilishi yoki hodisani yozib olishdan foydalanishni belgilaydi. Bu parametrdan foydalanish ixtiyoriy.

{% hint style="warning" %}
E'tibor bering, hodisa uchun "on" prefiksidan foydalanmaysiz; "onclick" o'rniga "click" dan foydalanasiz.
{% endhint %}

### Elementga hodisa boshqaruvchisini qo'shing

{% code title="Foydalanuvchi elementni bosganida "Salom dunyo!" matnli alertni chiqarish:" %}
```
element.addEventListener("click", function(){ alert("Hello World!"); });
```
{% endcode %}

Siz alohida funksiyaga ham murojaat qilishingiz mumkin:

{% code title="Foydalanuvchi elementni bosganida "Salom dunyo!" matnli alertni chiqarish:" %}
```
element.addEventListener("click", myFunction);

function myFunction() {
  alert ("Hello World!");
}
```
{% endcode %}

### Xuddi shu elementga ko'plab hodisa boshqaruvchilarini qo'shish

`addEventListener()` metodi mavjud hodisalarni o'zgartirmasdan, bita elementga ko'plab hodisalar qo'shish imkonini beradi:

```
element.addEventListener("click", myFunction);
element.addEventListener("click", mySecondFunction);
```

Siz bir xil elementga turli hodisalar qo'shishingiz mumkin:

```
element.addEventListener("mouseover", myFunction);
element.addEventListener("click", mySecondFunction);
element.addEventListener("mouseout", myThirdFunction);
```

### Window obyektiga hodisa boshqaruvchisini qo'shish

`addEventListener()` metodi HTML elementlari, HTML hujjati, window obyekti yoki `xmlHttpRequest` obyekti kabi hodisalarni qo'llab-quvvatlaydigan boshqa obyektlar kabi istalgan HTML DOM obyektiga hodisa tinglovchilarini qo'shish imkonini beradi.

{% code title="Foydalanuvchi window oʻlchamini oʻzgartirganda ishga tushadigan hodisa tinglovchisini qoʻshish:" %}
```
window.addEventListener("resize", function(){
  document.getElementById("demo").innerHTML = sometext;
});
```
{% endcode %}

### O'tkazish parametrlari

Parametr qiymatlarini o'tkazishda berilgan funksiyani parametrlar bilan chaqiradigan "anonim funksiya" dan foydalanish:

```
element.addEventListener("click", function(){ myFunction(p1, p2); });
```

### Event bubling yoki Event Capturing ?

HTML DOM-da hodisalarni tarqatishning ikki yo'li mavjud: bubling va Capturing.

Event bubling - bu hodisa sodir bo'lganda element tartibini aniqlash usulidir. Agar sizda \<div> elementi ichida \<p> elementi bo'lsa va foydalanuvchi \<p> ​​elementiga bosgan bo'lsa, qaysi elementning "click" hodisasi birinchi bo'lib ishlov berilishi kerak ?

Bubblingda eng ohirigi elementning hodisasi birinchi boʻlib olinadi, keyin undan avvalgilarining hodisalari: avval \<p> elementining click hodisasi, keyin esa \<div> elementining click hodisasi ishlaydi.

_Capturingda eng birinchi elementning hodisasi birinchi bo'lib olinadi keyin uning ichidagi elementlarning hodisalari_: avval \<div> elementining click hodisasi, keyin esa \<p> elementining click hodisasi ishlanadi.

`addEventListener()` metodi yordamida `"useCapture"` parametridan foydalanib bubling turini belgilashingiz mumkin:

```
addEventListener(event, function, useCapture);
```

Standart qiymat false bo'lganida, u bubblingdan foydalanadi, qiymat true bo'lganida, hodisa capturingdan foydalanadi.

```
document.getElementById("myP").addEventListener("click", myFunction, true);
document.getElementById("myDiv").addEventListener("click", myFunction, true);
```

### removeEventListener() metodi

`removeEventListener()` metodi `addEventListener()`  metodi bilan biriktirilgan hodisa boshqaruvchisini olib tashlaydi:

```
element.removeEventListener("mousemove", myFunction);
```

### HTML DOM hodisasi obyektiga havola

Barcha HTML DOM hodisalarining roʻyxatini koʻrish uchun bizning HTML DOM hodisa obyekti haqida maʼlumotnoma sahifamizga o'ting.
