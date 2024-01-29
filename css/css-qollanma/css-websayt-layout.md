# CSS Websayt layout

### Website tartibi <a href="#website-tartibi" id="website-tartibi"></a>

Website lar asosan headerlar, menyular, kontent va footer larga bo'linadi.

<figure><img src="../../.gitbook/assets/image (822).png" alt=""><figcaption></figcaption></figure>

Tanlash uchun juda ko'p turli xil layout dizaynlari mavjud. Biroq, yuqoridagi struktura eng keng tarqalganlardan biri bo'lib, biz uni ushbu qo'llanmada batafsil ko'rib chiqamiz.

### Header <a href="#header" id="header"></a>

Header odatda Websaytning yuqori qismida (yoki yuqori navigatsiya menyusi ostida) joylashadi. U ko'pincha logotip yoki Web-site nomini o'z ichiga oladi:

```
.header {
  background-color: #F1F1F1;
  text-align: center;
  padding: 20px;
}
```

<figure><img src="../../.gitbook/assets/image (284).png" alt=""><figcaption></figcaption></figure>

### Navbar <a href="#navbar" id="navbar"></a>

Navbar, foydalanuvchiga website sahifalariga o'tishga yordam beradigan havolalar ro'yxatini o'z ichiga oladi:

```
/* The navbar container */
.topnav {
  overflow: hidden;
  background-color: #333;
}

/* Navbar links */
.topnav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* Links - change color on hover */
.topnav a:hover {
  background-color: #ddd;
  color: black;
}
```

<figure><img src="../../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure>

### Kontent <a href="#kontent" id="kontent"></a>

Ushbu bo'limdagi layout ko'pincha qanday foydalanuvchilarga qilinayotganligiga bog'liq. Eng keng tarqalgan layout, quyidagilardan biri (yoki ularni birlashtirish).

* **1 ta ustunli** (ko'pincha mobil qurilmalar uchun)
* **2 ta ustunli** (ko'pincha planshetlar uchun)
* **3 ta ustunli** (faqatgina kompyuterlar uchun)

<figure><img src="../../.gitbook/assets/image (769).png" alt=""><figcaption></figcaption></figure>

Endi 3 ta ustunli kontent yaratamiz va uni mobil qurilmalar uchun 1 ustunliga aylantiramiz

```
/* Create three equal columns that float next to each other */
.column {
  float: left;
  width: 33.33%;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Responsive layout - makes the three columns stack on top of each other instead of next to each other on smaller screens (600px wide or less) */
@media screen and (max-width: 600px) {
  .column {
    width: 100%;
  }
}
```

<figure><img src="../../.gitbook/assets/image (762).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Maslahat:** Agar ikki ustunli layout yaratmoqchi bo'lsangiz unda width ni 50% qiling, agar 4 ta ustunli layout bo'lsa unda 25%.

**Maslahat:** media query qanday ishlashini bilmoqchimisiz ? Unda <mark style="color:green;">CSS Media querielar</mark> bo'limimizga o'ting.

**Maslahat:** Ustun tartibini yaratishning zamonaviy usuli bu <mark style="color:green;">Flexbox</mark>-dan foydalanishdir. Biroq, u **Internet Explorer 10** va undan oldingi versiyalarida qo'llab-quvvatlanmaydi. Agar sizga IE6-10 uchun yordam kerak bo'lsa, floatlardan foydalaning.
{% endhint %}

### Teng bo'lmagan ustunlar <a href="#teng-bolmagan-ustunlar" id="teng-bolmagan-ustunlar"></a>

Asosiy kontent saytingizning eng katta va eng muhim qismidir.

Bu odatda ustunlarning teng bo'lmagan kengligida qilinadi, shuning uchun bo'sh joyning katta qismi asosiy tarkibga ajratiladi. Yon tarkib (agar mavjud bo'lsa) ko'pincha muqobil navigatsiya sifatida yoki asosiy tarkibga tegishli ma'lumotlarni ko'rsatish uchun ishlatiladi. Kengliklarni xohlaganingizcha o'zgartiring, faqat jami 100% gacha qo'shilishi kerakligini yodda tuting:

```
.column {
  float: left;
}

/* Left and right column */
.column.side {
  width: 25%;
}

/* Middle column */
.column.middle {
  width: 50%;
}

/* Responsive layout - makes the three columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column.side, .column.middle {
    width: 100%;
  }
}
```

<figure><img src="../../.gitbook/assets/image (809).png" alt=""><figcaption></figcaption></figure>

### Footer <a href="#footer" id="footer"></a>

Footer sahifaning eng pastki qismida joylashadi. U ko'pincha mualliflik huquqi va aloqa ma'lumotlari kabi ma'lumotlarni o'z ichiga oladi:

```
.footer {
  background-color: #F1F1F1;
  text-align: center;
  padding: 10px;
}
```

<figure><img src="../../.gitbook/assets/image (778).png" alt=""><figcaption></figcaption></figure>

### Responsive websayt tartibi <a href="#responsive-websayt-tartibi" id="responsive-websayt-tartibi"></a>

Yuqoridagi ba'zi CSS kodlaridan foydalanib, ekran kengligiga qarab ikki ustun va to'liq kenglikdagi ustunlar orasida o'zgarib turadigan responsive web-site layoutini tuzdik:

<figure><img src="../../.gitbook/assets/image (816).png" alt=""><figcaption></figcaption></figure>
