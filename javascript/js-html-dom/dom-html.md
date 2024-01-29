# DOM HTML

HTML DOM JavaScript-ga HTML elementlarining tarkibini o'zgartirish imkonini beradi.

### HTMLning tarkibini o'zgartirish

Elementining tarkibini o'zgartirishning eng oson yo'li `innerHTML` xususiyatidan foydalanishdir.

HTML elementining tarkibini o'zgartirish uchun ushbu sintaksisdan foydalaning:

```
document.getElementById(id).innerHTML = new HTML
```

Ushbu misol `<p>` elementining tarkibini o'zgartiradi:

```
<html>
<body>

<p id="p1">Hello World!</p>

<script>
document.getElementById("p1").innerHTML = "New text!";
</script>

</body>
</html>
```

Misolni tushuntirish:

* Yuqoridagi HTML hujjatida `id="p1"` atributiga ega `<p>`elementi bor
* Elementni `id="p1"` bilan olish uchun HTML DOM dan foydalanamiz
* JavaScript ushbu elementning tarkibini (`innerHTML`) "New text!" ga o'zgartiradi.

Ushbu misol `<h1>` elementining tarkibini o'zgartiradi:

```
<!DOCTYPE html>
<html>
<body>

<h1 id="id01">Old Heading</h1>

<script>
const element = document.getElementById("id01");
element.innerHTML = "New Heading";
</script>

</body>
</html>
```

Misolni tushuntirish:

* Yuqoridagi HTML hujjatida `id="id01"` atributiga ega `<h1>` elementi bor
* Elementni `id="id01"`  orqali olish uchun HTML DOM dan foydalanamiz
* JavaScript ushbu elementning tarkibini (`innerHTML`) "New Heading" ga o'zgartiradi

### Atribut qiymatini o'zgartirish

HTML atributining qiymatini o'zgartirish uchun ushbu sintaksisdan foydalaning:

```
document.getElementById(id).attribute = new value
```

Ushbu misol `<img>` elementining src atributidagi qiymatni o'zgartiradi:

```
<!DOCTYPE html>
<html>
<body>

<img id="myImage" src="smiley.gif">

<script>
document.getElementById("myImage").src = "landscape.jpg";
</script>

</body>
</html>
```

Misolni tushuntirish:

* Yuqoridagi HTML hujjatida `id="myImage"` atributiga ega `<img>` elementi bor
* Elementni `id="myImage"` orqali olish uchun HTML DOM dan foydalanamiz
* JavaScript ushbu elementning `src` atributini "smiley.gif" dan "landscape.jpg" ga o'zgartiradi.

### Dinamik HTML tarkibi

JavaScript dinamik HTML tarkibini yaratishi mumkin:

Sana: Chorshanba 05 aprel 2023 11:13:11 GMT+0500 (Pokiston standart vaqti)

```
<!DOCTYPE html>
<html>
<body>

<script>
document.getElementById("demo").innerHTML = "Date : " + Date(); </script>

</body>
</html>
```

### document.write()

JavaScript-da `document.write()`to'g'ridan-to'g'ri HTML chiqish oqimiga yozish uchun ishlatilishi mumkin:

```
<!DOCTYPE html>
<html>
<body>

<p>Bla bla bla</p>

<script>
document.write(Date());
</script>

<p>Bla bla bla</p>

</body>
</html>
```

{% hint style="warning" %}
Hujjat yuklangandan keyin hech qachon `document.write()` dan foydalanmang . U hujjatni qayta yozadi.
{% endhint %}
