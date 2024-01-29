# CSS Birliklari

### CSS Unitlar <a href="#css-unitlar" id="css-unitlar"></a>

CSS da uzunlikni o'lchash uchun har xil (o'lchov) birliklardan foydalaniladi.

Ko'plab CSS xususiyatlari "length" qiymatlarini oladi, masalan `width`, `margin`, `padding`, `font-size` va hokazolar

**Length** - uzunlik birligi bilan birga keladigan raqam, masalan 10px, 20em...

```
h1 {
  font-size: 60px;
}

p {
  font-size: 25px;
  line-height: 50px;
}
```

**Eslatma**: Raqam va birlik o'rtasida bo'sh joy bo'lmasligi kerak. Ammo, qiymat 0 bo'lsa, birlikdan foydalanmaslik mumkin.

CSSning ba'zi xususiyatlarida manfiy uzunlikdan foydalanish mumkin

Uzunlik birliklarining ikki xil turi bor: Absolute va Relative

### Absolute uzunlik o'lchovlari <a href="#absolute-length-lar" id="absolute-length-lar"></a>

Absolute uzunlik o'lchov birliklari oldindan belgilangan bo'ladi va ularning har birida ifodalangan uzunlik aynan shu o'lchamda ko'rinadi.

Ekranlar bilan ishlayotganda Absolute uzunilik birligidan foydalanish tavsiya qilinmaydi, sababi hamma ekran o'lchamlari ham bir xil emas. Ammo agar o'rtacha qiymat ma'lum bo'lsa absolute qiymatdan foydalansa bo'ladi.

| Uzunlik o'lchov birligi | Ta'rif                             |
| ----------------------- | ---------------------------------- |
| cm                      | santimetrlar                       |
| mm                      | millimeterlar                      |
| in                      | inch (1in = 96px = 2.54cm)         |
| px \*                   | piksellar (1px = 1in ning 1/96 si) |
| pt                      | pointlar (1pt = 1in ning 1/72 si)  |
| pc                      | picas (1pc = 12 pt)                |

\* Piksellar (px) foydalanilayitgan qurilmaga qarab o'z qiymatini o'zgartirishi mumkin. Past dpi-li qurilmalar uchun 1px qurilma displeyning 1 pikseli (nuqtasi) hisoblanadi. Printerlar va yuqori aniqlikdagi ekranlar uchun 1px qurilma piksellarining bir nechtasini bildiradi.

### Relative uzunlik birliklari <a href="#relative-length-lar" id="relative-length-lar"></a>

Relative uzunlik birliklari, boshqa uzunlik xususiyatlariga nisbatan uzunlikni belgilaydi. Relative uzunlik birliklari turli renderlash vositalari o'rtasida yaxshiroq o'lchaydi.

| O'lchov birliklari | Ta'rif                                                                                             |
| ------------------ | -------------------------------------------------------------------------------------------------- |
| em                 | Elementning shrift o'lchamiga nisbatan (2em joriy shrift hajmidan 2 baravar kattaligini bildiradi) |
| ex                 | Joriy shriftning x balandligiga nisbatan (kamdan-kam ishlatiladi)                                  |
| ch                 | "0" ning kengligiga nisbatan (nol)                                                                 |
| rem                | Ildiz elementining shrift o'lchamiga nisbatan                                                      |
| vw                 | Ko'rish oynasi kengligining 1% ga nisbatan\*                                                       |
| vh                 | Ko'rish oynasi balandligining 1% ga nisbatan\*                                                     |
| vmin               | Ko'rish oynasi\* kichikroq o'lchamining 1% ga nisbatan                                             |
| vmax               | Ko'rish oynasi\* kattaroq o'lchamining 1% ga nisbatan                                              |
| %                  | Asosiy elementga nisbatan                                                                          |

{% hint style="warning" %}
**Maslahat:** _Em_ va _rem_ birliklari mukammal kengaytiriladigan layout yaratishda eng yaxshi tanlov!

\* Viewport = brauzer oynasining o'lchami. Agar viewport kengligi 50 sm bo'lsa, 1vw = 0,5 sm bo'ladi.
{% endhint %}

### Brauzerning qo'llab quvvatlashi <a href="#brauzer-qollab-quvvatlashi" id="brauzer-qollab-quvvatlashi"></a>

Jadvaldagi raqamlar length birligini to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Uzunlik birliklari                | Chrome | Edge | Firefox | Safari | Opera |
| --------------------------------- | ------ | ---- | ------- | ------ | ----- |
| em, ex, %, px, cm, mm, in, pt, pc | 1.0    | 3.0  | 1.0     | 1.0    | 3.5   |
| ch                                | 27.0   | 9.0  | 1.0     | 7.0    | 20.0  |
| rem                               | 4.0    | 9.0  | 3.6     | 4.1    | 11.6  |
| vh, vw                            | 20.0   | 9.0  | 19.0    | 6.0    | 20.0  |
| vmin                              | 20.0   | 12.0 | 19.0    | 6.0    | 20.0  |
| vmax                              | 26.0   | 16.0 | 19.0    | 7.0    | 20.0  |
