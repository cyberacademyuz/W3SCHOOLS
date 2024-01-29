# CSS Transitionlar

### CSS Transitionlar <a href="#css-transitionlar" id="css-transitionlar"></a>

CSS transitionlar xususiyat qiymatlarini ma'lum vaqt davomida bir tekisda o'zgartirish imkonini beradi.

**CSSning transition effektini ko'rish uchun sichqonchani quyidagi element ustiga olib boring:**

![](<../../.gitbook/assets/image (267).png>)

Ushbu bo'limda quyidagi xususiyatlar haqida bilib olasiz:

* `transition`
* `transition-delay`
* `transition-duration`
* `transition-property`
* `transition-timing-function`

### Brauzerning qo'llab quvvatlashi <a href="#brauzer-qollab-quvvatlashi" id="brauzer-qollab-quvvatlashi"></a>

Jadvaldagi raqamlar xususiyatni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Xususiyat                  | Chrome | Edge | Firefox | Safari | Opera |
| -------------------------- | ------ | ---- | ------- | ------ | ----- |
| transition                 | 26.0   | 10.0 | 16.0    | 6.1    | 12.1  |
| transition-delay           | 26.0   | 10.0 | 16.0    | 6.1    | 12.1  |
| transition-duration        | 26.0   | 10.0 | 16.0    | 6.1    | 12.1  |
| transition-property        | 26.0   | 10.0 | 16.0    | 6.1    | 12.1  |
| transition-timing-function | 26.0   | 10.0 | 16.0    | 6.1    | 12.1  |

### CSS Transitiondan qanday foydalaniladi ? <a href="#css-transitiondan-qanday-foydalaniladi" id="css-transitiondan-qanday-foydalaniladi"></a>

Transition effektini yaratish uchun ikkita narsani belgilashingiz kerak:

* Effektga qo'shiladigan CSS xususiyatlari
* Uning davomiyligi

**Eslatma**: Agar davomiylik parametri berilmagan bo'lsa, transition ning hech qanday ta'siri bo'lmaydi, chunki standart qiymat 0 hisoblanadi.

Quyidagi misolda 100px \* 100px-li qizil `<div>` elementi koʻrsatilgan. `<div>` elementida `width` xususiyati uchun 2 soniya davomiylik va transition effekti ham belgilangan:

```
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s;
}
```

Belgilangan CSS xususiyati (width) qiymatni o'zgartirganda, transition effekti boshlanadi.

Endi foydalanuvchi `<div>` elementi ustiga sichqonchani kursorini olib borganida width xususiyati uchun yangi qiymat belgilanadi:

```
 div:hover {
  width: 300px;
}
```

E'tibor bering, kursor elementdan tashqariga chiqganida, u asta-sekin asl holatiga qaytmoqda.

### Bir nechta xususiyat qiymatlarini o'zgartirish <a href="#bir-nechta-xususiyat-qiymatlarini-ozgartirish" id="bir-nechta-xususiyat-qiymatlarini-ozgartirish"></a>

Quyidagi misolda `width` va `height` xususiyatiga transition effekti qoʻshilgan, uning davomiyligi width uchun 2 soniya va height uchun 4 soniya qilingan:

```
div {
  transition: width 2s, height 4s;
}
```

### Transitionning curve tezligini belgilash <a href="#transition-tezligi-curve-chizigini-belgilash" id="transition-tezligi-curve-chizigini-belgilash"></a>

`transition-timing-function` xususiyati transition effektining curve tezligini belgilaydi.

`transition-timing-function` xususiyati quyidagi qiymatlarga ega bo'lishi mumkin:

* `ease` - sekin boshlanib, keyin tezlashadi va ohirida sekin to'xtaydigan transition effektini beradi (bu standart)
* `linear` - boshidan oxirigacha bir xil tezlikda transition effektini beradi
* `ease-in` - sekin boshlanadigan transition effektini beradi
* `ease-out` - sekin tugaydigan transition effektini beradi
* `ease-in-out` - sekin boshlanib va sekin tugaydigan transition effektini beradi
* `cubic-bezier(n,n,n,n)` - cubic-bezier funksiyasi o'zingiz istagan qiymatlarni berish imkonini beradi

Quyidagi misolda foydalanish mumkin bo'lgan har xil curve tezliklari  ko'rsatilgan:

```
#div1 {transition-timing-function: linear;}
#div2 {transition-timing-function: ease;}
#div3 {transition-timing-function: ease-in;}
#div4 {transition-timing-function: ease-out;}
#div5 {transition-timing-function: ease-in-out;}
```

### Transition effektni ushlab turish <a href="#transition-effektni-kechiktirish" id="transition-effektni-kechiktirish"></a>

`transition-delay` xususiyati transition effekti boshlanishini ushlasb turishni (sekundlarda) belgilaydi.

Quyidagi misolda boshlashdan oldin 1 soniya kutib turiladi:

```
div {
  transition-delay: 1s;
}
```

### Transition + Transform <a href="#transition-transform" id="transition-transform"></a>

Quyidagi misolda transformatsiyaga transition effekti qo'shiladi:

```
div {
  transition: width 2s, height 2s, transform 2s;
}
```

### Transitionga ko'proq misollar <a href="#koplab-transition-misollar" id="koplab-transition-misollar"></a>

CSSning `transition` xususiyatlari alohida berilishi mumkin, masalan:

```
div {
  transition-property: width;
  transition-duration: 2s;
  transition-timing-function: linear;
  transition-delay: 1s;
}
```

yoki qisqa `transition` xususiyati orqali berilishi mumkin:

```
 div {
  transition: width 2s linear 1s;
}
```

### CSSning transition xususiyatlari <a href="#css-transition-xususiyatlari" id="css-transition-xususiyatlari"></a>

Quyidagi jadvalda CSSning barcha `transition` xususiyatlari ko'rsatilgan:

| Xususiyat                                                                                               | Ta'rif                                                                                            |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| [transition](https://www.w3schools.com/cssref/css3\_pr\_transition.asp)                                 | To'rtta transition xususiyatini bitta xususiyatga o'rnatish uchun qisqartma transition xususiyati |
| [transition-delay](https://www.w3schools.com/cssref/css3\_pr\_transition-delay.asp)                     | Transition effekti uchun kechikishni (soniyalarda) belgilaydi                                     |
| [transition-duration](https://www.w3schools.com/cssref/css3\_pr\_transition-duration.asp)               | Transition effekti necha soniya yoki millisekundda bajarilishini belgilaydi                       |
| [transition-property](https://www.w3schools.com/cssref/css3\_pr\_transition-property.asp)               | Transition effekti uchun CSS xususiyati nomini belgilaydi                                         |
| [transition-timing-function](https://www.w3schools.com/cssref/css3\_pr\_transition-timing-function.asp) | Transition effektining tezlik curve chizig'ini belgilaydi                                         |
