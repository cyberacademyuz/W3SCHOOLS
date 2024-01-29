# CSS Web shriftlar

### CSS @font-face qoidasi <a href="#css-font-face-qoidasi" id="css-font-face-qoidasi"></a>

Web-shriftlar web-dizaynerlarga foydalanuvchi kompyuteriga o'rnatilmagan shriftlardan foydalanish imkonini beradi.

Foydalanmoqchi bo'lgan shriftingizni topib/sotib olgach, shrift faylini web-serveringizga qo'shing va kerak bo'lganda u avtomatik tarzda foydalanuvchiga yuklab olinadi.

O'zingizning "shaxsiy" shriftlaringiz CSSning `@font-face` qoidasi ichida ifodalanadi.

### Turli shrift formatlari <a href="#har-xil-font-formatlari" id="har-xil-font-formatlari"></a>

#### TrueType Fonts (TTF) <a href="#truetype-fontlar-ttf" id="truetype-fontlar-ttf"></a>

TrueType 1980-yillarning oxirida Apple va Microsoft tomonidan ishlab chiqilgan shrift standarti hisoblanadi. TrueType Mac OS va Microsoft Windows operatsion tizimlari uchun eng keng tarqalgan shrift formatidir.

#### OpenType Fonts (OTF) <a href="#opentype-fontlar-otf" id="opentype-fontlar-otf"></a>

OpenType - kengaytiriladigan kompyuter shriftlari uchun format. U TrueTypeda qurilgan va Microsoft-ning ro'yxatdan o'tgan savdo belgisidir. OpenType Fonts bugungi kunda asosiy kompyuter platformalarida keng qo'llaniladi.

#### The Web Open Font Format (WOFF) <a href="#the-web-open-font-format-woff" id="the-web-open-font-format-woff"></a>

WOFF - Web-sahifalarda foydalanish uchun chiqarilgan shrift formati. U 2009 yilda ishlab chiqilgan va hozirda W3C tavsiyasi hisoblanadi. WOFF aslida OpenType yoki TrueType bo'lib, kompresslangan va qo'shimcha metama'lumotlarga ega. Maqsad tarmoq orqali serverdan clientga shrift distributionini yuborish va shriftdan foydalanish.

#### The Web Open Font Format (WOFF 2.0) <a href="#the-web-open-font-format-woff-20" id="the-web-open-font-format-woff-20"></a>

WOFF 1.0 dan yaxshiroq kompresslashni ta'minlovchi TrueType/OpenType shrift.

#### SVG Shriftlar/Shakllar <a href="#svg-fontlarshakllar" id="svg-fontlarshakllar"></a>

SVG shriftlari matnni ko'rsatishda SVG dan glif sifatida foydalanish imkonini beradi. SVG 1.1 spetsifikatsiyasi SVG hujjatida shriftlarni yaratish imkonini beruvchi font modulini belgilaydi. CSS-ni SVG hujjatlarida ham qo'llashingiz mumkin va `@font-face` qoidasi orqali SVGdagi matnga qo'llanilishi mumkin.

#### Embedded OpenType Fontlar (EOT) <a href="#embedded-opentype-fontlar-eot" id="embedded-opentype-fontlar-eot"></a>

EOT shriftlari Microsoft tomonidan web-sahifalarda o'rnatilgan shriftlar sifatida foydalanish uchun ishlab chiqilgan OpenType shriftlarining ixcham shakli hisoblanadi.

### Brauzerlarning shrift formatlarini qo'llab quvvatlash jadvali <a href="#font-formatlari-uchun-brauzerlar-qollab-quvvatlash-jadvali" id="font-formatlari-uchun-brauzerlar-qollab-quvvatlash-jadvali"></a>

Jadvaldagi raqamlar shrift formatini to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Font format | Edge                  | Chrome                | Firefox               | Safari                | Opera                 |
| ----------- | --------------------- | --------------------- | --------------------- | --------------------- | --------------------- |
| TTF/OTF     | 9.0\*                 | 4.0                   | 3.5                   | 3.1                   | 10.0                  |
| WOFF        | 9.0                   | 5.0                   | 3.6                   | 5.1                   | 11.1                  |
| WOFF2       | 14.0                  | 36.0                  | 39.0                  | 10.0                  | 26.0                  |
| SVG         | Qo'llab quvvatlamaydi | Qo'llab quvvatlamaydi | Qo'llab quvvatlamaydi | 3.2                   | Qo'llab quvvatlamaydi |
| EOT         | 6.0                   | Qo'llab quvvatlamaydi | Qo'llab quvvatlamaydi | Qo'llab quvvatlamaydi | Qo'llab quvvatlamaydi |

\*IE: Shrift formati faqat "o'rnatish mumkin" qilib sozlanganda ishlaydi.

### O'zingiz xohlagan shriftdan foydalanish <a href="#ozingiz-xohlagan-fontdan-foydalanish" id="ozingiz-xohlagan-fontdan-foydalanish"></a>

`@font-face` qoidasida; avval shriftga nom bering (masalan, myFirstFont) va keyin shrift faylini ulang.

{% hint style="warning" %}
**Maslahat:** Shriftning URL manzili uchun har doim kichik harflardan foydalaning. Katta harflar IEda kutilmagan natijalarga olib kelishi mumkin.
{% endhint %}

HTML elementi uchun shriftdan foydalanishda `font-family` xususiyati orqali shrift nomiga (myFirstFont) murojaat qiling:

```
@font-face {
  font-family: myFirstFont;
  src: url(sansation_light.woff);
}

div {
  font-family: myFirstFont;
}
```

### Qalin matndan foydalanish <a href="#qalin-jirniy-matndan-foydalanish" id="qalin-jirniy-matndan-foydalanish"></a>

Qalin matndan foydalanish uchun tavsiflovchilarni o'z ichiga olgan boshqa `@font-face` qoidasini qo'shishingiz kerak:

```
@font-face {
  font-family: myFirstFont;
  src: url(sansation_bold.woff);
  font-weight: bold;
}
```

"_sansation\_bold.woff_" fayli boshqa shrift fayli hisoblanib, unda Sansation shrifti uchun qalin belgilar mavjud.

Brauzerlar “_myFirstFont_” shrift oilasiga mansub matn qalin qilib ko‘rsatilishi kerak bo‘lganda undan foydalanishadi.

Shu tarzda bir xil shriftda ko'plab `@font-face` qoidalariga ega bo'lishingiz mumkin.

### CSSning shrift tavsiflovchilari <a href="#css-font-tavsiflovchilari" id="css-font-tavsiflovchilari"></a>

Quyidagi jadvalda `@font-face` qoidasi ichida belgilanishi mumkin bo'lgan barcha font identifikatorlari keltirilgan:

| Tavsiflovchi  | Qiymatlar                                                                                                                                           | Ta'rif                                                                                               |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| font-family   | _name_                                                                                                                                              | Majburiy. Font nomini belgilaydi                                                                     |
| src           | _URL_                                                                                                                                               | Majburiy. Font faylining URL manzilini belgilaydi                                                    |
| font-stretch  | <p>normal<br>condensed<br>ultra-condensed<br>extra-condensed<br>semi-condensed<br>expanded<br>semi-expanded<br>extra-expanded<br>ultra-expanded</p> | Ixtiyoriy. Font qanday cho'zilishi kerakligini belgilaydi. Standart “normal”                         |
| font-style    | <p>normal<br>italic<br>oblique</p>                                                                                                                  | Ixtiyoriy. Font uslubi qanday bo'lishi kerakligini belgilaydi. Standart “normal”                     |
| font-weight   | <p>normal<br>bold<br>100<br>200<br>300<br>400<br>500<br>600<br>700<br>800<br>900</p>                                                                | Ixtiyoriy. Fontning qalinligini belgilaydi. Standart “normal”                                        |
| unicode-range | _unicode-range_                                                                                                                                     | Ixtiyoriy. Font qo'llab-quvvatlaydigan UNICODE belgilar oralig'ini belgilaydi. Standart “U+0-10FFFF” |
