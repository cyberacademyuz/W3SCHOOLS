# Video

HTMLning `<video>` elementi veb-sahifada videoni ko'rsatish uchun ishlatiladi.

[Big Buck Bunny](https://translate.google.com/website?sl=ru\&tl=uz\&hl=en\&client=webapp\&u=https://www.bigbuckbunny.org/) ning odobi:



### \<video> elementi

Videoni HTMLda ko'rsatish uchun `<video>` elementidan foydalaning:

```
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>
```

### U qanday ishlaydi

`controls` atributi videoni o'qish, to'xtatib turish va ovoz balandligi kabi video boshqaruvlarini qo'shadi.

Har doim `width` va `height` atributlarni kiritish yaxshi hisoblanadi. Agar balandlik va kenglik o'rnatilmagan bo'lsa, video yuklanayotganda sahifa miltillashi mumkin.

`<source>` elementi brauzer tanlashi mumkin bo'lgan muqobil video fayllarni belgilash imkonini beradi. Brauzer birinchi ko'rsatilgan formatdan foydalanadi.

`<video>`va `</video>` teglari orasidagi matn faqat `<video>` elementini qo'llab-quvvatlamaydigan brauzerlarda ko'rsatiladi.

### &#x20;\<video>  Avtomatik ijro

Videoni avtomatik tarda boshlash uchun `autoplay` atributidan foydalaning:

```
<video width="320" height="240" autoplay>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>
```

{% hint style="warning" %}
**Eslatma:** Chromium brauzerlari ko'p hollarda avtomatik ijroga ruxsat bermaydi. Biroq, `muted autoplay` ga har doim ruxsat beriladi.
{% endhint %}

Videongiz avtomatik tarzda ijro etilishni boshlashi uchun `autoplay` dan keyin `muted` ni qoʻshing:

```
<video width="320" height="240" autoplay muted>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>
```

### Brauzerni qo'llab-quvvatlashi

Jadvaldagi raqamlar `<video>` elementini to'liq qo'llab-quvvatlaydigan brauzerlarning ilk versiyasini ko'rsatadi.

| Element  | Chrome | Edge | Firefox | Safari | Opera |
| -------- | ------ | ---- | ------- | ------ | ----- |
| \<video> | 4.0    | 9.0  | 3.5     | 4.0    | 10.5  |

### HTML video formatlari

Uchta qo'llab-quvvatlanadigan video formatlari mavjud: MP4, WebM va Ogg. Ushbu formatlar uchun brauzerni qo'llab-quvvatlashi:

| Brauzer | MP4 | WebM | Ogg  |
| ------- | --- | ---- | ---- |
| Edge    | Ha  | Ha   | Ha   |
| Chrome  | Ha  | Ha   | Ha   |
| Firefox | Ha  | Ha   | Ha   |
| Safari  | Ha  | Ha   | Yo'q |
| Opera   | Ha  | Ha   | Ha   |

### HTML video - Media turlari

| Fayl formati | Media turi |
| ------------ | ---------- |
| MP4          | video/mp4  |
| WebM         | video/webm |
| Ogg          | video/ogg  |

### HTML video - metodlar, xususiyatlar va hodisalar

HTML DOM `<video>` elementi uchun metodlar, xususiyatlar va hodisalar belgilaydi.

Bu sizga videolarni yuklash, ijro etish va to‘xtatib turish, shuningdek, davomiylik va ovoz balandligini sozlash imkonini beradi.

Shuningdek, videoni ijro etish boshlaganda, to'xtatilganda va hokazolarda sizni xabardor qiladigan DOM hodisalari ham mavjud.

#### Misol: JavaScript-dan foydalanish

[Video Big Buck Bunny](https://translate.google.com/website?sl=ru\&tl=uz\&hl=en\&client=webapp\&u=https://www.bigbuckbunny.org/) tomonidan taqdim etilgan.

Batafsil DOM ma'lumotnomasi ko'rish uchun bizning HTML Audio/Video DOM ma'lumotnoma sahifamizga o'ting.

### HTMLning video teglar

| Teg                                                                                                                                       | Ta'rif                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| [\<video>](https://www-w3schools-com.translate.goog/tags/tag\_video.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Videoni yoki filmni belgilaydi                                                           |
| [\<source>](https://www-w3schools-com.translate.goog/tags/tag\_source.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Media elementlari uchun bir nechta resourcelarni belgilaydi, masalan \<vide> va \<audio> |
| [\<track>](https://www-w3schools-com.translate.goog/tags/tag\_track.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Media pleerlarida matnli subtitlelarni belgilaydi                                        |
