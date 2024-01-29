# Vue Routing

{% hint style="success" %}
**Vue-da marshrutlash** Vue ilovasida harakatlanish uchun ishlatiladi va u mijoz tomonida (brauzerda) sahifani to'liq qayta yuklamasdan sodir bo'ladi, bu esa tezroq foydalanuvchi tajribasiga olib keladi.

**Marshrutlash** - ilgari [dinamik komponentlardan](https://www-w3schools-com.translate.goog/vue/vue\_dynamic-components.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) foydalanganimiz kabi navigatsiya qilish usuli .

**Marshrutlash** yordamida biz Vue ilovamizda kimnidir ma'lum bir joyga yo'naltirish uchun URL manzilidan foydalanishimiz mumkin.
{% endhint %}

### Dinamik komponent yordamida navigatsiya

Vue-da marshrutlashni tushunish uchun avvalo ikkita komponent o'rtasida almashish uchun dinamik komponentdan foydalanadigan dasturni ko'rib chiqaylik.

Biz tugmalar yordamida komponentlar o'rtasida almashishimiz mumkin:

{% code title="FoodItems.vue:" %}
```html
<template>
    <h1>Food!</h1>
    <p>I like most types of food.</p>
</template>
```
{% endcode %}

{% code title="AnimalCollection.vue:" %}
```html
<template>
    <h1>Animals!</h1>
    <p>I want to learn about at least one new animal every year.</p>
</template>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <p>Choose what part of this page you want to see:</p>
  <button @click="activeComp = 'animal-collection'">Animals</button>
  <button @click="activeComp = 'food-items'">Food</button><br>
  <div>
    <component :is="activeComp"></component>
  </div>
</template>

<script>
export default {
  data() {
      return {
        activeComp: ''
      }
    }
}
</script>

<style scoped>
  button {
    padding: 5px;
    margin: 10px;
  }
  div {
    border: dashed black 1px;
    padding: 20px;
    margin: 10px;
    display: inline-block;
  }
</style>
```
{% endcode %}

### Dinamik komponentdan marshrutlashgacha

Biz Vue bilan SPA (Yagona sahifali ilovalar) yaratamiz, ya'ni bizning ilovamiz faqat bitta \*.html faylini o'z ichiga oladi. Bu shuni anglatadiki, biz odamlarni boshqa \*.html fayllarga yo'naltira olmaymiz va ularga bizning sahifamizda turli xil kontentni ko'rsata olmaymiz.

Yuqoridagi misolda biz sahifadagi turli kontentlar orasida harakat qilishimiz mumkin, lekin biz boshqa birovga sahifaga manzil bera olmaymiz, shunda ular to'g'ridan-to'g'ri oziq-ovqat haqida bo'limga kirishadi, lekin marshrutlash orqali biz buni qila olamiz.

Marshrut to'g'ri sozlangan bo'lsa, Vue ilovasini URL manziliga kengaytmali ochsangiz, masalan, "/food-items" kabi, siz to'g'ridan-to'g'ri oziq-ovqat tarkibiga kirasiz.

#### Vue Router kutubxonasini o'rnating

Mashinangizda Vue-da marshrutlashdan foydalanish uchun terminaldan foydalanib loyiha papkangizga Vue Router kutubxonasini o'rnating:

```bash
npm install vue-router@4
```

#### main.js-ni yangilang

Marshrutlashdan foydalanish uchun biz router yaratishimiz kerak va buni main.js faylida qilamiz.

{% code title="main.js:" lineNumbers="true" %}
```js
import { createApp } from 'vue'
import { createRouter, createWebHistory } from 'vue-router'

import App from './App.vue'
import FoodItems from './components/FoodItems.vue'
import AnimalCollection from './components/AnimalCollection.vue'

const router = createRouter({
    history: createWebHistory(),
    routes: [
        { path: '/animals', component: AnimalCollection },
        { path: '/food', component: FoodItems },
    ]
});

const app = createApp(App)

app.use(router);
app.component('food-items', FoodItems);
app.component('animal-collection', AnimalCollection);

app.mount('#app'
```
{% endcode %}

Router funksiyasini qo'shish uchun 2, 8-14 va 18-qatorlar qo'shiladi.

19-20-qatorlar o'chiriladi, chunki komponentlar 11-12-qatorlarga router orqali allaqachon kiritilgan.

Endi biz, masalan, original URL manzilining oxiriga "/hayvanlar" qo'shilsa, "AnimalCollection" komponentini ochishi mumkin bo'lgan yo'riqnoma yaratdik, lekin komponentni qo'shganimizda keyingi bo'limgacha ishlamaydi `<router-view>`. Router shuningdek, veb-tarixni kuzatib boradi, shunda siz odatda URL-manzil yonidagi veb-brauzerning yuqori chap burchagida joylashgan strelkalar yordamida tarixda oldinga va orqaga qaytishingiz mumkin.

#### \<router-view> komponentidan foydalaning

Bizning sahifamizdagi tarkibni yangi yo'riqnoma bilan o'zgartirish uchun biz oldingi misoldagi dinamik komponentni olib tashlashimiz va uning `<router-view>`o'rniga komponentdan foydalanishimiz kerak.

{% code title="App.vue:" %}
```html
<template>
  <p>Choose what part of this page you want to see:</p>
  <button @click="activeComp = 'animal-collection'">Animals</button>
  <button @click="activeComp = 'food-items'">Food</button><br>
  <div>
    <router-view></router-view>
    <component :is="activeComp"></component>
  </div>
</template>
 
```
{% endcode %}

Agar siz kompyuteringizda yuqoridagi o'zgarishlarni amalga oshirgan bo'lsangiz, brauzerdagi loyiha sahifangizning URL manziliga "/food" ni qo'shishingiz mumkin va sahifa oziq-ovqat tarkibini ko'rsatish uchun yangilanishi kerak, masalan:

<figure><img src="https://www.w3schools.com/vue/img_screenshot_router.png" alt=""><figcaption></figcaption></figure>

#### \<router-link> komponentidan foydalaning

Biz tugmachalarni `<router-link>`komponent bilan almashtirishimiz mumkin, chunki u router bilan yaxshiroq ishlaydi.

Biz endi "activeComp" ma'lumotlar xususiyatiga muhtoj emasmiz, shuning uchun biz uni o'chirib tashlashimiz mumkin va biz butun `<script>`tegni o'chirib tashlashimiz mumkin, chunki u bo'sh.

{% code title="App.vue:" %}
```html
<template>
  <p>Choose what part of this page you want to see:</p>
  <router-link to="/animals">Animals</router-link>
  <router-link to="/food">Food</router-link><br>
  <div>
    <router-view></router-view>
  </div>
</template>

<script></script>
```
{% endcode %}

#### \<router-link> komponentiga uslub

Komponent `<router-link>`tegga ko'rsatiladi `<a>`. Brauzerdagi elementni sichqonchaning o'ng tugmasi bilan bosib, tekshirib ko'rsak, buni ko'rishimiz mumkin:

<figure><img src="https://www.w3schools.com/vue/img_router-link-render.png" alt=""><figcaption></figcaption></figure>

Yuqoridagi skrinshotda ko'rib turganingizdek, Vue qaysi komponent faol ekanligini ham kuzatib boradi va faol komponentga "router-link-active" sinfini beradi ( `<router-link>`bu endi tegga ko'rsatiladi `<a>`).

`<router-link>`Qaysi komponent faol ekanligini ta'kidlash uchun uslub berish uchun yuqoridagi ma'lumotlardan foydalanishimiz mumkin:

{% code title="App.vue:" %}
```html
<template>
  <p>Choose what part of this page you want to see:</p>
  <router-link to="/animals">Animals</router-link>
  <router-link to="/food">Food</router-link><br>
  <div>
    <router-view></router-view>
  </div>
</template>

<style scoped>
  a {
    display: inline-block;
    background-color: black;
    border: solid 1px black;
    color: white;
    padding: 5px;
    margin: 10px;
  }
  a:hover,
  a.router-link-active {
    background-color: rgb(110, 79, 13);
  }
  div {
    border: dashed black 1px;
    padding: 20px;
    margin: 10px;
    display: inline-block;
  }
</style> 
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Yuqoridagi misolda URL manzili yangilanmagan, lekin agar siz buni o'zingizning kompyuteringizda qilsangiz, URL manzili yangilanadi. Yuqoridagi misol, URL manzili yangilanmagan bo'lsa ham ishlaydi, chunki marshrutlash Vue-dagi router tomonidan ichki nazorat qilinadi.
{% endhint %}
