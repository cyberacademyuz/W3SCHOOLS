# CSS Rasm spritlari

### Rasm Sprite lar <a href="#rasm-sprite-lar" id="rasm-sprite-lar"></a>

Rasm spritelari bu bitta rasmda joylashgan ko'plab rasmlar to'plami hisoblanadi.

Web sahifada ko'p rasmdan foydalanish uni yuklanishini sekinlashtirishi mumkin.

Rasm spritlaridan foydalanish server so'rovlarini kamaytiradi va trafikni tejaydi.

### Rasm Sprite lar - Oddiy misol <a href="#rasm-sprite-lar-oddiy-misol" id="rasm-sprite-lar-oddiy-misol"></a>

Uchta alohida rasmlardan foydalanish o'rniga, ushbu bitta rasmdan foydalanamiz ("img\_navsprites.gif"):

![](<../../.gitbook/assets/image (784).png>)

CSS yordamida, rasmning kerakli qismini tanlab ekranda ko'rsatishimiz mumkin:

Quyidagi misolda "_img\_navsprites.gif_" rasmini kesib to'g'rilaymiz:

```
#home {
  width: 46px;
  height: 44px;
  background: url(img_navsprites.gif) 0 0;
}
```

**Misolni tushuntirish:**

* `<img id="home" src="img_trans.gif">` - Faqatgina kichik shaffof rasmni belgilaydi, chunki `src` atributi bo'sh bo'lmasligi kerak. Ko'rsatilgan rasm esa CSS-da berilgan background rasm hisoblanadi.
* `width: 46px; height: 44px;` - Rasmning biz foydalanmoqchi bo'lgan qismini belgilaydi
* `background: url(img_navsprites.gif) 0 0` - orqafon rasmini va uning joylashishini belgilaydi (chap 0px, tepa 0px)

Bu rasm spritelaridan foydalanishning eng oddiy usuli, endi uni havolalar va hover effektlari bilan ishlatamiz.

### Rasm sprite lari - Navigatsiya ro'yhatini yaratish <a href="#rasm-sprite-lar-navbar-uchun-list" id="rasm-sprite-lar-navbar-uchun-list"></a>

Rasm spritelari orqali navigatsiya uchun ro'yhat yaratmoqchimiz.

Buning uchun HTML ro'yhatidan foydalanamiz chunki u havola bo'lishi mumkin va background rasmni ham qo'llab-quvvatlaydi:

```
#navlist {
  position: relative;
}

#navlist li {
  margin: 0;
  padding: 0;
  list-style: none;
  position: absolute;
  top: 0;
}

#navlist li, #navlist a {
  height: 44px;
  display: block;
}

#home {
  left: 0px;
  width: 46px;
  background: url('img_navsprites.gif') 0 0;
}

#prev {
  left: 63px;
  width: 43px;
  background: url('img_navsprites.gif') -47px 0;
}

#next {
  left: 129px;
  width: 43px;
  background: url('img_navsprites.gif') -91px 0;
}
```

**Misolni tushuntirish:**

* <mark style="color:red;">`#navlist {position:relative;}`</mark> - uning ichida position absolute dan foydalanish uchun position relative qilindi.&#x20;
* <mark style="color:red;">`#navlist li {margin:0;padding:0;list-style:none;position:absolute;top:0;}`</mark> - ro'yhatdagi belgilar olib tashlandi, margin va padding qiymatlari 0 qilindi, va barcha `<li>` elementlari position absolute ga aylantirildi
* <mark style="color:red;">`#navlist li, #navlist a {height:44px;display:block;}`</mark> - barcha rasmlarning balandligi 44px qilindi

Endi har bir kichik qismlarga o'tsak:

* <mark style="color:red;">`#home {left:0px;width:46px;}`</mark> - Rasm to'liq chap tomonga o'tkazildi va kengligi 46px qilindi
* <mark style="color:red;">`#home {background:url(img_navsprites.gif) 0 0;}`</mark> - background rasmini ifodalaydi va uning joylashuvi (chapdan 0px va tepadan 0px)
* <mark style="color:red;">`#prev {left:63px;width:43px;}`</mark> - 63px oʻngga joylashtirilgan (#home kengligi 46px + elementlar orasidagi qoʻshimcha boʻsh joy) va kengligi 43px.
* <mark style="color:red;">`#prev {background:url('img_navsprites.gif') -47px 0;}`</mark> - Background rasmni 47px o'ng tomonga joylashtirishni ifodalaydi (#home kengligi 46px + hamda 1px ajratuvchi chiziq)
* <mark style="color:red;">`#next {left:129px;width:43px;}`</mark> - 129px oʻngga joylashtirilgan (#prev ning boshlanishi 63px + #prev 43px + bo'sh joy) va uning o'lchami 43px.
* <mark style="color:red;">`#next {background:url('img_navsprites.gif') -91px 0;}`</mark> - Background rasmni 91px o'ngga joylashtiradi (#home kengligi 46px +1px ajratuvchi chiziq + #prev kengligi 43px + 1px ajratuvchi chiziq)

### Rasm spritelari - hover effekti <a href="#rasm-spritelar-hover-effect" id="rasm-spritelar-hover-effect"></a>

Endi navigatsiya ro'yxatiga hover effektini qo'shamiz.

{% hint style="warning" %}
**Maslahat:** `:hover` selektori faqatgina havolalarda emas, balki barcha elementlarda ham ishlatilishi mumkin.
{% endhint %}

Bizning yangi ("img\_navsprites\_hover.gif") rasmimiz navigatsiya rasmlari va hoverdan foydalanish uchun 3 ta rasmdan tashkil topgan.

![](<../../.gitbook/assets/image (772).png>)

Bu oltita alohida fayl emas, bitta rasm bo'lgani uchun foydalanuvchi kursorni rasm ustiga olib kelganida yuklashda kechikish bo'lmaydi.

hover effektini qo'shish uchun faqat uch qator kod qo'shamiz xolos:

```
 #home a:hover {
  background: url('img_navsprites_hover.gif') 0 -45px;
}

#prev a:hover {
  background: url('img_navsprites_hover.gif') -47px -45px;
}

#next a:hover {
  background: url('img_navsprites_hover.gif') -91px -45px;
}
```

Misolni tushuntirish:

* <mark style="color:red;">`#home a:hover {background: url('img_navsprites_hover.gif') 0 -45px;}`</mark> - Barcha uchta hoverli rasm uchun, bir xil background postion beramiz faqat 45px pastroq bo'ladi.
