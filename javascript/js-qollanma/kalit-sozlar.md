# Kalit so'zlar

JavaScriptning ushbu maxsus kalit so'zlarini o'zgaruvchi, teg yoki funksiya nomi sifatida ishlata olmaysiz:

| abstract | argumentlar | await\*      | boolean   |
| -------- | ----------- | ------------ | --------- |
| break    | byte        | case         | catch     |
| char     | class\*     | const        | continue  |
| debugger | default     | delete       | do        |
| double   | else        | enum\*       | eval      |
| export\* | extends\*   | false        | final     |
| finally  | float       | for          | function  |
| goto     | if          | implements   | import\*  |
| in       | instanceof  | int          | interface |
| let\*    | long        | native       | new       |
| null     | package     | private      | protected |
| public   | return      | short        | static    |
| super\*  | switch      | synchronized | this      |
| throw    | throws      | transient    | true      |
| try      | typeof      | var          | void      |
| volatile | while       | with         | yield     |

\* bilan belgilangan so'zlar ECMAScript 5 va 6 da qo'shilgan.

{% hint style="warning" %}
JavaScript-ning turli versiyalari haqida batafsil ma'lumotlarni JS versiyalari bo'limida o'qishingiz mumkin.
{% endhint %}

### Olib tashlangan kalit so'zlar

Quyidagi kalit so'zlar ECMAScript 5/6 standartidan olib tashlandi:

| abstract     | boolean | byte      | char     |
| ------------ | ------- | --------- | -------- |
| double       | final   | float     | goto     |
| int          | long    | native    | short    |
| synchronized | throws  | transient | volatile |

{% hint style="warning" %}
Ushbu kalit so'zlarni ham o'zgaruvchi sifatida ishlatmang. ECMAScript 5/6 barcha brauzerlarda to'liq qo'llab-quvvatlanmaydi.
{% endhint %}

### JavaScript obyektlari, xususiyatlari va metodlari

Bundan tashqari, JavaScript-ning built-in obyektlari, xususiyatlari va metodlarining nomidan foydalanishdan saqlanishingiz kerak:

| Array          | Date     | eval      | function  |
| -------------- | -------- | --------- | --------- |
| hasOwnProperty | Infinity | isFinite  | isNaN     |
| isPrototypeOf  | length   | Math      | NaN       |
| name           | Number   | Object    | prototype |
| String         | toString | undefined | valueOf   |

### Java kalit  so'zlari

JavaScript ko'pincha Java bilan birga ishlatiladi. JavaScript identifikatorlari sifatida Javaning ba'zi obyektlari va xususiyatlarini ishlatishdan saqlanishingiz kerak:

| getClass   | java        | JavaArray | javaClass |
| ---------- | ----------- | --------- | --------- |
| JavaObject | JavaPackage |           |           |

### Boshqa kalit so'zlar

JavaScript ko'plab ilovalarda dasturlash tili sifatida ishlatilishi mumkin.

Bundan tashqari, HTML va window obyektlari va xususiyatlari nomidan foydalanishdan saqlanishingiz kerak:

| alert       | all                | anchor             | anchors           |
| ----------- | ------------------ | ------------------ | ----------------- |
| area        | assign             | blur               | button            |
| checkbox    | clearInterval      | clearTimeout       | clientInformation |
| close       | closed             | confirm            | constructor       |
| crypto      | decodeURI          | decodeURIComponent | defaultStatus     |
| document    | element            | elements           | embed             |
| embeds      | encodeURI          | encodeURIComponent | escape            |
| event       | fileUpload         | focus              | form              |
| forms       | frame              | innerHeight        | innerWidth        |
| layer       | layers             | link               | location          |
| mimeTypes   | navigate           | navigator          | frames            |
| frameRate   | hidden             | history            | image             |
| images      | offscreenBuffering | open               | opener            |
| option      | outerHeight        | outerWidth         | packages          |
| pageXOffset | pageYOffset        | parent             | parseFloat        |
| parseInt    | password           | pkcs11             | plugin            |
| prompt      | propertyIsEnum     | radio              | reset             |
| screenX     | screenY            | scroll             | secure            |
| select      | self               | setInterval        | setTimeout        |
| status      | submit             | taint              | text              |
| textarea    | top                | unescape           | untaint           |
| window      |                    |                    |                   |

### HTML event handlerlari

Bundan tashqari, barcha HTML event handlerlarning nomini ishlatishdan saqlanishingiz kerak.

Misollar:

| onblur    | onclick    | onerror     | onfocus     |
| --------- | ---------- | ----------- | ----------- |
| onkeydown | onkeypress | onkeyup     | onmouseover |
| onload    | onmouseup  | onmousedown | onsubmit    |
