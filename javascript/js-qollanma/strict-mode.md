# Strict mode

`"use strict";` javaScript kodi "qat'iy rejimda" bajarilishi kerakligini belgilaydi.

### "use strict" direktivasi

`"use strict"` ECMAScript 5-versiyasida yangi edi.

Bu steytment emas, balki JavaScript-ning avvalgi versiyalarida qo'llanilmagan literal expression.

`"use strict"`ning maqsadi kodni "qat'iy rejimda" bajarilishi kerakligini ko'rsatish hisoblanadi.

Masalan qat'iy rejimda,  e'lon qilinmagan o'zgaruvchilardan foydalana olmaysiz.

Internet Explorer 9 va undan kichik versiyalardan tashqari barcha zamonaviy brauzerlar "qat'iy rejimni" ni qo'llab-quvvatlaydi:

| Directive    | Chrome | Edge | Firefox | Safari | Opera |
| ------------ | ------ | ---- | ------- | ------ | ----- |
| "use strict" | 13.0   | 10.0 | 4.0     | 6.0    | 12.1  |

Quyidagi jadvalda brauzerlar qaysi versiyadan boshlab `let`ni to'liq qo'llab-quvvatlashi ko'rsatilgan.

{% hint style="warning" %}
Barcha dasturlaringizda qat'iy rejimdan foydalanishingiz mumkin. Bu sizga aniqroq kod yozishga yordam beradi, masalan, e'lon qilinmagan o'zgaruvchilardan foydalanishni oldini olish.

`"use strict"` shunchaki string, shuning uchun IE 9 uni tushunmasa ham xatoga yo'l qo'ymaydi.
{% endhint %}

### Qat'iy rejimni e'lon qilish

Qat'iy rejimni skript faly yoki funksiya boshiga "`use strict`" iborasini qo'shish orqali e'lon qilinadi.

Skript boshida e'lon qilinganda, u global miqyosda ishlaydi. (skriptdagi barcha kodlar qat'iy rejimda ishlaydi):

```
"use strict";
x = 3.14;       // This will cause an error because x is not declared
```

```
"use strict";
myFunction();

function myFunction() {
  y = 3.14;   // This will also cause an error because y is not declared
}
```

Funksiya ichida e'lon qilinganda esa, u lokal doirada ishlaydi (faqat funktsiya ichidagi kod qat'iy rejimda bo'ladi):

```
x = 3.14;       // This will not cause an error.
myFunction();

function myFunction() {
  "use strict";
  y = 3.14;   // This will cause an error
}
```

### "use strict"; Sintaksis

Qattiq rejimni e'lon qilish sintaksisi JavaScript-ning eski versiyalari bilan mos ravishda ishlab chiqilgan.

JavaScriptda raqam literalini (4 + 5;) yoki string literalini ("Jon Doe";) kompilyatsiya qilish hech qanday nojo'ya ta'sir ko'rsatmaydi. U shunchaki mavjud bo'lmagan o'zgaruvchiga kompilyatsiya qiladi va o'ladi.

Shuning uchun faqat  `"use strict";`ni "tushunadigan" yangi kompilyatorlar uchun muhimdir.

### Nima uchun qat'iy rejim?

Qay'iy rejim JavaScript-ni "xavfsiz" yozishni osonlashtiradi.

Qat'iy rejim, qatiy rejimsiz yozilgan kodlarda ko'rsatilmagan "sintaktik kamchiliklar" ni xato sifatida ko'rsatadi.

Masalan, oddiy JavaScript-da o'zgaruvchi nomini noto'g'ri kiritish yangi global o'zgaruvchini yaratadi. Qat'iy rejimda bu xatolikka olib keladi va kutilmagan global o'zgaruvchi yaratilmaydi.

Oddiy JavaScript-da, dasturchi yozilmagan xususiyatga qiymat belgilashda xatolik haqida bildirishnoma qabul qilmaydi.

Qatiy rejimda esa yozilmagan xususiyatga, qabul qiluvchi xususiyatga, mavjud bo'lmagan xususiyatga, mavjud bo'lmagan o'zgaruvchiga yoki mavjud bo'lmagan obyektga har qanday qiymat tayinlash xatolikka olib keladi.

### Qat'iy rejimda ruxsat berilmagan ishlar

O'zgaruvchini e'lon qilmasdan foydalanishga yo'l qo'yilmaydi:

```
"use strict";
x = 3.14;                // This will cause an error
```

{% hint style="warning" %}
Obyektlar ham o'zgaruvchidir.
{% endhint %}

Obyektni e'lon qilmasdan foydalanishga yo'l qo'yilmaydi:

```
"use strict";
x = {p1:10, p2:20};      // This will cause an error
```

O'zgaruvchini (yoki obektni) o'chirishga ruxsat berilmaydi.

```
"use strict";
let x = 3.14;
delete x;                // This will cause an error
```

Funksiyani o'chirishga ruxsat berilmaydi.

```
"use strict";
function x(p1, p2) {};
delete x;                // This will cause an error 
```

Parametr nomini takror yozishga ruxsat berilmaydi:

```
"use strict";
function x(p1, p1) {};   // This will cause an error
```

Sakkizlik sanoq tizimidagi sonli harflarga ruxsat berilmaydi:

```
"use strict";
let x = 010;             // This will cause an error
```

Sakkizlik sanoq tizimida  qochish belgilariga ruxsat berilmaydi:

```
"use strict";
let x = "\010";            // This will cause an error
```

Read-only xususiyatiga yozishga ruxsat berilmaydi:

```
"use strict";
const obj = {};
Object.defineProperty(obj, "x", {value:0, writable:false});

obj.x = 3.14;            // This will cause an error
```

Get-only xususiyatiga yozishga ruxsat berilmaydi:

```
"use strict";
const obj = {get x() {return 0} };

obj.x = 3.14;            // This will cause an error
```

O'chirilmaydigan xususiyatni o'chirishga ruxsat berilmaydi:

```
"use strict";
delete Object.prototype; // This will cause an error
```

`eval` so'zini o'zgaruvchi sifatida ishlatib bo'lmaydi:

```
"use strict";
let eval = 3.14;         // This will cause an error
```

`arguments` so'zini o'zgaruvchi sifatida ishlatib bo'lmaydi:

```
"use strict";
let arguments = 3.14;    // This will cause an error
```

`with` steytmentiga ruxsat berilmaydi:

```
"use strict";
with (Math){x = cos(2)}; // This will cause an error
```

Xavfsizlik nuqtai nazaridan, `eval()` chaqirilgan scopeda o'zgaruvchilar yaratishga ruxsat berilmaydi.

{% code title="Qat'iy rejimda o'zgaruvchini e'lon qilishdan oldin ishlatib bo'lmaydi:" %}
```
"use strict";
eval ("x = 2");
alert (x);      // This will cause an error
```
{% endcode %}

{% code title="Qat'iy rejimda eval() var kalit so'zidan foydalanib o'zgaruvchini e'lon qila olmaydi:" %}
```
"use strict";
eval ("var x = 2");
alert (x);    // This will cause an error
```
{% endcode %}

{% code title="eval() o'zgaruvchini let kalit so'zidan foydalanib e'lon qila olmaydi:" %}
```
eval ("let x = 2");
alert (x);        // This will cause an error
```
{% endcode %}

Funktsiyalardagi `this` kalit so'zi qat'iy rejimda boshqacha ishlaydi.

`this` kalit so'zi funksiyani chaqirgan obyektga ishora qiladi.

Agar obyekt ko'rsatilmagan bo'lsa, qat'iy rejimdagi funktsiyalardan `undefined` qaytadi va normal rejimdagi funktsiyalar global obyektni (window) qaytaradi:

```
"use strict";
function myFunction() {
  alert(this); // will alert "undefined"
}
myFunction();
```

### Kelajakning isboti!

Kelajakdagi JavaScript versiyalari uchun ajratilgan kalit so'zlardan qat'iy rejimda o'zgaruvchilar nomi sifatida FOYDALANISH MUMKIN.

Bular:

* implements
* interface
* let
* package
* private
* protected
* public
* static
* yield

```
"use strict";
let public = 1500;      // This will cause an error
```

{% hint style="danger" %}
### Ehtiyot bo'ling!

"use strict" faqat skript yoki funksiya boshida qabul qilinadi.
{% endhint %}
