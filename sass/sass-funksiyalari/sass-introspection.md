# Sass Introspection

### Sass introspeksiya funksiyalari <a href="#sass-introspeksiya-funksiyalari" id="sass-introspeksiya-funksiyalari"></a>

Stylesheet yaratishda introspeksiya funksiyalari kamdan-kam qo'llaniladi. Biroq, agar biror nima to'g'ri ishlamasa, nima bo'layotganini aniqlash uchun ishlatilishi mumkin: masalan, debugging funksiyalari.

Quyidagi jadvalda Sass-dagi barcha introspeksiya funksiyalari keltirilgan:

| Funksiya                                 | Ta'rif & Misol                                                                                                                                                                                                               |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| call(_function_, _arguments_...)         | Funktsiyani argumentlar bilan chaqiradi va natijani qaytaradi.                                                                                                                                                               |
| content-exists()                         | Joriy mixin `@content` blokidan o'tganligini tekshiradi.                                                                                                                                                                     |
| feature-exists(_feature_)                | <p><em>feature</em>  joriy Sass ilovasi tomonidan qo'llab-quvvatlanishini tekshiradi.<br><strong>Misol:</strong><br>feature-exists("at-error");<br>Natija: true</p>                                                          |
| function-exists(_functionname_)          | <p>Belgilangan funksiya mavjudligini tekshiradi.<br><strong>Misol:</strong><br>function-exists("nonsense")<br>Natija: false</p>                                                                                              |
| get-function(_functionname_, css: false) | Belgilangan funktsiyani qaytaradi. Agar CSS true bo'lsa, uning o'rniga oddiy CSS funksiyasini qaytaradi.                                                                                                                     |
| global-variable-exists(_variablename_)   | <p>Belgilangan global o'zgaruvchi bor yo'qligini tekshiradi.<br><strong>Misol:</strong><br>variable-exists(a)<br>Natija: true</p>                                                                                            |
| inspect(_value_)                         | _qiymat_ ning strring tasvirini qaytaradi.                                                                                                                                                                                   |
| mixin-exists(_mixinname_)                | <p>Belgilangan mixin bor yo'qligini tekshiradi.<br><strong>Misol:</strong><br>mixin-exists("important-text")<br>Natija: true</p>                                                                                             |
| type-of(_value_)                         | <p><em>qiymat</em> turini qaytaradi. Number, string, color, list, map, bool, null, function, arglist boʻlishi mumkin.<br><strong>Misol:</strong><br>type-of(15px)<br>Natija: number<br>type-of(#ff0000)<br>Natija: color</p> |
| unit(_number_)                           | <p>Raqam bilan bog'langan uzunlik o'lchov birlikni qaytaradi.<br><strong>Misol:</strong><br>unit(15px)<br>Natija: px</p>                                                                                                     |
| unitless(_number_)                       | <p>Berilgan raqamda u bilan bog'langan uzunlik o'lchov birligi bor yo'qligini tekshiradi.<br><strong>Misol:</strong><br>unitless(15px)<br>Natija: false<br>unitless(15)<br>Natija: true</p>                                  |
| variable-exists(_variablename_)          | <p>Berilgan o'zgaruvchining joriy scopeda bor yo'qligini tekshiradi.<br><strong>Example:</strong><br>variable-exists(b)<br>Result: true</p>                                                                                  |
