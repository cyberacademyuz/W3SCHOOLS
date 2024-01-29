# CSS Backgroundlar

<figure><img src="../../.gitbook/assets/image (819).png" alt=""><figcaption></figcaption></figure>

### CSS bir nechta fonlar <a href="#css-bir-nechta-fonlar" id="css-bir-nechta-fonlar"></a>

CSSning `background-image` xususiyati elementga bir qancha orqafon rasmlar qo'shish imkonini beradi.

Orqafonga har xil rasmlar berishda ular vergul bilan ajratiladi va rasmlar bir-birining ustiga joylashtiriladi, birinchi rasm foydalanuvchiga eng yaqin rasm bo'ladi.

Quyidagi misolda ikkita background rasm bor, birinchi rasm gul (pastki va o'ng tomonga to'g'irlangan) va ikkinchi rasm qog'ozga o'xshash orqafon (tepa qismning chap burchagiga to'g'irlangan):

```
#example1 {
  background-image: url(img_flwr.gif), url(paper.gif);
  background-position: right bottom, left top;
  background-repeat: no-repeat, repeat;
}
```

Bir nechtalik background rasmlarni alohida bo'lgan background xususiyatlari (yuqoridagi kabi) yoki `background` xususiyati yordamida belgilash mumkin.

Quyidagi misolda `background` xususiyatidan foydalanilgan (natija yuqoridagi misol bilan bir xil bo'ladi):

```
#example1 {
  background: url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;
}
```

### CSS background-size <a href="#css-background-size" id="css-background-size"></a>

CSSning `background-size` xususiyati backgrounddagi rasmlarning o'lchamini o'zgartirish imkonini beradi.

Ol'cham, uzunlik birliklarida, foizlarda yoki ikkita `contain` va `cover` kalit so'zlaridan biri yordamida ko'rsatilishi mumkin.

Quyidagi misolda backgrounddagi rasm asl rasmdan ancha kichkina qilib o'zgartirilgan (**px**lar yordamida):

<figure><img src="../../.gitbook/assets/image (286).png" alt=""><figcaption></figcaption></figure>

Uning kodi:

```
#div1 {
  background: url(img_flower.jpg);
  background-size: 100px 80px;
  background-repeat: no-repeat;
}
```

Bu qiymatlardan tashqari `contain` va `cover` lardan ham foydalanish mumkin.

`contain` kalit so'zi background rasmni iloji boricha kattaroq qilib kengaytiradi (lekin uning kengligi ham, balandligi ham kontent maydoniga mos kelishi kerak). Shunday qilib, background image va  background position maydoniga qarab, backgroundga berilgan rasm backgroundning ba'zi joylarini qoplay olmasligi mumkin.

`cover` kalit so'zi backgrounddagi rasmni shunday o'lchaydiki, kontent maydoni backgrounddagi rasm bilan to'liq qoplanadi (uning kengligi ham, balandligi ham kontent maydoniga teng yoki undan yuqori bo'ladi). Shunday qilib, backgrounddagi rasmning ba'zi qismlari background positiob maydonida ko'rinmasligi mumkin.

Quyidagi misolda `contain` va `cover` ning farqlari amaliy tarzda ko'rsatilgan:

```
#div1 {
  background: url(img_flower.jpg);
  background-size: contain;
  background-repeat: no-repeat;
}

#div2 {
  background: url(img_flower.jpg);
  background-size: cover;
  background-repeat: no-repeat;
}
```

### Bir qancha background rasmlarning o'lchamini belgilash <a href="#bir-qancha-fon-rasmini-razmerini-belgilash" id="bir-qancha-fon-rasmini-razmerini-belgilash"></a>

`background-size` xususiyati bir nechtalik backgroundlar bilan ishlayotganda, background o'lchami uchun (vergul bilan ajratilgan ro'yxat yordamida) bir qancha qiymatlar qabul qiladi.

Quyidagi misolda har bir rasm uchun turlicha background o'lchamiga ega uchta background rasm ko'rsatilgan:

```
#example1 {
  background: url(img_tree.gif) left top no-repeat, url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;
  background-size: 50px, 130px, auto;
}
```

### To'liq o'lchamli background rasm <a href="#toliq-olchamli-fon-rasmi" id="toliq-olchamli-fon-rasmi"></a>

Endi websaytga har doim brauzerning butun oynasini qamrab oluvchi background rasm qo'shmoqchimiz&#x20;

Uning uchun quyidagi talablar bo'lishi kerak:

* Butun sahifani rasm bilan qamrab oling (bo'sh joysiz)
* Rasmni kerakligicha masshtablashtiring
* Rasmni sahifa o'rtasiga joylashtirsh
* Scrollbar paydo bo'lmasin

Buni qanday qilish quyidagi misolda ko'rsatilgan; `<html>` elementidan foydalaning (`<html>` elementi har doim kamida brauzer oynasining balandligida bo'ladi). Keyin uni fixed qiling va backgroundni o'rtaga olib keling. So'ngra uning o'lchamini `background-size` xususiyati orqali o'zgartiring:

```
html {
  background: url(img_man.jpg) no-repeat center fixed;
  background-size: cover;
}
```

### Hero rasm <a href="#geroy-rasm" id="geroy-rasm"></a>

Hero rasm (matnli katta rasm) yaratish va uni xohlagan joyga joylashtirish uchun `<div>` da turli `background` xususiyatlaridan foydalanishingiz mumkin.

```
.hero-image {
  background: url(img_man.jpg) no-repeat center;
  background-size: cover;
  height: 500px;
  position: relative;
}
```

### CSS background-origin xususiyati <a href="#css-background-origin-xususiyati" id="css-background-origin-xususiyati"></a>

CSS `background-origin` xususiyati background rasmni qayerda joylashganligini belgilaydi.

Xususiyat 3-ta qiymat qabul qiladi:

* border-box - background rasm chegaraning yuqori chap burchagidan boshlanadi
* padding-box - (standart) background rasm padding chetining yuqori chap burchagidan boshlanadi
* content-box - background rasm kontentning yuqori chap burchagidan boshlanadi

Quyidagi misol `background-origin` xususiyatini ko'rsatib beradi:

```
#example1 {
  border: 10px solid black;
  padding: 35px;
  background: url(img_flwr.gif);
  background-repeat: no-repeat;
  background-origin: content-box;
}
```

### CSS background-clip xususiyati <a href="#css-background-clip-xususiyati" id="css-background-clip-xususiyati"></a>

CSSning `background-clip` xususiyati backgroundning bo'yaladigan maydonini belgilaydi.

Xususiyat 3-ta qiymat qabul qiladi:

* border-box - (standart) orqafon borderning tashqi cheti bilan bo'yaladi
* padding-box - orqafon padding ning tashqi cheti bilan bo'yaladi
* content-box - orqafon kontent qutisidagina bo'yaladi

Quyida `background-clip` xususiyatining kodini keltiramiz:

```
#example1 {
  border: 10px dotted black;
  padding: 35px;
  background: yellow;
  background-clip: content-box;
}
```

### CSSning kengaytirilgan background xususiyatlari <a href="#css-kengaytirilgan-fon-xususiyatlari" id="css-kengaytirilgan-fon-xususiyatlari"></a>

| Xususiyat                                                                             | Ta'rif                                                                           |
| ------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| [background](https://www.w3schools.com/cssref/css3\_pr\_background.asp)               | Barcha fon xususiyatlarini bir deklaratsiyada keltirish mumkin bo'lgan xususiyat |
| [background-clip](https://www.w3schools.com/cssref/css3\_pr\_background-clip.asp)     | Fonning bo'yash maydonini belgilaydi                                             |
| [background-image](https://www.w3schools.com/cssref/pr\_background-image.asp)         | Element uchun bir yoki bir nechta fon rasmini belgilaydi                         |
| [background-origin](https://www.w3schools.com/cssref/css3\_pr\_background-origin.asp) | Fon rasm(lar)i qayerda joylashganligini belgilaydi                               |
| [background-size](https://www.w3schools.com/cssref/css3\_pr\_background-size.asp)     | Fon rasm(lar)ining hajmini belgilaydi                                            |
