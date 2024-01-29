# Vue CSS binding

{% hint style="success" %}
`v-bind`CSS-ni `style`va atributlari bilan o'zgartirish uchun qanday foydalanish haqida ko'proq bilib oling `class`.

`style`Va `class`atributlarni o'zgartirish tushunchasi `v-bind`juda aniq bo'lsa-da, sintaksisga biroz ko'nikish kerak bo'lishi mumkin.
{% endhint %}

### Vue-da dinamik CSS

Siz va atributlaridan `v-bind`foydalanib CSS-ni o'zgartirish uchun Vue-dan qanday foydalanishimiz mumkinligini allaqachon ko'rgansiz . Ushbu qo'llanmada qisqacha tushuntirilgan va Vue o'zgaruvchan CSS bilan bir nechta misollar ham berilgan.`styleclass`[`v-bind`](https://www-w3schools-com.translate.goog/vue\_v-bind.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)

Bu erda biz CSS-ni Vue yordamida qanday qilib dinamik ravishda o'zgartirish mumkinligini batafsilroq tushuntiramiz. Biroq, avval ushbu qo'llanmada ko'rgan texnikalar bilan ikkita misolni ko'rib chiqaylik: in-line styling va `v-bind:style`sinf tayinlash.`v-bind:class`

### In chiziqli uslublar

`v-bind:style`Biz Vue-da in-line uslublarini qilish uchun foydalanamiz.

Element chiziqli uslubdan foydalangan holda elementning `<input type="range">`shaffofligini o'zgartirish uchun ishlatiladi .`<div>`

```
<input type="range" v-model="opacityVal">
<div v-bind:style="{ backgroundColor: 'rgba(155,20,20,'+opacityVal+')' }">
  Drag the range input above to change opacity here.
</div>
```

### Sinf tayinlash

`v-bind:class`Biz Vue-da HTML tegiga sinf belgilash uchun foydalanamiz.

Oziq-ovqat tasvirlarini tanlang. `v-bind:class`Tanlangan oziq-ovqat siz tanlagan narsani ko'rsatish uchun yordamida ta'kidlanadi.

```
<div v-for="(img, index) in images">
  <img v-bind:src="img.url"
       v-on:click="select(index)"
       v-bind:class="{ selClass: img.sel }">
</div>
```

### Sinflar va uslublarni belgilashning boshqa usullari

Foydalanishning turli jihatlari `v-bind:class`va `v-bind:style`biz ushbu qo'llanmada ilgari ko'rmaganmiz:

1. CSS sinflari ikkalasi bilan HTML tegiga tayinlanganda `class=""`va `v-bind:class=""`Vue sinflarni birlashtiradi.
2. Bir yoki bir nechta sinflarni o'z ichiga olgan ob'ekt bilan tayinlangan `v-bind:class="{}"`. Ob'ekt ichida bir yoki bir nechta sinflarni yoqish yoki o'chirish mumkin.
3. `v-bind:style`CSS xususiyatini belgilashda in-line uslub ( ) bilan camelCase afzalroqdir, lekin agar u tirnoq ichida yozilgan bo'lsa, "kabob-case" dan ham foydalanish mumkin.
4. CSS sinflari massivlar / massiv belgilari / sintaksisi bilan tayinlanishi mumkin

Ushbu fikrlar quyida batafsilroq tavsiflanadi.

### 1. Vue "sinf" va "v-bind: sinf" ni birlashtiradi

HTML yorlig'i bilan tayinlangan sinfga tegishli bo'lgan `class=""`va shuningdek, bilan sinfga tayinlangan hollarda `v-bind:class=""`, Vue biz uchun sinflarni birlashtiradi.

Element `<div>`ikkita sinfga tegishli: "impClass" va "yelClass". "Muhim" sinf atribut bilan normal tarzda o'rnatiladi `class`va "sariq" sinf bilan o'rnatiladi `v-bind:class`.

```
<div class="impClass" v-bind:class="{yelClass: isYellow}">
  This div belongs to both 'impClass' and 'yelClass'.
</div>
```

### 2. 'v-bind:class' bilan bir nechta sinflarni tayinlash

ga ega bo'lgan sinfga HTML elementini tayinlashda `v-bind:class="{}"`biz bir nechta sinflarni ajratish va belgilash uchun verguldan foydalanishimiz mumkin.

`<div>`Vue ma'lumotlarining "isYellow" va "isImportant" xususiyatlariga qarab, element "impClass" va "yelClass" sinflariga tegishli bo'lishi mumkin.

```
<div v-bind:class="{yelClass: isYellow, impClass: isImportant}">
  This tag can belong to both the 'impClass' and 'yelClass' classes.
</div>
```

### 3. “V-bind:style” bilan tuya va kabob o‘rtasidagi belgi

Vue-da CSS-ni chiziqli uslub bilan o'zgartirganda ( `v-bind:style`), CSS xususiyati uchun camelCase notatsiyasidan foydalanish tavsiya etiladi, ammo CSS xususiyati tirnoq ichida bo'lsa, "kabob-case" dan ham foydalanish mumkin.

Bu yerda biz CSS xususiyatlarini `background-color`va element `font-weight`uchun `<div>`ikki xil usulda o‘rnatamiz: camelCase bilan tavsiya etilgan usul `backgroundColor`va qo‘shtirnoq ichidagi “kabob qutisi” bilan tavsiya etilmaydigan usul `'font-weight'`. Ikkala muqobil ish.

```
<div v-bind:style="{ backgroundColor: 'lightpink', 'font-weight': 'bolder' }">
  This div tag has pink background and bold text.
</div>
```

{% hint style="warning" %}
“Tuya ishi” va “kabob idishi” yozuvlari boʻsh joy va tinish belgilarisiz qator soʻzlarni yozish usullaridir.

* **Tuya ishi** belgisi birinchi so'z kichik harf bilan boshlanadi va keyin har bir so'z bosh harf bilan boshlanadi, masalan, "backgroundColor" yoki "camelCaseNotation". Bu tuya ishi deb ataladi, chunki biz har bir bosh harfni tuyaning orqa tomonidagi dumga o'xshashligini tasavvur qilishimiz mumkin.
* **Kabob holati**`-` belgisi - bu so'zlar "fon rangi" yoki "kabob ko'rinishi" kabi chiziqcha bilan ajratilganda . Bu kabob qutisi deb ataladi, chunki biz "shish kabob"dagi shishka o'xshash chiziqlarni tasavvur qilishimiz mumkin.
{% endhint %}

### 4. 'v-bind:class' bilan massiv sintaksisi

Biz bir nechta sinflarni qo'shish uchun massiv sintaksisidan foydalanishimiz mumkin `v-bind:class`. Massiv sintaksisi bilan biz Vue xususiyatiga bog'liq bo'lgan ikkala sinfdan ham, Vue xususiyatiga bog'liq bo'lmagan sinflardan ham foydalanishimiz mumkin.

Bu erda biz massiv sintaksisi bilan "impClass" va "yelClass" CSS sinflarini o'rnatdik. "impClass" klassi Vue xususiyatiga bog'liq `isImportant`va "yelClass" klassi har doim elementga biriktirilgan `<div>`.

```
<div v-bind:class="[{ impClass: isImportant }, 'yelClass' ]">
  This div tag belongs to one or two classes depending on the isImportant property.
</div>
```
