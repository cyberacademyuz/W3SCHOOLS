# Vue Nega, qanday va sozlash

{% hint style="success" %}
Vue loyihamiz uchun \*.vue fayllaridan foydalanish mantiqiy, chunki:

* andozalar va komponentlardan foydalangan holda yirik loyihalarni boshqarish osonroq bo'ladi.
* Biz loyihamizni https protokoli orqali ko'rishimiz va sinab ko'rishimiz mumkin, xuddi foydalanuvchilar sahifani ko'radi.
* o'zgarishlar saqlanganida sahifa qayta yuklanmasdan darhol yangilanadi.
* Vue-da haqiqiy veb-sahifalar shunday qurilgan.
* ishlab chiquvchilar shunday ishlaydi.
{% endhint %}

### Nega ?

Oldingi sahifada Vue-dagi shablonlar va komponentlar haqida ko'rganimizdek, endi ishlashning boshqa usullariga ehtiyoj bor, chunki biz quyidagilarni xohlaymiz:

* kattaroq loyihalarga ega
* Vue bilan bog'liq barcha kodlarni bir joyda to'plang
* Vue-da komponentlardan foydalaning (biz bu haqda tez orada kelamiz)
* muharrirda ta'kidlash va avtomatik to'ldirishni qo'llab-quvvatlashga ega
* brauzerni avtomatik yangilash

Va bularning barchasini amalga oshirish uchun biz \*.vue fayllariga o'tamiz.

### Qanaqasiga?

SFC (Yagona fayl komponentlari) yoki \*.vue fayllari bilan ishlash osonroq, lekin to'g'ridan-to'g'ri brauzerda ishlay olmaydi, shuning uchun biz \*.vue fayllarimizni \*.html, \*.css va formatlarga kompilyatsiya qilish uchun kompyuterimizni sozlashimiz kerak. \*.js fayllari brauzer Vue ilovamizni ishga tushirishi uchun.

Veb-sahifamizni SFClar asosida yaratish uchun biz Vite deb nomlangan dasturni yaratish vositasi sifatida foydalanamiz va kodimizni Vue 3 til xususiyatlari uchun Volar kengaytmasi bilan VS Code muharririga yozamiz.

### Sozlash; o'rnatish

Vue SFC ilovalarini kompyuteringizda ishga tushirish uchun kerak bo'lgan narsalarni o'rnatish uchun quyidagi uchta bosqichni bajaring.

1.  **"VS Code" muharriri**

    Vue loyihalari uchun ishlatilishi mumkin bo'lgan juda ko'p turli xil muharrirlar mavjud. Biz VS Code muharriridan foydalanamiz. [VS kodini yuklab oling](https://translate.google.com/website?sl=de\&tl=uz\&hl=ru\&client=webapp\&u=https://code.visualstudio.com/download) va o'rnating.



    ***

    <figure><img src="https://www.w3schools.com/vue/img_download_vscode.png" alt=""><figcaption></figcaption></figure>
2.  **VS kodi "Volar" kengaytmasi**

    Tahrirlovchida \*.vue fayllari bilan ajratib ko'rsatish va avtomatik to'ldirish uchun VS kodini oching, chap tomondagi "Kengaytmalar" ga o'ting. "Volar" ni qidiring va eng ko'p yuklangan kengaytmani va "Vue 3 uchun tilni qo'llab-quvvatlash" tavsifini o'rnating.



    ***

    <figure><img src="https://www.w3schools.com/vue/img_vsCode_volar-extension_3.png" alt=""><figcaption></figcaption></figure>
3.  **Node.js**

    [Node.js](https://translate.google.com/website?sl=de\&tl=uz\&hl=ru\&client=webapp\&u=https://nodejs.org/en/) ning so'nggi versiyasini yuklab oling va o'rnating , chunki Vue qurish vositasi "Vite" buning ustiga ishlaydi.

    Node.js ochiq manbali server tomonidagi JavaScript ish vaqti muhitidir.



    ***

    <figure><img src="https://www.w3schools.com/vue/img_download_nodejs.png" alt=""><figcaption></figcaption></figure>

### Standart misol loyihasini yarating

Kompyuteringizda standart Vue misol loyihasini yaratish uchun quyidagi amallarni bajaring.

4.  Kompyuteringizda Vue loyihalaringiz uchun papka yarating.

    ***
5.  VS Code-da menyudan Terminal -> New Terminal ni tanlab terminalni oching:

    ![Yangi terminal skrinshoti](https://www.w3schools.com/vue/img\_vsCode\_newTerminal.png)

    ***
6.  , , `cd <folder-name>`( Mac/Linux) va (Windows) kabi buyruqlar yordamida hozirgina yaratilgan Vue jildiga o'tish uchun terminaldan foydalaning . Agar siz terminalda buyruqlar yozish bilan tanish bo'lmasangiz, Buyruqlar qatori interfeysi (CLI) ga [bu yerda](https://www-w3schools-com.translate.goog/whatis/whatis\_cli.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) kirishimizga qarang .`cd ..lsdir`

    ***
7. Terminaldagi Vue jildingizga o'tganingizdan so'ng, quyidagilarni yozing:

```
npm init vue@latest
```

8.  Birinchi loyihangizni "firstsfc" nomi bilan yarating:\


    <figure><img src="https://www.w3schools.com/vue/img_projectName_firstsfc.png" alt=""><figcaption></figcaption></figure>
9.  Barcha variantlarga "Yo'q" deb javob bering:



    ***

    <figure><img src="https://www.w3schools.com/vue/img_noToAll.png" alt="" width="375"><figcaption></figcaption></figure>
10. Endi siz terminalda buni taqdim etishingiz kerak:

    ![](https://www.w3schools.com/vue/img\_firstsfc\_done.png)

    ***
11. Endi biz yuqorida tavsiya etilgan buyruqlarni bajaramiz.

    Katalogni "firstsfc" jildidagi yangi loyihangizga o'zgartirish uchun ushbu buyruqni bajaring:

```
cd firstsfc
```

12. Vue loyihasi ishlashi uchun barcha kerakli bog'liqliklarni o'rnating:

```
npm install
```

13. Rivojlanish serverini ishga tushiring:

```
npm run dev
```

14. Endi terminal oynasi quyidagicha ko'rinishi kerak:

<figure><img src="https://www.w3schools.com/vue/img_runDev.png" alt=""><figcaption></figcaption></figure>

Va sizning brauzeringiz namunaviy loyihani avtomatik ravishda ochishi kerak:

<figure><img src="https://www.w3schools.com/vue/img_vue_myfirst.png" alt=""><figcaption></figcaption></figure>

Agar siz brauzerda loyiha namunasini topa olmasangiz, terminaldagi havoladan foydalaning. Terminal oynasida topilgan havola yuqoridagi skrinshotdagi manzildan boshqa manzilga ega bo'lishi mumkin.

Endi misol loyihasi kompyuteringizda Vite qurish vositasi tomonidan ishlab chiqish rejimida ishlamoqda.

### Loyiha fayllari

Avtomatik ravishda yaratilgan namunaviy loyiha ko'plab fayllarni o'z ichiga oladi va biz ulardan bir nechtasini tezda ko'rib chiqamiz.

#### main.js

VS Code muharririda Vue loyihangizga o'ting, "src" papkasida "main.js" faylini toping:

<figure><img src="https://www.w3schools.com/vue/img_mainjs.png" alt=""><figcaption></figcaption></figure>

"main.js" Vite-ga "App.vue" fayli asosida Vue loyihasini qanday yaratishni aytadi. Bu brauzerga Vue kodimizni qanday ishga tushirishni va Vue misolini tegga qanday o'rnatganimizni aytib berish uchun avval skript yorlig'i bilan CDN havolasini berganimizga o'xshaydi `<div id="app">`.

#### App.vue

Xuddi shu misol loyiha papkasida "App.vue" faylini toping va uni oching. Boshqa barcha \*.vue fayllari singari, "App.vue" ham uchta qismdan iborat: `<script>`qism, `<template>`qism va `<style>`qism.

{% code title="App.vue:" %}
```html
<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
```
{% endcode %}

"App.vue" ning skript qismida ko'rib turganingizdek, boshqa \*.vue fayllari nazarda tutilgan: ular "komponentlar" va "komponentlar" jildida joylashgan. Agar siz "App.vue" faylining "shablon" qismini ko'rib chiqsangiz, oddiy HTML teglari bo'lmagan teglarni ko'rishingiz mumkin: `<HelloWorld>`va `<TheWelcome>`. Komponentlar shunday nomlanadi. Komponentlar ilova ichidagi ilovalarga o‘xshaydi. Tez orada komponentlar haqida ko‘proq bilib olamiz.
