# Vue Provide/inject

{% hint style="success" %}
**Vue-da Provide/Inject** bir komponentdan boshqa komponentlarga, ayniqsa yirik loyihalarda ma'lumotlarni taqdim etish uchun ishlatiladi.

**Ta'minlash** boshqa komponentlar uchun ma'lumotlarni taqdim etadi.

**Inject** taqdim etilgan ma'lumotlarni olish uchun ishlatiladi.

**Provide/Inject** - bu rekvizitlar yordamida ma'lumotlarni uzatishga alternativa sifatida ma'lumotlarni almashish usuli.
{% endhint %}

### Ta'minlash / AOK qilish

Komponentlar ichida komponentlar bo'lgan yirik loyihada "App.vue" dan kichik komponentga ma'lumot berish uchun rekvizitlardan foydalanish qiyin bo'lishi mumkin, chunki u ma'lumotlar o'tadigan har bir komponentda rekvizitlarni aniqlashni talab qiladi.

Agar biz rekvizitlar o'rniga provide/inject dan foydalansak, biz faqat taqdim etilgan ma'lumotlarni taqdim etishimiz kerak va biz faqat kiritilgan ma'lumotlarni kiritishimiz kerak.

### Ma'lumotlarni taqdim eting

Biz boshqa komponentlar uchun ma'lumotlarni taqdim qilish uchun "ta'minlash" konfiguratsiya opsiyasidan foydalanamiz:

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <div @click="this.activeComp = 'food-about'" class="divBtn">About</div>
  <div @click="this.activeComp = 'food-kinds'" class="divBtn">Kinds</div>
  <div id="divComp">
    <component :is="activeComp"></component>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: 'food-about',
      foods: [
        { name: 'Pizza', imgUrl: '/img_pizza.svg' },
        { name: 'Apple', imgUrl: '/img_apple.svg' },
        { name: 'Cake', imgUrl: '/img_cake.svg' },
        { name: 'Fish', imgUrl: '/img_fish.svg' },
        { name: 'Rice', imgUrl: '/img_rice.svg' }
      ]
    }
  },
  provide() {
    return {
      foods: this.foods
    }
  }
}
</script> 
```
{% endcode %}

Yuqoridagi kodda "oziq-ovqatlar" massivi endi loyihangizning boshqa komponentlariga kiritilishi uchun taqdim etilgan.

### Ma'lumotlarni kiritish

Endi "Oziq-ovqatlar" massivi "App.vue" da "provide" orqali taqdim etilgan bo'lsa, biz uni "FoodKinds" komponentiga kiritishimiz mumkin.

"FoodKinds" komponentiga kiritilgan "oziq-ovqatlar" ma'lumotlari bilan biz App.vue ma'lumotlaridan "FoodKinds" komponentida turli xil ovqatlarni ko'rsatish uchun foydalanishimiz mumkin:

{% code title="FoodKinds.vue:" %}
```html
<template>
    <h2>Different Kinds of Food</h2>
    <p><mark>In this application, food data is provided in "App.vue", and injected in the "FoodKinds.vue" component so that it can be shown here:</mark></p>
    <div v-for="x in foods">
        <img :src="x.imgUrl">
        <p class="pName">{{ x.name }}</p>
    </div>
</template>

<script>
export default {
    inject: ['foods']
}
</script>

<style scoped>
    div {
        margin: 10px;
        padding: 10px;
        display: inline-block;
        width: 80px;
        background-color: #28e49f47;
        border-radius: 10px;
    }
    .pName {
        text-align: center;
    }
    img {
        width: 100%;
    }
</style>
```
{% endcode %}
