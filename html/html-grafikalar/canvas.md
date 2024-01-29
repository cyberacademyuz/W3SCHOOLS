# Canvas

HTMLning  `<canvas>` elementi veb-sahifada grafik rasmlar chizish uchun ishlatiladi.

Chapdagi rasm `<canvas>` bilan yaratilgan. Unda to'rtta element ko'rsatilgan: qizil to'rtburchak, gradientli to'rtburchak, turli rangdagi to'rtburchak va turli rangdagi matn.

## HTMLdagi Canvas nima ?

HTMLning `<canvas>`elementi JavaScript orqali grafik rasmlar chizish uchun ishlatiladi.

`<canvas>` elementi faqat grafik rasmlar uchun konteyner hisoblanadi. Rasmlar chizish uchun JavaScript-dan foydalanishingiz kerak.

Yo'llar, qutilar, doiralar, matn chizish va rasmlar qo'shishning bir necha usullari mavjud.

## Qo'llab quvvatlovchi brauzerlar

Jadvaldagi raqamlar `<canvas>` elementini to'liq qo'llab-quvvatlaydigan brauzerning boshlang'ich versiyasini bildiradi.

| Element nomi | Chrome | Edge | Firefox | Safari |     |
| ------------ | ------ | ---- | ------- | ------ | --- |
| \<canvas>    | 4.0    | 9.0  | 2.0     | 3.1    | 9.0 |

### Kanvasga misollar

Canvas HTML sahifadagi to'rtburchak maydon hisoblanadi. Canvasning chegara chizig'i va kontenti mavjud bo'lmaydi.

Canvas yaratish quyidagi kabi amalga oshiriladi:

```
<canvas id="myCanvas" width="200" height="100"></canvas>
```

Eslatma: Canvas o'lchmani berish uchun har doim `id,` `width`va `height` atributini bering. Chegara qo'shish uchun `style` atributidan foydalaning.

Mana bu, oddiy bo'm bo'sh canvasga misol:

![](<../../.gitbook/assets/image (187).png>)

```
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
</canvas> 
```

## Javascript qo'shish

To'rtburchak canvas maydonini yaratganingizdan so'ng unga chizish uchun Javascript qo'shishingiz shart.

Mana bunga bir nechta misollar:

### Chiziq chizish

![](<../../.gitbook/assets/image (36).png>)

```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.moveTo(0, 0);
ctx.lineTo(200, 100);
ctx.stroke();
</script> 
```

## Aylana chizish

![](<../../.gitbook/assets/image (188).png>)

```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.beginPath();
ctx.arc(95, 50, 40, 0, 2 * Math.PI);
ctx.stroke();
</script> 
```

### Matn chizish

![](<../../.gitbook/assets/image (5).png>)

```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.fillText("Hello World", 10, 50);
</script>
```

### Stroke matn

![](<../../.gitbook/assets/image (28).png>)

```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.strokeText("Hello World", 10, 50);
</script> 
```

### Chiziqli gradientni chizish

![](<../../.gitbook/assets/image (44).png>)

```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");

// Create gradient
var grd = ctx.createLinearGradient(0, 0, 200, 0);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");

// Fill with gradient
ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</script> 
```

### Gradientli aylana chizish

![](<../../.gitbook/assets/image (214).png>)

```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");

// Create gradient
var grd = ctx.createRadialGradient(75, 50, 5, 90, 60, 100);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");

// Fill with gradient
ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</script> 
```



{% code title="Rasm chizish" %}
```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
var img = document.getElementById("scream");
ctx.drawImage(img, 10, 10);
</script> 
```
{% endcode %}
