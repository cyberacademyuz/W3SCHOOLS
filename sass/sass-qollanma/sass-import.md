# Sass @import

Sass CSS kodlarini DRY (O'zingni qayta takrorlama) prinsipi asosida saqlaydi. DRY usulida kod yozishning bir usuli kodlarni alohida fayllarda saqlashdir.

Kodlarni boshqa Sass fayllariga ulash uchun CSS snippetlari orqali kichik fayllar yaratishingiz mumkin. Bunday fayllar faylni tiklash, o'zgaruvchilar, ranglar, shriftlar, shrift o'lchamlari va boshqalar misol bo'lishi mumkin.

### Sass Fayllarni import qilish <a href="#sass-fayllarni-import-qilish" id="sass-fayllarni-import-qilish"></a>

Xuddi CSS singari, Sass ham `@import` direktivasini qo'llab-quvvatlaydi.

`@import` direktivasi bir faylning tarkibini boshqasiga ulash imkonini beradi.

CSSdagi `@import` direktivasi, performancedagi muammolari tufayli katta kamchiliklarga ega; unga har safar murojaat qilganingizda qo'shimcha HTTP so'rovini yaratadi. Biroq, Sassning `@import` direktivasi CSS-dagi faylni o'z ichiga oladi; shuning uchun ish vaqtida qo'shimcha HTTP chaqiruvi talab qilinmaydi!

{% code title="Sass @import sintaksisi" %}
```
@import filename;
```
{% endcode %}

**Maslahat**: Fayl kengaytmasini berishingiz shart emas, Sass avtomatik tarzda .`sass` yoki `.scss` faylini nazarda tutayotganingizni biladi. CSS fayllarini ham import qilishingiz mumkin. `@import` direktivasi faylni import qiladi va import qilingan faylda belgilangan har qanday o'zgaruvchilar yoki aralashmalarni keyinchalik asosiy faylda ishlatilishini taminlaydi.

Asosiy faylga keraklicha fayllarni import qilishingiz mumkin:

```
@import "variables";
@import "colors";
@import "reset";
```

Misolni ko'rib chiqamiz: Faraz qilaylik, bizda "reset.scss" nomli qayta o'rnatish fayli bor, u quyidagicha ko'rinadi:

```
html,
body,
ul,
ol {
  margin: 0;
  padding: 0;
}
```

va endi biz "reset.scss" faylini "standard.scss" deb nomlangan boshqa faylga import qilmoqchimiz.

Buni qanday qilamiz: Faylning yuqori qismiga `@import` direktivasini qo'shamiz; shu tarzda uni foydalanish mumkin bo'lgan global scopega aylantiramiz:

```
@import "reset";

body {
  font-family: Helvetica, sans-serif;
  font-size: 18px;
  color: red;
}
```

Va qachonki standard.scss fayli CSSga o'girilganda, CSS fayl mana bu ko'rinishda bo'ladi

```
html, body, ul, ol {
  margin: 0;
  padding: 0;
}

body {
  font-family: Helvetica, sans-serif;
  font-size: 18px;
  color: red;
}
```

### Sass Partials <a href="#sass-partials" id="sass-partials"></a>

Standart tarzda, Sass barcha `.scss` fayllarini to'g'ridan-to'g'ri CSSga o'giradi. Biroq, faylni import qilmoqchi bo'lganingizda, faylni to'g'ridan-to'g'ri o'girish kerak emas.

Sassda buning uchun mexanizm mavjud: Agar fayl nomini pastki chiziq bilan boshlasangiz, Sass uni o'girmaydi. Shu tarzda nomlangan fayllar Sassda Partials deb ataladi.

Shunday qilib, Sassning Partials fayli faylning boshida pastki chiziq bilan yozish orqali nomlanadi:

{% code title="Sass Partial Sintaksisi" %}
```
_filename;
```
{% endcode %}

Quyidagi misolda "\_colors.scss" nomli partials fayli ko'rsatilgan. (Ushbu fayl to'g'ridan-to'g'ri "colors.css" ga o'girilmaydi):

```
$myPink: #EE82EE;
$myBlue: #4169E1;
$myGreen: #8FBC8F;
```

Endi partial faylni import qilganingizda, pastki chiziqni yozmang. Sassning o'zi "\_colors.scss" faylini import qilishi kerakligini tushunadi:

```
@import "colors";

body {
  font-family: Helvetica, sans-serif;
  font-size: 18px;
  color: $myBlue;
}
```
