# RWD Grid View

### Grid-View nima ?

Ko'p veb-sahifalar grid ko'rinishiga asoslangan, ya'ni sahifa ustunlarga bo'linadi:

<figure><img src="../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure>

Grid ko'rinishidan foydalanish veb-sahifalarni loyihalashda juda foydali. Bu elementlarni sahifaga joylashtirishni osonlashtiradi.

<figure><img src="../.gitbook/assets/image (413).png" alt=""><figcaption></figcaption></figure>

Moslashuvchan gridda ko'pincha 12 ta ustun bo'ladi va umumiy kengligi 100% ni tashkil qiladi va brauzer oynasining o'lchamini o'zgartirganda kichrayadi va kengayadi.

### Responsive Grid-view yaratish

Keling, Responsive grid-view yaratishni boshlaymiz.

Eng avval, barcha HTML elementlarida `box-sizing` xususiyati `border-box` qilinganiga ishonch hosil qiling. Bu padding va borderni, elementlarning umumiy kengligi va balandligiga kiritilganligiga ishonch hosil qiladi.

CSS-ga quyidagi kodni qo'shing:

```
* {
  box-sizing: border-box;
}
```

`box-sizing` xususiyati haqida [<mark style="color:green;">CSS Box-sizing</mark>](../css/yuqori-darajali-css/css-box-sizing.md) bo'limida batafsil o'qing.

Quyidagi misolda ikki ustunli oddiy moslashuvchan veb-sahifa ko'rsatilgan:

<figure><img src="../.gitbook/assets/image (394).png" alt=""><figcaption></figcaption></figure>

```
.menu {
  width: 25%;
  float: left;
}
.main {
  width: 75%;
  float: left;
}
```

Agar veb-sahifa faqat ikkita ustundan iborat bo'lsa, yaxshi.

Lekin, veb-sahifani ko'proq boshqarish uchun 12 ustunli moslashuvchan **grid-view**dan foydalanmoqchimiz.

Avval bitta ustun uchun uning foizini hisoblashimiz kerak: 100% / 12 ustun = 8,33%.

Keyin 12 ta ustunning har biriga `class="col-"` classini va bo'lim qancha ustundan iborat bo'lishi kerakligini belgilaydigan raqamni kiritishimiz kerak:

{% code title="CSS:" %}
```
.col-1 {width: 8.33%;}
.col-2 {width: 16.66%;}
.col-3 {width: 25%;}
.col-4 {width: 33.33%;}
.col-5 {width: 41.66%;}
.col-6 {width: 50%;}
.col-7 {width: 58.33%;}
.col-8 {width: 66.66%;}
.col-9 {width: 75%;}
.col-10 {width: 83.33%;}
.col-11 {width: 91.66%;}
.col-12 {width: 100%;}
```
{% endcode %}

&#x20;Ushbu ustunlarning barchasi chap tomonga float bo'ladi, va 15px paddingga ega bo'lishi kerak:

{% code title="CSS:" %}
```
[class*="col-"] {
  float: left;
  padding: 15px;
  border: 1px solid red;
}
```
{% endcode %}

Har bir qator (row)  `<div>` bilan o'ralgan bo'lishi kerak. Qator ichidagi ustunlar soni har doim 12 tagacha qo'shilishi kerak:

{% code title="HTML:" %}
```
<div class="row">
  <div class="col-3">...</div> <!-- 25% -->
  <div class="col-9">...</div> <!-- 75% -->
</div>
```
{% endcode %}

Qator ichidagi ustunlar hammasi chapga float bo'ladi va shu sababli sahifa oqimidan chiqariladi va boshqa elementlar ustunlar mavjud emasdek joylashtiriladi. Buning oldini olish uchun oqimni tozalaydigan still qo'shamiz:

{% code title="CSS:" %}
```
.row::after {
  content: "";
  clear: both;
  display: table;
}
```
{% endcode %}

Bundan tashqari, uni yanada yaxshiroq qilish uchun ba'zi stillar va ranglar qo'shamiz:

```
html {
  font-family: "Lucida Sans", sans-serif;
}

.header {
  background-color: #9933cc;
  color: #ffffff;
  padding: 15px;
}

.menu ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.menu li {
  padding: 8px;
  margin-bottom: 7px;
  background-color :#33b5e5;
  color: #ffffff;
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
}

.menu li:hover {
  background-color: #0099cc;
}
```

{% hint style="warning" %}
Brauzer oynasining o'lchamining kengligini juda kichkina qilganingizda, misolda ko'rsatilgan veb-sahifa yaxshi ko'rinmasligiga **e'tibor bering.** Keyingi bo'limda buni qanday to'girlashni o'rganib olasiz.
{% endhint %}
