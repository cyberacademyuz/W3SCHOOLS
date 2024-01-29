# Qayerga joylashtirish

## \<script> tegi

HTMLda javascript kodlari `<script>` va `</script>` teglari orasida yoziladi.

{% code title="Misol" %}
```html
<script>
     document.getElementById("demo").innerHTML = "My First JavaScript";
</script> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto" %}

{% hint style="warning" %}
Eski javascript kodlarda type atributidan foydalanish mumkin. \<script type="text/javascript">\
Type atributi talab qilinmaydi. Javascript HTMLda default skript til hisoblanadi.
{% endhint %}

## JavaScript funksiyalari va hodisa(event)lari

JavaScriptdagi `function`  bu JavaScript kodning bir bloki, u "chaqirilganida" funksiya bloki ichidagi kodlar ishga tushadi.

Masalan, foydalanuvchi tugmani bosishi kabi biror hodisa sodir bo'lganida, funksiya chaqirilishi mumkin.

{% hint style="warning" %}
Keyingi bo'limlarida funksiyalar va hodisalar haqida ko'proq bilib olasiz.
{% endhint %}

## \<head> yoki \<body> ichida javascript&#x20;

HTML ichiga istalgancha skriptlar joylashtirishingiz mumkin.

Skriptlarni HTML-sahifaning `<body>` yoki `<head>` elementi ichida yoki ikkalasida ham joylashtirish mumkin.

## \<head> ichida javascript

Ushbu misolda javascript funksiyasi HTML sahifaning `<head>` qismiga joylashtirilgan.

Tugma bosilganida funksiya ishga tushadi:

```html
<!DOCTYPE html>
<html>
<head>
  <script>
    function myFunction() {
      document.getElementById("demo").innerHTML = "Paragraph changed.";
    }
  </script>
</head>
<body>

  <h2>Demo JavaScript in Head</h2>

  <p id="demo">A Paragraph</p>
  <button type="button" onclick="myFunction()">Try it</button>

</body>
</html>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_head" %}

## \<body> ichida javascript

Ushbu misolda javascript funksiyasi HTML sahifaning `<body>` qismiga joylashtirilgan.

Tugma bosilganida funksiya ishga tushadi:

```html
!DOCTYPE html>
<html>
<body>

  <h2>Demo JavaScript in Body</h2>

  <p id="demo">A Paragraph</p>
  
  <button type="button" onclick="myFunction()">Try it</button>

  <script>
    function myFunction() {
      document.getElementById("demo").innerHTML = "Paragraph changed.";
    }
  </script>

</body>
</html>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_body" %}

{% hint style="warning" %}
Skriptlarni `<body>` elementining pastki qismiga joylashtirish sahifani yuklanish tezligini yaxshilaydi, chunki skriptni o'qish boshqa ma'lumotlarni ekranga chiqishini sekinlashtiradi.
{% endhint %}

## Tashqi fayldagi javascript

Skriptlar tashqi fayllarga ham joylashtirilishi mumkin:

{% code title="Tashqi fayl: myScript.js" %}
```
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
```
{% endcode %}

Tashqi skriptlar bir xil kodlarni turli sahifalarda ishlatishda foydali bo'ladi.

JavaScript fayllar **.js** kengaytmasiga ega.

Tashqi fayldagi skriptdan foydalanish uchun fayl nomini `<script>` tegining `src` atributiga kiriting:

```html
<script src="myScript.js"></script>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_external" %}

Siz tashqi faylning havolasini `<head>` yoki `<body>`ga xohlaganingizcha joylashtirishingiz mumkin.

Skript xuddi `<script>` tegi joylashgan joyda joylashgandek ishlaydi.

{% hint style="warning" %}
Tashqi script fayllarida \<script> tegi bo'lmaydi
{% endhint %}

## Tashqi faylning afzalliklari

Skriptlarni tashqi fayllarga joylashtirishning afzalliklari:

* U HTML va javascript kodni ajratib turadi. (Aralashib ketmaydi)
* Bu HTML va JavaScript kodlarini o'qishni va saqlashni osonlashtiradi
* Keshlangan JavaScript fayllar sahifa yuklanishini tezlashtirishi mumkin

Bir sahifaga bir nechta skript fayllarini qo'shish uchun - bir nechta \<skript> teglaridan foydalaning:

```
<script src="myScript1.js"></script>
<script src="myScript2.js"></script> 
```

## Tashqi faylni ulash

Tashqi skript faylini 3 xil usulda ulash mumkin:

* To'liq URL bilan (veb sahifaning to'liq manzili)
* Fayl joylashuvi orqali (masalan /js/)
* Hech qanday path-dann foydalanmay

Ushbu misolda myScript.js faylini ulash uchun toʻliq URL manzildan foydalanilgan:

```
<script src="https://www.w3schools.com/js/myScript.js"></script> 
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_url" %}

Ushbu misolda myScript.js faylini ulash uchun fayl yo'lidan foydalanilgan:

```
<script src="/js/myScript.js"></script> 
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_url_relative" %}

Ushbu misolda myScript.js faylini ulash uchun hech qanday yo'ldan foydalanilmagan:

```
<script src="myScript.js"></script> 
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_whereto_external" %}

{% hint style="warning" %}
Fayl path-i haqida HTMLning [fayl yo'llari ](../../html/boshlash/fayl-yollari.md)bo'limida o'qishingiz mumkin .
{% endhint %}
