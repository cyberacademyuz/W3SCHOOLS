# DOM Document

DOM hujjat obyekti veb-sahifangizdagi barcha boshqa obyektlarning egasidir.

### HTML DOM - Document object

Hujjat obyekti veb-sahifangizni ifodalaydi.

Agar HTML-sahifadagi istalgan elementga murojaat qilishni istasangiz, doimo hujjat obyektiga murojaat qilishdan boshlaysiz.

Quyida HTML-ga murojaat qilish va uni boshqarish uchun hujjat obyektidan qanday foydalanish mumkinligi haqidagi ba'zi misollar keltirilgan.

### HTML elementlarini topish

| Metod                                   | Ta'rif                                     |
| --------------------------------------- | ------------------------------------------ |
| document.getElementById(_id_)           | Elementni uning id-si yordamida topish     |
| document.getElementsByTagName(_name_)   | Elementlarni teg nomi bilan topish         |
| document.getElementsByClassName(_name_) | Elementlarni uning class nomi bilan topish |

### HTML elementlarini o'zgartirish

| Xususiyat                                  | Ta'rif                                           |
| ------------------------------------------ | ------------------------------------------------ |
| _element_.innerHTML =  _new html content_  | Elementning ichki HTML-ni o'zgartiring           |
| _element_._attribute = new value_          | HTML elementining atribut qiymatini o'zgartirish |
| _element_.style._property = new style_     | HTML elementining stilini o'zgartirish           |
| Metod                                      | Ta'rif                                           |
| _element_.setAttribute_(attribute, value)_ | HTML elementining atribut qiymatini o'zgartirish |

### Elementlarni qo'shish va o'chirish

| Metod                             | Ta'rif                            |
| --------------------------------- | --------------------------------- |
| document.createElement(_element_) | HTML elementini yaratish          |
| document.removeChild(_element_)   | HTML elementini o'chirish         |
| document.appendChild(_element_)   | HTML element qo'shish             |
| document.replaceChild(_new, old_) | HTML elementini almashtirish      |
| document.write(_text_)            | HTMLning chiquvchi oqimiga yozish |

### Hodisa boshqaruvchilarini qo'shish

| Metod                                                      | Ta'rif                                                   |
| ---------------------------------------------------------- | -------------------------------------------------------- |
| document.getElementById(_id_).onclick = function(){_code_} | Onclick hodisasiga hodisa boshquruvining kodini qo'shish |

### HTML obyektlarini topish

Birinchi DOM 1-bosqichi  11 ta HTML obyektini, obyektlar to'plamini va xususiyatlarini yaratdi. Ular hali ham HTML5 da bor.

Keyinchalik, DOM 3-bosqichda ko'proq obyektlarm to'plamlar va xususiyatlar qo'shildi.

| Xususiyat                    | Ta'rif                                                             | DOM bosqichi |
| ---------------------------- | ------------------------------------------------------------------ | ------------ |
| document.anchors             | Name atributiga ega barcha elementlarni qaytaradi                  | 1            |
| document.applets             | Eskirgan                                                           | 1            |
| document.baseURI             | Hujjatning mutlaq asosiy URI-ni qaytaradi                          | 3            |
| document.body                | \<body> elementini qaytaradi                                       | 1            |
| document.cookie              | Hujjatning cookie-sini qaytaradi                                   | 1            |
| document.doctype             | Hujjatning doctype-ini qaytaradi                                   | 3            |
| document.documentElement     | \<html> elementini qaytaradi                                       | 3            |
| document.documentMode        | Brauzer tomonidan ishlatiladigan rejimni qaytaradi                 | 3            |
| document.documentURI         | Hujjatning URI-ni qaytaradi                                        | 3            |
| document.domain              | Hujjat serverining domen nomini qaytaradi                          | 1            |
| document.domConfig           | Obsolete                                                           | 3            |
| document.embeds              | Barcha \<embed> elementlarini qaytaradi                            | 3            |
| document.forms               | Barcha \<form> elementlarini qaytaradi                             | 1            |
| document.head                | \<head> elementini qaytaradi                                       | 3            |
| document.images              | Barcha \<img> elementlarini qaytaradi                              | 1            |
| document.implementation      | DOM ilovasini qaytaradi                                            | 3            |
| document.inputEncoding       | Hujjatning kodlanishini qaytaradi (belgilar to'plami)              | 3            |
| document.lastModified        | Hujjat yangilangan sana va vaqtni qaytaradi                        | 3            |
| document.links               | Href atributiga ega barcha \<area> va \<a> elementlarini qaytaradi | 1            |
| document.readyState          | Hujjatning (yuklanish) holatini qaytaradi                          | 3            |
| document.referrer            | Yo'naltiruvchining URI-ni qaytaradi (bog'lovchi hujjat)            | 1            |
| document.scripts             | Barcha \<script> elementlarini qaytaradi                           | 3            |
| document.strictErrorChecking | Xatolarni tekshirish amalga oshirilsa, qaytariladi                 | 3            |
| document.title               | \<title> elementini qaytaradi                                      | 1            |
| document.URL                 | Hujjatning to'liq URL manzilini qaytaradi                          | 1            |
