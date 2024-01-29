# Audio

HTMLning `<audio>` elementi veb-sahifadagi audio faylni ijro etish uchun ishlatiladi.

### \<audio> elementi

HTML-da audio faylni ijro etish uchun `<audio>` elementidan foydalaning:

```
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>
```

### HTML Audio - U qanday ishlaydi

`controls` atributi  ijro etish, to'xtatib turish va ovoz balandligi kabi audio boshqaruvlarini qo'shadi.

`<source>` elementi brauzer tanlashi mumkin bo'lgan muqobil audio fayllarni belgilash imkonini beradi. Brauzer birinchi berilgan formatdan foydalanadi.

`<audio>`va `</audio>` teglari orasidagi matn faqat `<audio>` elementini qo'llab-quvvatlamaydigan brauzerlarda ko'rsatiladi.

### \<audio> Avtomatik ijro

Audio faylni avtomatik tarzda ishga tushirish uchun `autoplay` atributidan foydalaning:

```
<audio controls autoplay>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>
```

{% hint style="warning" %}
**Eslatma:** Chromium brauzerlari ko'p hollarda avtomatik ijroga ruxsat bermaydi. Biroq, ovossiz tarzda avtomatik ijro qilishga har doim ruxsat beriladi.
{% endhint %}

Audio faylingiz avtomatik ijro qilinishi uchun `autoplay`dan keyin `muted`ni qoʻshing:

```
<audio controls autoplay muted>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>
```

### Brauzerni qo'llab-quvvatlashi

Jadvaldagi raqamlar `<audio>` elementini qo'llab-quvvatlaydigan ilk brauzer versiyasini ko'rsatadi.

| Element  | Chrome | Edge | Firefox | Safari | Opera |
| -------- | ------ | ---- | ------- | ------ | ----- |
| \<audio> | 4.0    | 9.0  | 3.5     | 4.0    | 10.5  |

### HTMLning audio formatlari

Uchta qo'llab-quvvatlanadigan audio formatlari mavjud: MP3, WAV va OGG. Turli formatlar uchun brauzerni qo'llab-quvvatlash:&#x20;

| Browser | MP3 | WAV | OGG  |
| ------- | --- | --- | ---- |
| Edge/IE | HA  | HA  | HA   |
| Chrome  | HA  | HA  | HA   |
| Firefox | HA  | HA  | HA   |
| Safari  | HA  | HA  | YO'Q |
| Opera   | HA  | HA  | HA   |

\* Edge 79 dan boshlab

### HTML Audio - Media turlari

| Fayl formati | Media turi |
| ------------ | ---------- |
| MP3          | audio/mpeg |
| OGG          | audio/ogg  |
| WAV          | audio/wav  |

### HTML Audio - metodlar, xususiyatlar va hodisalar

HTML DOM `<audio>` elementi uchun metodlar, xususiyatlar va hodisalarni belgilaydi.

Bu sizga audiolarni yuklash, ijro etish va pauza qilish, shuningdek, davomiylik va ovoz balandligini boshqarish imkonini beradi.

Bundan tashqari, audio ijro etilishi boshlanganda, to'xtatilganda va hokazolarda sizga xabar beradigan DOM hodisalari mavjud.

To'liq DOM ma'lumotnomasi uchun bizning HTML Audio/Video DOM ma'lumotnomamizga o'ting .

### HTML audio teglar

| Tag                                                                                                                                       | Ta'rif                                                                                  |
| ----------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| [\<audio>](https://www-w3schools-com.translate.goog/tags/tag\_audio.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Audio tarkibini belgilaydi                                                              |
| [\<source>](https://www-w3schools-com.translate.goog/tags/tag\_source.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Media elementlari uchun bir nechta resurslarni belgilaydi, masalan \<video> va \<audio> |

