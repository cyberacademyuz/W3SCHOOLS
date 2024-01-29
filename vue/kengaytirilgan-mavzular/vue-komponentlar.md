# Vue Komponentlar

{% hint style="success" %}
**Vue-dagi komponentlar** bizga veb-sahifamizni ishlash uchun qulay bo'lgan kichikroq qismlarga ajratish imkonini beradi.

Biz Vue komponenti bilan veb-sahifaning qolgan qismidan alohida, o‘z mazmuni va mantig‘i bilan ishlashimiz mumkin.

Veb-sahifa ko'pincha Vue komponentlaridan iborat.
{% endhint %}

### Komponentlar nima ?

Komponentlar qayta foydalanish mumkin bo'lgan va o'z-o'zidan tuzilgan kod bo'laklari bo'lib, ular foydalanuvchi interfeysining ma'lum bir qismini qamrab oladi, shuning uchun biz Vue ilovalarini kengaytiriladigan va texnik xizmat ko'rsatishni osonlashtira olamiz.

Biz Vue-da komponentlarni o'zimiz yaratishimiz yoki keyinroq bilib oladigan o'rnatilgan komponentlardan foydalanishimiz mumkin, masalan [`<Teleport>`](https://www-w3schools-com.translate.goog/vue/vue\_teleport.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)yoki kabi [`<KeepAlive>`](https://www-w3schools-com.translate.goog/vue/vue\_dynamic-components.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp#KeepAlive). Bu erda biz o'zimiz ishlab chiqaradigan komponentlarga e'tibor qaratamiz.

### Komponent yaratish

Vue-dagi komponentlar juda kuchli vositadir, chunki u bizning veb-sahifamizni yanada kengaytirilishiga va kattaroq loyihalarni boshqarishni osonlashtiradi.

Keling, komponent yarataylik va uni loyihamizga qo'shamiz.

1. `components`Jild ichida yangi papka yarating `src`.
2. Jild ichida `components`yangi fayl yarating `FoodItem.vue`. Komponentlarni PascalCase nomlash konventsiyasi bo'yicha, bo'sh joysiz va barcha yangi so'zlar bosh harf bilan boshlanadigan birinchi so'z bilan nomlash odatiy holdir.
3. `FoodItem.vue`Fayl quyidagicha ko'rinishiga ishonch hosil qiling :

Komponent ichidagi kod `FoodItem.vue`:

```html
<template>
  <div>
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Apples',
      message: 'I like apples'
    }
  }
};
</script>

<style></style>
```

Yuqoridagi misolda ko'rib turganingizdek, komponentlar ham xuddi bizning asosiy faylimiz kabi , `<template>`va `<script>`teglardan iborat .`<style>App.vue`

### Komponentni qo'shish

`<script>`Yuqoridagi misoldagi teg bilan boshlanganiga e'tibor bering `export default`. Bu ma'lumotlar xususiyatlarini o'z ichiga olgan ob'ektni boshqa faylga qabul qilish yoki import qilish mumkinligini anglatadi. `FoodItem.vue`Biz bundan komponentni fayl bilan import qilish orqali mavjud loyihamizga kiritish uchun foydalanamiz `main.js`.

Birinchidan, oxirgi qatorni asl faylingizdagi ikki qatorga qayta yozing `main.js`:

{% code title="main.js:" %}
```jsx
import { createApp } from 'vue'

import App from './App.vue'

const app = createApp(App)
app.mount('#app')
```
{% endcode %}

Endi `FoodItem.vue`faylingizga 4 va 7 qatorlarni qo'shib komponentni qo'shing `main.js`:

{% code title="main.js:" %}
```jsx
import { createApp } from 'vue'

import App from './App.vue'
import FoodItem from './components/FoodItem.vue'

const app = createApp(App)
app.component('food-item', FoodItem)
app.mount('#app')
```
{% endcode %}

7-qatorda komponent qo'shiladi, shunda biz uni faylimizdagi teg `<food-item/>`ichida maxsus teg sifatida ishlatishimiz mumkin :`<template>App.vue`

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <food-item/>
  <food-item/>
  <food-item/>
</template>

<script></script>

<style></style> 
 
 
```
{% endcode %}

`<style>`Va keling, fayldagi teg ichiga uslub qo'shamiz `App.vue`. Ishlab chiqish serveri ishlayotganiga ishonch hosil qiling va natijani tekshiring.

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <food-item/>
  <food-item/>
  <food-item/>
</template>

<script></script>

<style>
  #app > div {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: lightgreen;
  }
</style> 
```
{% endcode %}

**Rivojlanish rejimi:** Vue loyihalaringiz bilan ishlaganda, terminalda quyidagi kod qatorini ishga tushirish orqali loyihangizni har doim ishlab chiqish rejimida saqlash foydalidir:

```
npm run dev
```

### individual komponentlar

Vue-da komponentlar bilan ishlashda juda foydali va kuchli xususiyat shundan iboratki, biz oddiy JavaScript-da qilganimizdek, noyob identifikatorlarga ega elementlarni belgilamasdan turib, ularni individual tarzda bajarishimiz mumkin. Vue avtomatik ravishda har bir komponentga alohida e'tibor qaratadi.

`<div>`Keling , elementlarni bosganimizda hisobga olinsin .

Bizning asosiy dastur faylimizga qo'shilgan yagona narsa `App.vue`- bu CSS-da kursor kursorni ko'tarayotganda ishora qilayotgan qo'lga o'xshab, qandaydir bosish funksiyasi mavjudligini anglatadi.

CSS kodi tegga `<style>`qo'shildi `App.vue`:

```css
#app > div:hover {
  cursor: pointer;
}
```

Komponent faylimizga ma'lumotlar xususiyatini , elementga bosish tinglovchisini , hisoblagichni oshirish uchun bosish sodir bo'lganda ishga tushirish usulini va hisoblashni ko'rsatish uchun matn interpolyatsiyasini `FoodItem.vue`qo'shishimiz kerak .`count<div>{{}}`

{% code title="FoodItem.vue:" %}
```html
<template>
  <div v-on:click="countClicks">
    <h2>{{ name }}</h2>  
    <p>{{ message }}</p>
    <p id="red">You have clicked me {{ clicks }} times.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Apples',
      message: 'I like apples',
      clicks: 0
    }
  },
  methods: {
    countClicks() {
      this.clicks++;
    }
  }
}
</script>

<style>
  #red {
    font-weight: bold ;
    color: rgb(144, 12, 12);
  }
</style>
```
{% endcode %}

`<div>`Har bir element uchun alohida hisoblashni boshqarish uchun Vue uchun noyob identifikatorlarni belgilashimiz yoki qo'shimcha ishlarni bajarishimiz shart emas , Vue buni faqat avtomatik ravishda bajaradi.

Ammo turli xil hisoblagich qiymatlari bundan mustasno, elementlarning mazmuni `<div>`hali ham bir xil. Keyingi sahifada biz komponentlar haqida ko'proq ma'lumotga ega bo'lamiz, shunda biz tarkibiy qismlardan yanada mantiqiyroq foydalanishimiz mumkin. Misol uchun, har bir elementda har xil turdagi oziq-ovqatlarni ko'rsatish mantiqiyroq bo'ladi `<div>`.
