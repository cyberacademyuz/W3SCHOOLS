# Drag/Drop

HTMLda har qanday elementni ushlab surish va qo'yib yuborish mumkin.

### Misol

![](<../../.gitbook/assets/image (829).png>)

W3Schools suratini ikkinchi to'rtburchak ichiga surib o'tkazing.

### Drag va Drop

Drag va drop - obyektni "ushlab", uni boshqa joyga surib olib o'tkaningish uchun juda keng tarqalgan xususiyat hisoblanadi.

### Brauzerni qo'llab-quvvatlash

Jadvaldagi raqamlar drag va dropni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini bildiradi.

| API          | Chrom | Edge | Firefox |     |      |
| ------------ | ----- | ---- | ------- | --- | ---- |
| Drag va Drop | 4.0   | 9.0  | 3.5     | 6.0 | 12.0 |

### HTML Drag va Dropga misol

Quyidagi misol oddiy surib olib o'tish va qo'yib yuborishga bir misol:

```html
<!DOCTYPE HTML>
<html>
<head>
<script>
function allowDrop(ev) {
  ev.preventDefault();
}

function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<img id="drag1" src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="336" height="69">

</body>
</html>O'zingiz sinab ko'ring »
```

Bu qiyin tuyulishi mumkin, lekin keling surib olib o'tish hodisasining barcha turli qismlarini ko'rib chiqamiz.

### Elementni surib olib o'tiladigan qilib qo'ying

Avvalo: Elementni surib olib o'tiladigan qilish uchun `draggable` atributinining qiymatini true qiling:

```
<img draggable="true">
```

### Nimani surib olib o'tish kerak - ondragstart va setData()

Keyin, element surilganda nima bo'lishini belgilang.

Yuqoridagi misolda `ondragstart` atributi qaysi ma'lumotlarni surib olib o'tishni belgilaydigan drag(hodisa) funksiyasini chaqiradi.

`dataTransfer.setData()` metodi ma'lumotlar turini va surib olib o'tilgan ma'lumotlarning qiymatini belgilaydi:

```
function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}
```

Bu holatda, ma'lumotlar turi "string" va qiymat surib olib o'tiladigan elementning id-si ("drag1") hisoblanadi.

### Qayerga qo'yish kerak - ondragover

`ondragover` hodisasi surib olib o'tiladigan ma'lumotlarni qayerga qo'yish mumkinligini ifodalaydi.

Standart tarzda, ma'lumotlarni/elementlarni boshqa elementlarga olib o'tib bo'lmaydi. Qo'yishga ruxsat berish uchun elementning standart tarzda handle qilishini oldini olishimiz kerak.

Bu ondragover hodisasi uchun `event.preventDefault()` metodini chaqirish orqali amalga oshiriladi:

```
event.preventDefault()
```

### Qo'yib yuborish - ondrop

Surib olib kelingan ma'lumotlar qo'yib yuborilganda, drop hodisasi sodir bo'ladi.

Yuqoridagi misolda ondrop atributi drop(hodisa) funksiyasini chaqiradi:

```javascript
function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
```

Kodni tushuntirish:

* Brauzerda ma'lumotlarning standart tarzda ishlashini oldini olish uchun preventDefault() ni chaqiring (standart havola sifatida ochiladi)
* DataTransfer.getData() metodi orqali surib olib o'tilgan ma'lumotlarni oling. Bu metod `setData()` metodida bir xil turdagi har qanday ma'lumotlarni qaytaradi
* Olingan ma'lumotlar surib olib o'tilgan elementning id-isi hisoblanadi ("drag1")
* Olib o'tilgan elementni drop elementiga qo'shing
