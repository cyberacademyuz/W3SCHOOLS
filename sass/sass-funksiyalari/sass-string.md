# Sass String

### Sass String funksiyalari <a href="#sass-satr-funksiyalari" id="sass-satr-funksiyalari"></a>

String funksiyalari stringlarni manipulyatsiya qilish va ular haqida ma'lumot olish uchun ishlatiladi.

Sass stringlari 1 dan boshlanuvchi indeksga asoslangan. Ya'ni stringdagi birinchi belgi 0 emas, balki 1-indeksda joylashadi.

Quyidagi jadvalda Sass-dagi barcha string funksiyalarining ro'yxati keltirilgan:

| Funksiya                                | Ta'rid & Misol                                                                                                                                                                                                                                          |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| quote(_string_)                         | <p>Stringga qo'shtirnoq qo'ashadi.<br><strong>Misol:</strong><br>quote(Hello world!)<br>Natija: "Hello world!"</p>                                                                                                                                      |
| str-index(_string_, _substring_)        | <p><em>string</em> ichidagi <em>sub string</em> ning birinchi aniqlangan indeksini qaytaradi.<br><strong>Misol:</strong><br>str-index("Hello world!", "H")<br>Natija: 1</p>                                                                             |
| str-insert(_string_, _insert_, _index_) | <p>Berilgan stringni ko'rsatilgan  <em>indeks</em> joylashuviga kiritgan holda qaytaradi<br><strong>Misol:</strong><br>str-insert("Hello world!", " wonderful", 6)<br>Natija: "Hello wonderful world!"</p>                                              |
| str-length(_string_)                    | <p><em>string</em> ning uzunligini qaytaradi (belgilarda).<br><strong>Misol:</strong><br>str-length("Hello world!")<br>Natija: 12</p>                                                                                                                   |
| str-slice(_string_, _start_, _end_)     | <p><em>string</em> dan belgilarni ajratib oladi; <em>berilgan indeksdan</em> boshlanadi va to'htashi kerak bo'lgan indeksda tugaydi va kesilgan natijani qaytaradi.<br><strong>Misol:</strong><br>str-slice("Hello world!", 2, 5)<br>Natija: "ello"</p> |
| to-lower-case(_string_)                 | <p><em>string</em> ni kichik harflarga aylantiradi.<br><strong>Misol:</strong><br>to-lower-case("Hello World!")<br>Natija: "hello world!"</p>                                                                                                           |
| to-upper-case(_string_)                 | <p><em>string</em> ni katta harflarga aylantiradi.<br><strong>Misol:</strong><br>to-upper-case("Hello World!")<br>Natija: "HELLO WORLD!"</p>                                                                                                            |
| unique-id()                             | <p>Unikal random string qaytaradi (joriy sass sessiyasida unikal bo'lishi kafolatlangan).<br><strong>Misol:</strong><br>unique-id()<br>Natija: tyghefnsv</p>                                                                                            |
| unquote(_string_)                       | <p><em>string</em> dagi har qanday qo'shtirnoqlarni olib tashlaydi.<br><strong>Misol:</strong><br>unquote("Hello world!")<br>Natija: Hello world!</p>                                                                                                   |
