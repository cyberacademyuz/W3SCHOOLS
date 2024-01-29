# WEB Storage API

Web Storage API - bu brauzerda ma'lumotlarni saqlash va olish uchun sodda sintaksis. Undan foydalanish juda oson:

```
localStorage.setItem("name", "John Doe");
localStorage.getItem("name");
```

Web Storage API barcha brauzerlarda qo'llab-quvvatlanadi:

| Chrome | IE/Edge | Firefox | Safari | Opera |
| ------ | ------- | ------- | ------ | ----- |
| Ha     | Ha      | Ha      | Ha     | Ha    |

### LocalStorage obyekti

localStorage obyekti ma'lum bir sayt uchun lokal xotiraga murojaat qilishni ta'minlaydi. Bu ushbu domen uchun maʼlumotlarni saqlash, oʻqish, qoʻshish, oʻzgartirish va oʻchirish imkonini beradi.

Ma'lumotlar amal qilish muddatisiz saqlanadi va brauzer yopilganda o'chirilmaydi.

Ma'lumotlar kunlar, haftalar va yillar davomida ham mavjud bo'ladi.

### setItem() metodi

`localStorage.setItem()` metodi ma'lumotlar elementini xotirada saqlaydi.

U parametr sifatida nom va qiymat qabul qiladi:

```
localStorage.setItem("name", "John Doe");
```

### getItem() metodi

`localStorage.getItem()` metod xotiradan ma'lumotlar elementini oladi.

U parametr sifatida nom qabul :

```
localStorage.getItem("name");
```

### sessionStorage obyekti

`sessionStorage` obyekti `localStorage` obyekti bilan bir xil.

Farqi shundaki, `sessionStorage` obyekti ma’lumotlarni bitta sessiya uchungina saqlaydi.

Brauzer yopilganda ma'lumotlar o'chiriladi.

```
sessionStorage.getItem("name")
```

### setItem() metodi

`SessionStorage.setItem()` metodi ma'lumotlar elementini xotirada saqlaydi.

U parametr sifatida nom va qiymat qabul qiladi:

```
sessionStorage.setItem("name", "John Doe");
```

### getItem() metodi

`sessionStorage.getItem()` metod xotiradan maʼlumotlar elementini oladi.

U parametr sifatida nom qabul qiladi:

```
sessionStorage.getItem("name");
```

### Storage obeyktining xususiyatlari va metodlari

| Xususiyat/Metod                                                                                                                                                        | Ta'rif                                                                             |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| [key(_n_)](https://www-w3schools-com.translate.goog/jsref/met\_storage\_key.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                        | Xotiradagi n-kalit nomini qaytaradi                                                |
| [length](https://www-w3schools-com.translate.goog/jsref/prop\_storage\_length.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                      | Storage obyektida saqlangan ma'lumotlar elementlarining sonini qaytaradi           |
| [getItem(_keyname_)](https://www-w3schools-com.translate.goog/jsref/met\_storage\_getitem.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)          | Belgilangan kalit nomining qiymatini qaytaradi                                     |
| [setItem(_keyname_, _value_)](https://www-w3schools-com.translate.goog/jsref/met\_storage\_setitem.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Xotiraga kalit qo'shadi yoki (agar kalit mavjud bo'lsa) kalit qiymatini yangilaydi |
| [removeItem(_keyname_)](https://www-w3schools-com.translate.goog/jsref/met\_storage\_removeitem.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)    | Bu kalitni storagedan olib tashlaydi                                               |
| [clear()](https://www-w3schools-com.translate.goog/jsref/met\_storage\_clear.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                       | Storagedagi barcha kalitlarni bo'shating                                           |

### Web Storage API uchun tegishli sahifalar

| Xususiyat                                                                              | Ta'rif                                                                                                  |
| -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [window.localStorage](https://www.w3schools.com/jsref/prop\_win\_localstorage.asp)     | Veb-brauzerda kalit/qiymat juftligini saqlashga imkon beradi. Ma'lumotlarni saqlash muddatisiz saqlaydi |
| [window.sessionStorage](https://www.w3schools.com/jsref/prop\_win\_sessionstorage.asp) | Veb-brauzerda kalit/qiymat juftlarini saqlashga imkon beradi. Bir seans uchun ma'lumotlarni saqlaydi    |
