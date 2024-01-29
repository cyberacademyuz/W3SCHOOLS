# CSS Position

`position` xususiyati element uchun joylashuvni anilash usulini belgilaydi (static, relative, fixed, absolute yoki sticky).

### Position xususiyati <a href="#position-xususiyati" id="position-xususiyati"></a>

`position` xususiyati element uchun joylashuvni anilash usulini belgilaydi

Unda 5 xil joylashuv qiymatlari bor:

* <mark style="color:red;">`static`</mark>
* <mark style="color:red;">`relative`</mark>
* <mark style="color:red;">`fixed`</mark>
* <mark style="color:red;">`absolute`</mark>
* <mark style="color:red;">`sticky`</mark>

Keyin elementlar **top**, **bottom**, **left**, va **right** xususiyatlardan foydalangan holda joylashtiriladi. Biroq bu xususiyatlar, birinchi bo'lib `position` xususiyati berilmaguncha, ishlamaydi. position qiymatiga ko'ra har xil ishlaydi.

### position: static; <a href="#position-static" id="position-static"></a>

HTML elementlari standart tarzda static joylashtirilgan bo'ladi.

Static joylashgan elementlarga top, bottom, left va right xususiyatlar ta'sir qilmaydi.

`position:static;`ga ega bo'lgan element hech qanday maxsus joylashuvga ega bo'lmaydi. U har doim sahifaning normal oqimiga qarab joylashadi.

<figure><img src="../../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure>

Foydalanilgan CSS kod:

```
div.static {
  position: static;
  border: 3px solid #73AD21;
}
```

### position: relative; <a href="#position-relative" id="position-relative"></a>

`position: relative;`ga ega bo'lgan element normal joylashuvga nisbatan joylashtiriladi

Nisbatan joylashtirilgan elementning **top**, **right**, **bottom** va **left** xususiyatlarini berish uning o'z joyidan uzoqroqga joylashishiga olib keladi. Boshqa kontentlar element qoldirgan boʻsh joyga moslashtirilmaydi.

<figure><img src="../../.gitbook/assets/image (484).png" alt=""><figcaption></figcaption></figure>

```
div.relative {
  position: relative;
  left: 30px;
  border: 3px solid #73AD21;
}
```

### position: fixed; <a href="#position-fixed" id="position-fixed"></a>

`position: fixed;` bo'lgan element **viewport**ga nisbatan joylashadi, ya'ni sahifa scroll qilinganda ham u doimo bir joyda qoladi. Top, right, bottom va left xususiyatlari elementni joylashtirish uchun ishlatiladi.

fixed qilingan element hech qanday bo'sh joy qoldirmaydi va normal joylashadi.

Sahifaning pastki o'ng burchagidagi fixed qilingan elementga e'tibor bering. Mana bu uning CSS kodi:

```
div.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 300px;
  border: 3px solid #73AD21;
}
```

### position: absolute; <a href="#position-absolute" id="position-absolute"></a>

`position: absolute;`ga ega element eng yaqin joylashgan parentga nisbatan joylashtiriladi (ya'ni viewportga nisbatan joylashish o'rniga, fixed kabi).

Biroq; agar absolute joylashtirilgan elementning ota elementlari bo'lmasa, u HTMLning `<body>` elementidan foydalanadi va sahifa scroll bo'lganida birga harakatlanadi.

**Eslatma:** Absolute joylashtirilgan elementlar oddiy oqimdan olib tashlanadi va elementlarning ustiga chiqib qoladi.

![](<../../.gitbook/assets/image (481).png>)

```
div.relative {
  position: relative;
  width: 400px;
  height: 200px;
  border: 3px solid #73AD21;
}

div.absolute {
  position: absolute;
  top: 80px;
  right: 0;
  width: 200px;
  height: 100px;
  border: 3px solid #73AD21;
}
```

### position: sticky; <a href="#position-sticky" id="position-sticky"></a>

`position: sticky;` ga ega element foydalanuvchining scroll joylashuviga asoslanib joylashadi.

Sticky element scroll holatiga qarab `relative` va `fixed` o'rtasida almashadi. U viewportda ma'lum bir ofset pozitsiyasi bajarilgunga qadar nisbiy joylashadi - keyin esa kelgan joyiga "to'xtaydi" ((`position:fixed` kabi).

<figure><img src="../../.gitbook/assets/image (471).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma:** Internet Explorer sticky elementlarni qo'llab-quvvatlamaydi. Safari uchun esa `-webkit-` prefiksi talab qilinadi. Sticky joylashuvning ishlashi uchun top, right, bottom yoki leftda kamida bittasini berish kerak.
{% endhint %}

Ushbu misolda sticky element (top:0) tepaga joylashadi.

```
div.sticky {
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
  background-color: green;
  border: 2px solid #4CAF50;
}
```

### Matnning rasmda joylashuvi <a href="#barcha-css-position-qiymatlari" id="barcha-css-position-qiymatlari"></a>

Matnni rasm ustiga qanday joylashtirish mumkin:

<figure><img src="../../.gitbook/assets/image (498).png" alt=""><figcaption></figcaption></figure>

## Ko'proq misollar <a href="#barcha-css-position-qiymatlari" id="barcha-css-position-qiymatlari"></a>



### Barcha CSS Position qiymatlari <a href="#barcha-css-position-qiymatlari" id="barcha-css-position-qiymatlari"></a>

| Xususiyat                                                            | Description                               |
| -------------------------------------------------------------------- | ----------------------------------------- |
| [bottom](https://www.w3schools.com/cssref/pr\_pos\_bottom.asp)       | elementni pastki tomonga joylashtiradi    |
| [clip](https://www.w3schools.com/cssref/pr\_pos\_clip.asp)           | Mutlaqo joylashtirilgan elementni qirqadi |
| [left](https://www.w3schools.com/cssref/pr\_pos\_left.asp)           | Elementni chapki tomonga joylashtiradi    |
| [position](https://www.w3schools.com/cssref/pr\_class\_position.asp) | Joylashuvni qanday bo'lishini belgilaydi  |
| [right](https://www.w3schools.com/cssref/pr\_pos\_right.asp)         | Elementni o'ng tomonga joylashtiradi      |
| [top](https://www.w3schools.com/cssref/pr\_pos\_top.asp)             | Elementni tepaga joylashtiradi            |
