# CSS Dropdownlar

CSS orqali hoverli dropdown yasash.

## Demo: Dropdownga misollar <a href="#demo-css-dropdown" id="demo-css-dropdown"></a>

Quyidagi misollar ustiga sichqoncha kursorini olib boring:

<figure><img src="../../.gitbook/assets/image (635).png" alt=""><figcaption></figcaption></figure>

### Oddiy dropdown <a href="#oddiy-dropdown" id="oddiy-dropdown"></a>

Foydalanuvchi kursorni element ustiga olib borganida paydo bo'ladigan dropdown yasash:

```
<style>
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  padding: 12px 16px;
  z-index: 1;
}

.dropdown:hover .dropdown-content {
  display: block;
}
</style>

<div class="dropdown">
  <span>Mouse over me</span>
  <div class="dropdown-content">
    <p>Hello World!</p>
  </div>
</div> 
```

#### Misolni tushuntrish <a href="#misolni-tushuntrisak" id="misolni-tushuntrisak"></a>

**HTML)** Dropdownni ochish uchun `<span>` yoki `<button>` kabi har qanday elementdan foydalaning.

Dropdown tarkibini yaratish uchun konteyner elementdan (masalan, `<div>`) foydalaning va ichiga xohlagan narsangizni qo'shing.

CSS orqali dropdown tarkibni to'g'ri joylashtirish uchun elementlarni o'rab turuvchi `<div>` elementini o'rang.

**CSS)** Dropdown tarkibini `position:absolute` yordamida dropdown tugmasining tagiga joylashtirimoqchi bo'lsak `.dropdown` classida `position:relative` dan foydalaniladi.

`.dropdown-content` dropdown ning asosiy kontentini o'zida saqlaydi. Standart tarzda u ko'rinmas holatda bo'ladi va hover qilinganda ko'rinadi. Uning `min-width` qiymati 160px qilinganiga e'tibor bering. Uni bemalol o'zgartirishingiz mumkin. **Maslahat:** Agar dropdown kontentining kengligini dropdown buttonning o'lchami bilan bir xil qilmoqchi bo'lsangiz `width` qiymatini 100% qiling (va kichik ekranlarda scroll qilinishi uchun `overflow: auto` qiling).&#x20;

Dropddown menyu card-ga o'xshashi uchu `border` xususiyatining o'rniga `box-shadow` dan foydalandik.

`:hover` selektori foydalanuvchi sichqoncha kursorini dropdown tugmasining ustiga olib borganida dropdwon menyuni ko'rsatish uchun ishlatiladi.

## Dropdown Menu <a href="#dropdown-menu" id="dropdown-menu"></a>

Foydalanuvchiga ro'yxatdagi variantni tanlash imkonini beruvchi dropdown menyu yaratish:

![](<../../.gitbook/assets/image (817).png>)

Bu misol ham avvalgisiga o'xshaydi, faqat dropdown menyuga havolalar qo'shdik va havolalarni dropdown tugmasiga moslashtirish uchun still berdik:

```
<style>
/* Style The Dropdown Button */
.dropbtn {
  background-color: #4CAF50;
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

/* The container <div> - needed to position the dropdown content */
.dropdown {
  position: relative;
  display: inline-block;
}

/* Dropdown Content (Hidden by Default) */
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

/* Links inside the dropdown */
.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

/* Change color of dropdown links on hover */
.dropdown-content a:hover {background-color: #f1f1f1}

/* Show the dropdown menu on hover */
.dropdown:hover .dropdown-content {
  display: block;
}

/* Change the background color of the dropdown button when the dropdown content is shown */
.dropdown:hover .dropbtn {
  background-color: #3e8e41;
}
</style>

<div class="dropdown">
  <button class="dropbtn">Dropdown</button>
  <div class="dropdown-content">
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
    <a href="#">Link 3</a>
  </div>
</div> 
```

### O'ng tomonga joylashtirilgan dropdown <a href="#ong-tomonga-joylashtirilgan-dropdown" id="ong-tomonga-joylashtirilgan-dropdown"></a>

![](<../../.gitbook/assets/image (840).png>)

Agar dropdown menyuni o'ngdan chapga joylashtirmoqchi bo'lsangiz `right:0` qiymatini berishingiz kerak

Agar dropdown menyu chapdan o'ngga emas, o'ngdan chapga joylashishini hohlasangiz, `right:0;` qo'shing

```
.dropdown-content {
  right: 0;
}
```
