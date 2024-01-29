# Vertical navbar

### Vertikal navbar <a href="#vertical-navigation-bar" id="vertical-navigation-bar"></a>

<figure><img src="../../../.gitbook/assets/image (531).png" alt=""><figcaption></figcaption></figure>

Vertikal navbar yasash uchun, oldingi sahifadagi kodga qo'shimcha sifatida ro'yxat ichidagi \<a> elementlariga still berishingiz mumkin:

```
li a {
  display: block;
  width: 60px;
}
```

Misolni tushuntirsak:

* `display: block;` - Havolalarni blok element sifatida ko'rsatish (nafaqat matnni balki) havola egallab turgan butin maydonni bosishga imkon beradi va bu orqali bemalol ularga margin, width, padding va hokazolarni bera olamiz.
* `width: 60px` - Aslida blok elementlar standart tarzda butun maydonni egallab oladi, ammo biz uning kengligini 60px qilib belgiladik.

Bundan tashqari `<a>` elementiga width bermasdan, `<ul>` elementining o'ziga width berib qo'ysangiz ham bo'ladi chunki ular blok elementi sifatida ko'rsatilganda mavjud bo'lgan to'liq widthni egallab turadi. Bu ham avvalgi misolimiz bilan bir xil natija qaytaradi.

```
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 60px;
}

li a {
  display: block;
}
```

### Vertikal navbarga misollar <a href="#vertical-navigation-bar-misollari" id="vertical-navigation-bar-misollari"></a>

Orqafon ranggi kulrang bo'lgan oddiy vertikal navibar yarating va foydalanuvchi sichqonchani ularning ustiga olib borganida havolalarning fon rangini o'zgartiring:

![](<../../../.gitbook/assets/image (838).png>)

```
 ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 200px;
  background-color: #f1f1f1;
}

li a {
  display: block;
  color: #000;
  padding: 8px 16px;
  text-decoration: none;
}

/* Change the link color on hover */
li a:hover {
  background-color: #555;
  color: white;
}
```

### Aktiv/Joriy havola <a href="#aktivhozirgi-link" id="aktivhozirgi-link"></a>

Activ classini qo'shish orqali foydalanuvchi qaysi sahifada ekanligini ko'rsatishga yordam bering:

![](<../../../.gitbook/assets/image (421).png>)

```
.active {
  background-color: #04AA6D;
  color: white;
}
```

### Havolalarni o'rtaga joylashtiring va chegara qo'shing <a href="#linklarni-ortaga-joylashtiring-va-border-qoshing" id="linklarni-ortaga-joylashtiring-va-border-qoshing"></a>

Havolalarni o'rtaga joylashtirish uchun `<a>` yoki `<ul>` elementiga uchun `text-align: center;` xususiyatini bering.

Navbar atrofiga chegara qo'shish uchun `<ul>` elementiga `border` xususiyatini qo'shing. Agar  navbar ichida ham chegara qo'shmoqchi bo'lsangiz, `<li>` elementining ohirigisidan boshqalariga  `border` xususiyatini bering.&#x20;

![](<../../../.gitbook/assets/image (826).png>)

```
ul {
  border: 1px solid #555;
}

li {
  text-align: center;
  border-bottom: 1px solid #555;
}

li:last-child {
  border-bottom: none;
}
```

### Balandligi to'liq ekranni egallab qotib turuvchi vertikal navbar <a href="#butun-ekranni-egallagan-fixed-vertikal-navbar" id="butun-ekranni-egallagan-fixed-vertikal-navbar"></a>

Yon tomon tomonda balandligi to'liq ekranni egallovchi "sticky" navbar yarating:

<figure><img src="../../../.gitbook/assets/image (787).png" alt=""><figcaption></figcaption></figure>

```
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 25%;
  background-color: #f1f1f1;
  height: 100%; /* Butun ekranni egallasin */
  position: fixed; /* Skroll qilinsa ham yopishib tursin */
  overflow: auto; /* Sidenav da ko'p narsa bo'lib ketsa ham skroll yoniq tursin */
}
```

**Eslatma:** Ushbu misol mobil qurilmalarda ishlamasligi mumkin
