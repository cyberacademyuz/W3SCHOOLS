# CSS Align

<figure><img src="../../.gitbook/assets/image (511).png" alt=""><figcaption></figcaption></figure>

## Elementlarni markazga to'g'irlash

Block elementlarni (\<div> kabi) gorizontal tarzda o'rtaga joylashtirish uchun `margin: auto;` dan foydalaning.

Elementga width qiymatini (kengligini) berish, o'zi turgan konteyneridagi bo'sh joylarini egallab olish uchun cho'zilib ketishini oldini oladi.

Shunda element berilgan kenglikni egallaydi va qolgan bo'sh joylar ikki margin o'rtasida teng taqsimlanadi.

<figure><img src="../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

```
.center {
  margin: auto;
  width: 50%;
  border: 3px solid green;
  padding: 10px;
}
```

**Eslatma:** width qiymati berilmagan (yoki uning qiymati 100%) bo'lsa elementni o'rtaga olib kelish tasir qilmaydi.

### Matnni o'rtaga joylashtirish <a href="#matnni-ortaga-joylashtirish" id="matnni-ortaga-joylashtirish"></a>

Matnni o'rtaga joylashtirish uchun shunchaki `text-align: center;` dan foydalaning:

<figure><img src="../../.gitbook/assets/image (480).png" alt=""><figcaption></figcaption></figure>

```
.center {
  text-align: center;
  border: 3px solid green;
}
```

**Maslahat:** Matn qanday joylashtirilishi haqida ko'proq ma'lumot olish uchun [<mark style="color:green;">CSS Matn</mark> ](css-matn/)bo'limimizga o'ting.

### Rasmni o'rtaga joylashtirish <a href="#rasmni-ortaga-joylashtirish" id="rasmni-ortaga-joylashtirish"></a>

Rasmni o'rtaga joylashtirish uchun chap va o'ng tomon marginlarni `auto` qilib, rasmning o'zini `block` element qiling.

<figure><img src="../../.gitbook/assets/paris (2).jpg" alt=""><figcaption></figcaption></figure>

```
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 40%;
}
```

### Position dan foydalanib o'ng va chapga joylashtirish <a href="#position-dan-foydalanib-ong-va-chapga-joylashtirish" id="position-dan-foydalanib-ong-va-chapga-joylashtirish"></a>

Elementlarni joylashtirishning yana bir usuli`position: absolute;` dan foydalanish:

&#x20;                                                                                                       ![](<../../.gitbook/assets/image (514).png>)

```
.right {
  position: absolute;
  right: 0px;
  width: 300px;
  border: 3px solid #73AD21;
  padding: 10px;
}
```

**Eslatma:** Absalyut tarzda joylashtirilgan elementlar normal oqimdan chiqib elementlar ustiga chiqib qolishi mumkin.

### Float dan foydalanib elementni chap va o'ngga joylashtirish <a href="#float-ni-ishlatgan-holda-elementni-chap-va-ongga-joylashtirish" id="float-ni-ishlatgan-holda-elementni-chap-va-ongga-joylashtirish"></a>

Elementlarni joylashtirishdagi yana bir metod - `float` xususiyatidan foydalanish:

```
 .right {
  float: right;
  width: 300px;
  border: 3px solid #73AD21;
  padding: 10px;
}
```

### Clearfix hack <a href="#clearfix-hack" id="clearfix-hack"></a>

{% hint style="warning" %}
**Note:** Agar element uni o'rab turgan elementdan balandroq va `float` berilgan bo'lsa  u konteynerdan tashqariga "chiqib ketadi". Keyin bu muammoni hal qilish uchun **clearfix**ni qo'shishimiz mumkin:
{% endhint %}

<figure><img src="../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

Keyin bu muammoni hal qilish uchun o'rab turuvchi elementga clearfix qo'shishimiz mumkin:

```
.clearfix::after {
  content: "";
  clear: both;
  display: table;
} 
```

### Vertikal tarzda padding orqali o'rtaga joylashtirish <a href="#vertikal-holatda-padding-orqali-ortaga-joylashtirish" id="vertikal-holatda-padding-orqali-ortaga-joylashtirish"></a>

CSS da elementni vertikal tarzda o'rtaga joylashtirishni ko'p yo'llari bor. Eng sodda usullardan biri bu `padding` dan foydalanish:

<figure><img src="../../.gitbook/assets/image (288).png" alt=""><figcaption></figcaption></figure>

```
 .center {
  padding: 70px 0;
  border: 3px solid green;
}
```

Agar, ham vertikal ham gorizontal tarzda o'rtaga joylashtirmoqchi bo'lsangiz, unda `padding` va `text-align: center` dan foydalaning:

<figure><img src="../../.gitbook/assets/image (759).png" alt=""><figcaption></figcaption></figure>

```
.center {
  padding: 70px 0;
  border: 3px solid green;
  text-align: center;
}
```

<figure><img src="../../.gitbook/assets/image (761).png" alt=""><figcaption></figcaption></figure>

### Line-height orqali vertikal tarzda o'rtaga joylashtirish <a href="#line-height-orqali-vertikal-holatda-ortaga-joylashtirish" id="line-height-orqali-vertikal-holatda-ortaga-joylashtirish"></a>

`line-height` xususiyatidan ayyorona foydalanishning yana bir yo'li bu `height` bilan bir xil qiymat berib vertikal tarzda elementni o'rtaga joylashtirish

```
 .center {
  line-height: 200px;
  height: 200px;
  border: 3px solid green;
  text-align: center;
}

/* If the text has multiple lines, add the following: */
.center p {
  line-height: 1.5;
  display: inline-block;
  vertical-align: middle;
}
```

### Position va transform yordamida vertikal tarzda o'rtaga joylashtirish <a href="#position-va-transform-yordamida-vertikal-holatda-ortaga-joylashtirish" id="position-va-transform-yordamida-vertikal-holatda-ortaga-joylashtirish"></a>

Agar `padding` va `line-height` to'g'ri kelmasa, unda `position` va `transform` dan foydalanib ko'ring:

<figure><img src="../../.gitbook/assets/image (807).png" alt=""><figcaption></figcaption></figure>

```
 .center {
  height: 200px;
  position: relative;
  border: 3px solid green;
}

.center p {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

**Maslahat:** Transform xususiyati haqida <mark style="color:green;">2D Transform</mark> bo'limida ko'proq ma'lumotga ega bo'lasiz

### Flexbox yordamida vertikal tarzda o'rtaga joylashtirish <a href="#flexbox-yordamida-vertikal-holatda-ortaga-joylashtirish" id="flexbox-yordamida-vertikal-holatda-ortaga-joylashtirish"></a>

flexbox dan elementlarni joylashuvini to'g'rilash uchun ham foydalansangiz mumkin. Yana bir narsani ta'kidlash lozimki, flexbox IE10 va undan eski versiyalarda ishlamaydi:

<figure><img src="../../.gitbook/assets/image (845).png" alt=""><figcaption></figcaption></figure>

```
.center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
  border: 3px solid green;
}
```

**Maslahat:** Flexbox haqida <mark style="color:green;">Flexbox</mark> bo'limida ko'proq ma'lumotga ega bo'lasiz
