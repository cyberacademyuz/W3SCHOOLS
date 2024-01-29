# Sass Kirish

### Boshlashdan avval bilishingiz kerak bo'lgan nasalar <a href="#siz-nimalarni-oldindan-bilishingiz-zarur" id="siz-nimalarni-oldindan-bilishingiz-zarur"></a>

Sassni o'rganishda davom etishdan avval quyidagilarni hech bo'lmaganda boshlang'ich darajada bilishingiz kerak:

* HTML
* CSS

Agar bularni o'rganmoqchi bo'lsangiz unda bizning bosh sahifamizga o'tib darsliklarni o'rganing

### Sass nima ? <a href="#sass-nima" id="sass-nima"></a>

* **Sass** - **S**yntactically **A**wesome **S**tyle**S**heet so'zining qisqartmasi bo'lib o'zbekchada Sintaksisi taraflama ajoyib bo'lgan uslublar jadvali degan ma'noni anglatadi
* Sass CSS uchun kengaytma hisoblanadi
* Sass CSS ning pre-protsessori hisoblanadi
* Sass CSS ning barcha versiyalari uchun ishlaydi
* Sass CSS kodlarining takrorlanishini kamaytiradi va shu orqali vaqtni tejaydi.
* Sass **Hampton Catlin** va **Natali Vayzenbaum** tomonidan 2006-yilda ishlab chiqilgan
* Sass yuklab olish va ishlatish uchun bepul

### Sass nimaga ishlatiladi ? <a href="#sass-nimaga-ishlatiladi" id="sass-nimaga-ishlatiladi"></a>

Stylesheetlar kattalashib, murakkablashib bormoqda va ularni saqlash va ishlatish ham qiyinlashyapti. Bunda CSS pre-protsessori yordam berad oladi.

Sass sizga CSS-da mavjud bo'lmagan o'zgaruvchilardan, ichki qoidalardan, aralashmalardan, importlardan, inheritancedan, o'rnatilgan funksiyalardan va boshqa shu kabi xususiyatlardan foydalanish imkonini beradi.

### Sass nima uchun foydali ekanligiga oddiy bir misol <a href="#nimaga-sass-foydali-ekanligiga-sodda-misol" id="nimaga-sass-foydali-ekanligiga-sodda-misol"></a>

Aytaylik, bizda uchta asosiy rangga ega veb-sayt mavjud:

<figure><img src="../../.gitbook/assets/image (741).png" alt=""><figcaption></figcaption></figure>

Shunday qilib, HEX qiymatlarini necha marta yozishingiz kerak ? Ko'p marta. Bir xil ranglardan foydalanishni boshqa narsaga almashtirishga nima deysiz ?

Yuqoridagi qiymatlarni ko'p marta kiritish o'rniga, Sass dan foydalanishingiz va quyidagi kodni yozishingiz mumkin:

```
/* define variables for the primary colors */
$primary_1: #a2b9bc;
$primary_2: #b2ad7f;
$primary_3: #878f99;

/* use the variables */
.main-header {
  background-color: $primary_1;
}

.menu-left {
  background-color: $primary_2;
}

.menu-right {
  background-color: $primary_3;
}
```

Sass-dan foydalanganingizda, asosiy rang o'zgarsa, uni faqat bitta joyda o'zgartirishingiz kerak.

### Sass qanday ishlaydi ? <a href="#sass-qanday-ishlaydi" id="sass-qanday-ishlaydi"></a>

Brauzer Sass kodini tushunmaydi. Shuning uchun, Sass kodini standart CSS-ga aylantirish uchun sizga Sass pre-protsessori kerak bo'ladi.

Bu jarayon pranspiling (o'girish) deb ataladi. Shunday qilib, transpilerga (qandaydir dastur) Sass kodini berishingiz va keyin undan CSS kodini olishingiz kerak.

{% hint style="warning" %}
**Maslahat**: Transpiling - bu bir tilda yozilgan manba kodini olish va uni boshqa tilga aylantirish/o'giirishni bildiruvchi atamadir.
{% endhint %}

### Sass Fayl turi <a href="#sass-fayl-turi" id="sass-fayl-turi"></a>

Sass fayllari **.scss** fayl turida saqlanadi

### Sass Izohlar <a href="#sass-izohlari" id="sass-izohlari"></a>

Sass CSSning izohlarini qo'llab-quvvatlaydi `/* comment */` va qo'shimcha ravishda u inline izohlarni ham qo'llab-quvvatlaydi `// comment`:

```
/* define primary colors */
$primary_1: #a2b9bc;
$primary_2: #b2ad7f;

/* use the variables */
.main-header {
  background-color: $primary_1; // here you can put an inline comment
}
```
