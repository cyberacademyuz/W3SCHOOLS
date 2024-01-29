# DOM Elementlar

Ushbu sahifa HTML sahifasida HTML elementlarini qanday topish va ularga murojaat qilishni o'rgatadi.

### HTML elementlarini topish

Ko'pincha, JavaScript orqali HTML elementlarini manipulyatsiya qilishni xohlaysiz.

Buning uchun avval elementlarni topishingiz kerak. Buning bir necha yo'li bor:

* HTML elementlarini Id orqali topish
* HTML elementlarini teg nomi orqali topish
* HTML elementlarini class nomi orqali topish
* HTML elementlarini CSS selektorlari orqali topish
* HTML elementlarini HTML obyekt to'plamlari orqali topish

### HTML elementini Id orqali topish

DOM-da HTML elementini topishning eng oson yo'li elementning id-sidan foydalanish.

Ushbu misol `id="intro"` bilan elementni topadi:

```
const element = document.getElementById("intro");
```

Agar element topilsa, metod elementni obyekt sifatida qaytaradi.

Agar element topilmasa, element qiymati `null` bo'ladi.

### HTML elementlarini teg nomi orqali topish

Ushbu misol barcha `<p>` elementlarini topadi:

```
const element = document.getElementsByTagName("p");
```

Bu misol `id="main"` orqali elementni topadi va keyin "main"ga ega barcha \<p> elementlarini topadi:

```
const x = document.getElementById("main");
const y = x.getElementsByTagName("p");
```

### HTML elementlarini class nomi orqali topish

Agar bir xil class nomiga ega bo'lgan barcha elementlarni topmoqchi bo'lsangiz, `getElementsByClassName()`dan foydalaning.

Ushbu misol `class="intro"` yordamida barcha elementlar ro'yxatini qaytaradi.

```
const x = document.getElementsByClassName("intro");
```

### HTML elementlarini CSS selektorlari yordamida topish

Berilgan CSS selektoriga mos keladigan barcha elementlarni (id, class nomlari, turlari, atributlari, atribut qiymatlari va boshqalar) topmoqchi bo'lsangiz, `querySelectorAll()` dan foydalaning.

Ushbu misol `class="intro"` yordamida `<p>` elementlarining barcha ro'yxatini qaytaradi.

```
const x = document.querySelectorAll("p.intro");
```

### HTML elementlarini HTML obyektlar to'plamlari orqali topish

Ushbu misol formalar to'plamida `id="frm1"` orqali `form` elementini topadi va barcha element qiymatlarini ko'rsatadi:

```
const x = document.forms["frm1"];
let text = "";
for (let i = 0; i < x.length; i++) {
  text += x.elements[i].value + "<br>";
}
document.getElementById("demo").innerHTML = text;
```

Quyidagi HTML ob'ektlari (va ob'ektlar to'plami) ham mavjud:

* [document.anchors](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_anchors)
* [document.body](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_body)
* [document.documentElement](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_element)
* [document.embeds](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_embeds)
* [document.forms](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_forms)
* [document.head](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_head)
* [document.images](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_images)
* [document.links](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_links)
* [document.scripts](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_scripts)
* [document.title](https://www.w3schools.com/js/tryit.asp?filename=tryjs\_doc\_title)
