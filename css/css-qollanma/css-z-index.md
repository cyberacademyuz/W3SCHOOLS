# CSS Z-index

`z-index` xususiyati elementning usma ustlik tartibini belgilaydi.

### Z-index xususiyati <a href="#z-index-xususiyati" id="z-index-xususiyati"></a>

Elementlar joylashtirilganda, ular boshqa elementlarning ustiga chiqishi mumkin.

`z-index` xususiyati elementning usma ustlik tartibini belgilaydi (qaysi element boshqalarning ustiga yoki tagiga joylashtirilishi kerak).

Element manfit yoki musbat qiymat orqali ustma ustlik tartibiga ega bo'lishi mumkin:

![](<../../.gitbook/assets/image (392).png>)

```
img {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: -1;
}
```

**Eslatma:** `z-index` faqatgina `position` qiymatiga ega elementlar (position: absolute, position: relative, position: fixed, or position: sticky)da va `flex` elementlarda (`display: flex` elementlarining to'g'ridan to'g'ri child elementi bo'lgan elementlar)da ishlaydi.

### z-indexga yana bir misoli <a href="#yana-bir-z-index-misoli" id="yana-bir-z-index-misoli"></a>

{% code title="Bu misolda kattaroq tartib qiymaytiga ega element doimo kichik tartibga qiymatiga ega elementning tepasida turishini ko'ramiz:" %}
```
<html>
<head>
<style>
.container {
  position: relative;
}

.black-box {
  position: relative;
  z-index: 1;
  border: 2px solid black;
  height: 100px;
  margin: 30px;
}

.gray-box {
  position: absolute;
  z-index: 3;
  background: lightgray;
  height: 60px;
  width: 70%;
  left: 50px;
  top: 50px;
}

.green-box {
  position: absolute;
  z-index: 2;
  background: lightgreen;
  width: 35%;
  left: 270px;
  top: -15px;
  height: 100px;
}
</style>
</head>
<body>

<div class="container">
  <div class="black-box">Black box</div>
  <div class="gray-box">Gray box</div>
  <div class="green-box">Green box</div>
</div>

</body>
</html>
```
{% endcode %}

### z-indexsiz <a href="#z-indexsiz" id="z-indexsiz"></a>

Agar ikkita joylashtirilgan element `z-index` qiymati berilmagan holda bir-birining ustiga chiqib qolsa, HTML kodida oxirgi yaratilgan element tepada ko'rsatiladi.&#x20;

Tepadagi misol bilan bir xil, ammo bu yerda `z-index`dan foydalanilmagan:

```
<html>
<head>
<style>
.container {
  position: relative;
}

.black-box {
  position: relative;
  border: 2px solid black;
  height: 100px;
  margin: 30px;
}

.gray-box {
  position: absolute;
  background: lightgray;
  height: 60px;
  width: 70%;
  left: 50px;
  top: 50px;
}

.green-box {
  position: absolute;
  background: lightgreen;
  width: 35%;
  left: 270px;
  top: -15px;
  height: 100px;
}
</style>
</head>
<body>

<div class="container">
  <div class="black-box">Black box</div>
  <div class="gray-box">Gray box</div>
  <div class="green-box">Green box</div>
</div>

</body>
</html>
```

### CSSning barcha z-index xususiyatlari <a href="#barcha-css-z-index-xususiyatlari" id="barcha-css-z-index-xususiyatlari"></a>

| Xususiyat                                                        | Ta'rif                            |
| ---------------------------------------------------------------- | --------------------------------- |
| [z-index](https://www.w3schools.com/cssref/pr\_pos\_z-index.asp) | Element stek tartibini belgilaydi |
