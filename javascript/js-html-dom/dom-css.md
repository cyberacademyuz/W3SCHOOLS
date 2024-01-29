# DOM CSS

HTML DOM JavaScript-ga HTML elementlarining stillarini o'zgartirish imkonini beradi.

### HTML stilini o'zgartirish

HTML elementining stilini o'zgartirish uchun ushbu sintaksisdan foydalaning:

```
document.getElementById(id).style.property = new style
```

Quyidagi misol `<p>` elementining stilini o'zgartiradi:

```
<html>
<body>

<p id="p2">Hello World!</p>

<script>
document.getElementById("p2").style.color = "blue";
</script>

</body>
</html>
```

### Hodisalardan foydalanish

HTML DOM biror hodisa sodir bo'lganda ma'lum bit kodni bajarishga imkon beradi.

Hodisalar HTML elementlarida "nimadir sodir bo'lganda" brauzer tomonidan yaratiladi:

* Element bosilganda
* Sahifa yuklanganda
* Input maydoni o'zgartirilganda

Ushbu qo'llanmaning keyingi bo'limida hodisalar haqida batafsil bilib olasiz.

Ushbu misol, foydalanuvchi tugmani bosganida `id="id1"` orqali elementning stilini o'zgartiradi:

```
<!DOCTYPE html>
<html>
<body>

<h1 id="id1">My Heading 1</h1>

<button type="button"
onclick="document.getElementById('id1').style.color = 'red'">
Click Me!</button>

</body>
</html>
```

### Ko'proq misol

[Visibility](https://www-w3schools-com.translate.goog/js/tryit.asp?filename=tryjs\_visibility&\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) Elementni qanday qilib ko'rinmas qilish mumkin. Element ko'rsatilishini xohlaysizmi yoki ko'rsatilmasligini ?

### HTML DOMning stil obyektiga havola

HTML DOM stilining barcha xususiyatlarini olish uchun bizning **HTML DOM stil ob'ekti** haqida ma'lumotnoma sahigamizga o'ting.
