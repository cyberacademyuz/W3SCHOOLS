# Gorizontal navbar

### Gorizontal Navbar <a href="#gorizontal-navbar" id="gorizontal-navbar"></a>

<figure><img src="../../../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>

Gorizontal navbar yaratishning ikki xil yo'li bor: **Inline** hamda f**loat** ro'yxat elementlaridan foydalanish.

### Inline ro'yhat <a href="#inline-list" id="inline-list"></a>

Gorizontal navbar yaratish uchun `<li>` elementlarini inline qilish kerak. Buni avvalgi sahifadagi "standart" kodga qo'shimcha sifatida `<li>` elementlarini **inline** qilish kifoya:

```
li {
  display: inline;
}
```

Misolni tushuntirsak:

* `display: inline;` - `<li>` elementlar default tarzda block element bo'ladi. Shu sababdan bu xususiyatni qo'llagan holda ularni bir qatorga o'tkazamiz

### Float ro'yhati <a href="#float-list" id="float-list"></a>

Gorizontal navbar yaratishning yana bir usuli bu float dan foydalangan holda `<li>` elementlarni chapga yoki o'nga (odatda chapga) surish va havolalarni gorizontal tarzda joylashtirish:

```
li {
  float: left;
}

a {
  display: block;
  padding: 8px;
  background-color: #dddddd;
}
```

Misolni tushuntirsak:

* `float: left;` - Blok elementlarni bir birining yonida turishi uchun chap tomonga o'tkazadi
* `display: block;` - Padding (margin, width, height va hkz) berishga imkon yaratadi
* `padding: 8px;` - Har bir `<a>` elementlarining orasiga biroz padding beradi.
* `background-color: #dddddd;` - Har bir `<a>` elementining oraqafoniga kulrang orqafon beradi.

**Maslahar:** Agar butun navbarga rang bermoqchi bo'lsangiz `<a>` elementga emas `<ul>` elementifga background-color bering

```
ul {
  background-color: #dddddd;
} 
```

### Gorizontal navbarga misollar <a href="#gorizontal-navbar-misollari" id="gorizontal-navbar-misollari"></a>

Orqafoni to'q rangli bo'lgan navbar yarating va foydalanuvchi sichqoncha kursorini havolalar ustida harakatlantirganda ularning orqafon rangi o'zgarsin:

<figure><img src="../../../.gitbook/assets/image (815).png" alt=""><figcaption></figcaption></figure>

```
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* Change the link color to #111 (black) on hover */
li a:hover {
  background-color: #111;
} 
```

### Aktiv/Hozirgi havola <a href="#aktivhozirgi-link" id="aktivhozirgi-link"></a>

"active" classini qo'shing va foydalanuvchi qayerda ekanligini bildiruvchi havolaga orqafon rang bering:

<figure><img src="../../../.gitbook/assets/image (282).png" alt=""><figcaption></figcaption></figure>

```
.active {
  background-color: #04AA6D;
}
```

### O'ng tomonda joylashgan havollar <a href="#ong-tomonda-joylashgan-linklar" id="ong-tomonda-joylashgan-linklar"></a>

Roʻyxat elementlarini oʻngga surish orqali havolalarni oʻng tomonga joylashtiring:

<figure><img src="../../../.gitbook/assets/image (848).png" alt=""><figcaption></figcaption></figure>

```
 <ul>
  <li><a href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li style="float:right"><a class="active" href="#about">About</a></li>
</ul> 
```

## Chegarani ajratuvchilar

`<li>` elementlarga `border-right` xususiyatini berish orqali ajratib turuvchi chegara yarating:

<figure><img src="../../../.gitbook/assets/image (846).png" alt=""><figcaption></figcaption></figure>

```
 /* Add a gray right border to all list items, except the last item (last-child) */
li {
  border-right: 1px solid #bbb;
}

li:last-child {
  border-right: none;
} 
```

### fixed navigation bar <a href="#fixed-gorizontal-navbar" id="fixed-gorizontal-navbar"></a>

Foydalanuvchi sahifa bo'ylab tepa va pastga harakatlanganda ham navbar sahifaning yuqori yoki pastki qismida qolsin:

<figure><img src="../../../.gitbook/assets/image (634).png" alt=""><figcaption></figcaption></figure>

#### Tepa navbar <a href="#tepa-navbar" id="tepa-navbar"></a>

```
ul {
  position: fixed;
  top: 0;
  width: 100%;
}
```

#### Pastki Navbar <a href="#past-navbar" id="past-navbar"></a>

```
ul {
  position: fixed;
  bottom: 0;
  width: 100%;
}
```

{% hint style="warning" %}
**Eslatma:** Fixed navbarlar mobil qurilmalarda yaxshi ishlamasligi mumkin
{% endhint %}

### Kulrang gorizontal navbar <a href="#kulrang-gorizontal-navbar" id="kulrang-gorizontal-navbar"></a>

Kulrang gorizontal navbar kulrang border bilan:

Och kulrang hoshiyali va orqa foni kulrang gorizontal navbarga misol:&#x20;

<figure><img src="../../../.gitbook/assets/image (788).png" alt=""><figcaption></figcaption></figure>

```
 ul {
  border: 1px solid #e7e7e7;
  background-color: #f3f3f3;
}

li a {
  color: #666;
}
```

### Sticky navbar <a href="#yopishqoq-navbar" id="yopishqoq-navbar"></a>

Sticky navbar yasash uchun `<ul>` elementiga `position: sticky;` qiymatini bering

Sticky element skroll holatiga qarab **absolute** va **fixed** o'rtasida almashinadi. U viewportda ma'lum bir offset joylashuvi bajarilmaguncha relative joylashtiriladi - keyin u belgilangan joyiga kelganda "to'htaydi" (masalan: `position: fixed`).

<figure><img src="../../../.gitbook/assets/image (797).png" alt=""><figcaption></figcaption></figure>

```
ul {
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
}
```

{% hint style="warning" %}
**Eslatma**: Internet Explorer sticky joylashuvni qo'llab-quvvatlamaydi. Safari uchun -`webkit-` prefiksi talab qilinadi (yuqoridagi misolga qarang). Sticky joylashuvning ishlashi uchun top, right, bottom yoki leftdan birortasini belgilashingiz kerak.
{% endhint %}
