# CSS Opacity

`opacity` xususiyati elementning shaffofligini belgilaydi.

### Shaffof rasm <a href="#shaffof-rasm" id="shaffof-rasm"></a>

`opacity` xususiyati 0.0 va 1.0 oralig'ida qiymat qabul qiladi. Berilgan qiymat qanchalik kichk bo’lsa shunchalik shaffof bo’ladi.

<figure><img src="../../.gitbook/assets/image (805).png" alt=""><figcaption></figcaption></figure>

```
img {
  opacity: 0.5;
}
```

### Shaffof hover effekti <a href="#transparent-hover-effekt" id="transparent-hover-effekt"></a>

`opacity` xususiyati ko’pincha sichqoncha kursorini element ustiga olib kelinganida shaffoflik darajasi bildirish uchun `:hover` pseudo classi bilan ishlatiladi.

<figure><img src="../../.gitbook/assets/image (798).png" alt=""><figcaption></figcaption></figure>

```
img {
  opacity: 0.5;
}

img:hover {
  opacity: 1.0;
}
```

### Misolni tushuntirish <a href="#misolni-tushuntirsak" id="misolni-tushuntirsak"></a>

Birinchi CSS bloki birinchi misoldagi 2-rasmga o’xshaydi. Unga qo'shimcha qilib, foydalnuvchi kursorni rasm ustiga olib kelganida nima bo’lishi kerakligini qo’shdik.

Kursorni rasm ustidan olinganida, u yana o’zining birinchi blokdagi holatiga qaytadi.

Shu misolni aksi:

<figure><img src="../../.gitbook/assets/image (818).png" alt=""><figcaption></figcaption></figure>

```
img:hover {
  opacity: 0.5;
}
```

### Shaffof box <a href="#transparent-box" id="transparent-box"></a>

`opacity` dan foydalanayotganda elementning barcha bola elementlariga ham bir xil qiymat o’tib ketib qoladi va undagi matn o’qishga noqulay bo’lishi mumkin.

<figure><img src="../../.gitbook/assets/image (850).png" alt=""><figcaption></figcaption></figure>

```
div {
  opacity: 0.3;
}
```

### Shaffoflik berish uchu RGBAdan foydalanish <a href="#rgba-yordamida-shaffoflik" id="rgba-yordamida-shaffoflik"></a>

Agar bola elementlariga ham bir xil qiymat o'tib ketishini xohlamasangiz, **RGBA**dan foydalansangiz bo’ladi. Quyidagi misolda faqat orqafondagi shaffoflik o’zgargan, matndagi shaffoflik emas.

<figure><img src="../../.gitbook/assets/image (808).png" alt=""><figcaption></figcaption></figure>

[CSS ranglar](https://www.w3schools.com/css/css\_colors.asp) bo’limimizdan RGB qiymatlaridan CSSda foydalanish mumkinligini o’rgangan edingiz. Bundan tashqari RGBda Alpha qiymatlarini ham ishlatish mumkin. Ya’ni shaffoflikni rang orqali belgilash.

RGBA qiymatlari: _rgba(red, green, blue, alpha)_ holatida ifodalanadi. Alpha parametri xuddi opacity kabi 0.0 va 1.0 oralig'idagi qiymatlarni qabul qiladi.

**Maslahat:** Bu haqida batafsil malumot olish uchun [CSS Ranglar](https://www.w3schools.com/css/css\_colors.asp) bo’limimizni o’qib chiqing.

```
div {
  background: rgba(76, 175, 80, 0.3) /* Green background with 30% opacity */
}
```

### Shaffof box ichidagi matn <a href="#transparent-box-ichidagi-matn" id="transparent-box-ichidagi-matn"></a>

<figure><img src="../../.gitbook/assets/image (790).png" alt=""><figcaption></figcaption></figure>

```
<html>
<head>
<style>
div.background {
  background: url(klematis.jpg) repeat;
  border: 2px solid black;
}

div.transbox {
  margin: 30px;
  background-color: #ffffff;
  border: 1px solid black;
  opacity: 0.6;
}

div.transbox p {
  margin: 5%;
  font-weight: bold;
  color: #000000;
}
</style>
</head>
<body>

<div class="background">
  <div class="transbox">
    <p>This is some text that is placed in the transparent box.</p>
  </div>
</div>

</body>
</html>
```

### Misolni tushuntirish <a href="#misolni-tushuntirsak-2" id="misolni-tushuntirsak-2"></a>

Eng birinchi, orqa fon rasmli va chegarali \<div> elementini (class="background") yaratamiz.

Keyin birinchi \<div> elementining ichida boshqa bir \<div> (class=“transbox”) yaratdik.

\<div class="transbox"> orqa fon ranggi va chegaraga ga - divning o'zi shaffof

Shaffof \<div> ichidagi \<p> elementining ichiga ba'zi matnlar qo'shdik.
