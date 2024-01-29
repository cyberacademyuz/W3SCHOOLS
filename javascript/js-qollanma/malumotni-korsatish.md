# Ma'lumotni ko'rsatish

## JavaScriptnining ma'lumotlarni ko'rsatish imkoniyatlari

JavaScript ma'lumotlarni turli yo'llar bilan ko'rsatishi mumkin:

* `innerHTML` dan foydalanib HTML elementiga yozish.
* `document.write()` dan foydalanib HTML sahifada ko'rsatish.
* `window.alert()` dan foydalanib, ogohlantirish oynasini ko'rsatish.
* `console.log()` dan foydalanib brauzer konsolida ko'rsatish.

## innerHTML dan foydalanish

HTML elementiga murojaat qilish uchun JavaScript `document.getElementById(id)` metodidan oladi.

`id` atributi HTML elementini ifodalaydi. `innerHTML` xususiyati HTML tarkibini belgilaydi:

```html
<!DOCTYPE html>
<html>
<body>

    <h1>My First Web Page</h1>
    <p>My First Paragraph</p>

    <p id="demo"></p>

    <script>
        document.getElementById("demo").innerHTML = 5 + 6;
    </script>

</body>
</html>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_output_dom" %}

{% hint style="warning" %}
HTML elementining kontentini innerHTML xususiyati orqali o'zgartirish HTMLda ma'lumotlarni ko'rsatishning keng tarqalgan usuli hisoblanadi.
{% endhint %}

## document.write() dan foydalanish

`document.write()` sinov maqsadlarida foydalanish uchun qulay:

```html
<!DOCTYPE html>
<html>
<body>

<h1>My First Web Page</h1>
<p>My first paragraph.</p>

<script>
document.write(5 + 6);
</script>

</body>
</html>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_output_write" %}

{% hint style="danger" %}
HTML sahifa yuklangandan so'ng `document.write()` dan foydalanish sahifadagi barcha ma'lumotni o'chiradi:
{% endhint %}

```markup
<!DOCTYPE html>
<html>
<body>

<h1>My First Web Page</h1>
<p>My first paragraph.</p>

<button type="button" onclick="document.write(5 + 6)">Try it</button>

</body>
</html> 
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_output_write_over" %}

{% hint style="warning" %}
`document.write()` metodi faqat natijani tekshirib ko'rish uchun ishlatilishi kerak.
{% endhint %}

## window.alert() dan foydalanish

Ma'lumotlarni ko'rsatish uchun ogohlantirish oynasidan foydalanishingiz mumkin:

```markup
<!DOCTYPE html>
<html>
<body>

<h1>My First Web Page</h1>
<p>My first paragraph.</p>

<script>
window.alert(5 + 6);
</script>

</body>
</html>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_output_alert" %}

`window` kalit so'zini yozmasliginggiz ham mumkin.

JavaScript-da `window` obyekti global obyek hisoblanadi. Bu o'zgaruvchilar, xususiyatlar va metodlar standart tarzda window obyektiga tegishli ekanligini anglatadi. Shuningdek, `window` kalit so'zidan foydalanish ixtiyoriy ekanligini anglatadi:

```markup
<!DOCTYPE html>
<html>
<body>

<h1>My First Web Page</h1>
<p>My first paragraph.</p>

<script>
alert(5 + 6);
</script>

</body>
</html> 
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_output_alert2" %}

## console.log() dan foydalanish

Xatolarni to'g'irlash (debuggin) maqsadida ma'lumotlarni ko'rsatish uchun brauzerda `console.log()` metodini chaqirishingiz mumkin.

{% hint style="warning" %}
Debugging haqida keyingi bo'limda batafsil bilib olasiz.
{% endhint %}

```markup
<!DOCTYPE html>
<html>
<body>

<script>
console.log(5 + 6);
</script>

</body>
</html>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_output_console" %}

## Javascript orqali chop etish

JavaScript-da biror bir chop etish obyekti yoki chop etish metodlari mavjud emas.

Siz JavaScript-dan turib tashqi qurilmalariga kira olmaysiz.

Faqatgina istisno tarzda joriy sahifani chop etish uchun brauzerda `window.print()` metodini chaqirishingiz mumkin.

```markup
<!DOCTYPE html>
<html>
<body>

    <button onclick="window.print()">Print this page</button>

</body>
</html>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_output_print" %}
